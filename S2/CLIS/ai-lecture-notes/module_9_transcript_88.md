# Bash Loops & Flow Control — #while #until #break #continue #bash

## Keywords
#bash #loops #controlflow #while #until #break #continue #do-done #infinite-loop #ctrl-c

---

## Key Definitions
- #while: Loop that repeats while a command/condition evaluates to true (exit status 0).  
- #until: Loop that repeats until a command/condition evaluates to true (runs while false / non‑zero exit).  
- #break: Exit the current loop (or N levels with argument).  
- #continue: Skip remainder of current iteration and proceed to next (or N levels with argument).  
- #do-done: Delimiters that enclose the loop body in shell.  
- #infinite-loop: A loop with a condition that always evaluates true (e.g., `while true`).  
- #ctrl-c: Keyboard interrupt to forcibly stop a running loop/process.

---

## Formulas / Evaluation Rules
- Shell truth: command exit status 0 → true; non‑zero → false. (#bash)
- while syntax: `while <command>; do <body>; done` — executes while `<command>` returns 0. (#while)
- until syntax: `until <command>; do <body>; done` — executes while `<command>` returns non‑zero; stops when it returns 0. (#until)
- Arithmetic test examples:
  - `[ "$i" -lt 10 ]` → test builtin (0=true)
  - `(( i < 10 ))` → arithmetic (0=true)

---

## Key Algorithms / Concepts
- #while loop
  - Re-evaluates condition before each iteration.
  - Typical use: iterate while index less than limit.
- #until loop
  - Reverse of while: runs while condition is false; stops when true.
  - Use when you want to run until some success condition.
- #infinite-loop
  - `while true; do ...; done` — must be terminated (e.g., `break` or Ctrl+C).
- #break
  - `break` : exit current loop immediately.
  - `break N` : exit N nested loops (bash supports numeric arg).
- #continue
  - `continue` : skip remainder of current iteration, proceed to next.
  - `continue N` : apply to Nth enclosing loop.
- Scope
  - `break`/`continue` valid inside `for`, `while`, `until`. (#do-done)

---

## Important Properties / Invariants
- Condition checked before entering each iteration (pre-check loop). (#while #until)
- Loop body is strictly between `do` and `done`. (#do-done)
- `while` runs while condition is true (exit status 0); `until` runs while condition is false (non‑zero).
- `continue` does not exit loop — it jumps to next condition evaluation.
- `break` terminates loop immediately and resumes after `done`.
- Use `Ctrl-C` to interrupt long or infinite loops manually. (#ctrl-c)
- When using test `[` or `(( ))`, ensure proper spacing and quoting for variables.

---

## Quick Reference (scannable)
Syntax:
- while:
  - `while <command>; do <commands>; done`
- until:
  - `until <command>; do <commands>; done`
- infinite:
  - `while true; do <commands>; done`  # use `break` or Ctrl+C to stop
- break / continue:
  - `break` / `break N`
  - `continue` / `continue N`

Common examples:
- Count up (while):
  - `i=1; while [ "$i" -le 10 ]; do echo $i; i=$((i+1)); done`
- Skip a value (continue):
  - `i=1; while [ $i -le 10 ]; do (( i==5 )) && { i=$((i+1)); continue; }; echo $i; i=$((i+1)); done`
- Break on condition:
  - `i=1; while true; do echo $i; (( i==8 )) && break; i=$((i+1)); done`
- Until example:
  - `i=1; until [ "$i" -gt 10 ]; do echo $i; i=$((i+1)); done`  (#runs while i <= 10)

Behavior checklist:
- Condition success = exit status 0 → treated as true.
- `while` executes when condition is true; `until` executes when condition is false.
- `do`/`done` required block markers.
- `break`/`continue` affect innermost loop unless numeric arg used.

---

Keep this sheet nearby when writing shell loops — copy common patterns and adjust conditions/tests accordingly.