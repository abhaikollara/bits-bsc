# Bash comparison-based branching — Cheatsheet
#bash #shell #if #if-else #if-elif-else #case #test #[] #comparison #operators #-eq #-ne #-lt #-le #-gt #-ge #exit-status #$?

## Key Definitions
- Decision-making: executing different actions based on conditions.
- if statement: branch executed when a condition is true (closed by `fi`).
- if-else / if-elif-else: variants to select alternate branches or multiple conditions.
- case statement: switch-like construct for branching on a single variable's value.
- test command (`test`) / bracket alias (`[ ... ]`): evaluate comparisons, return exit status.
- Exit status: numeric return code of a command; 0 = true/success, non-zero = false/failure.
- `$?`: exit status of the last executed command.

## Syntax & Short Examples
- Basic if:
  - multiline:
    ```
    if CONDITION
    then
      COMMANDS
    fi
    ```
  - with else:
    ```
    if CONDITION; then
      COMMANDS
    else
      OTHER_COMMANDS
    fi
    ```
  - with elif:
    ```
    if C1; then
      ...
    elif C2; then
      ...
    else
      ...
    fi
    ```
- Using test or brackets:
  - `if test A -eq B; then ... fi`
  - `if [ A -eq B ]; then ... fi`
- Quick `$?` check:
  - `some_cmd; echo $?`  # prints exit status (0 → true)

- case (conceptual):
  - Branch on one variable's value (similar to switch). Useful when all branches depend on a single input.

## Operators / Comparisons (numeric)
| Operator | Meaning |
|---:|---|
| `-eq` | equal to |
| `-ne` | not equal to |
| `-lt` | less than |
| `-le` | less than or equal to |
| `-gt` | greater than |
| `-ge` | greater than or equal to |

Usage forms:
- `test A -eq B`
- `[ A -eq B ]`

## Important Properties / Invariants
- Exit status semantics: 0 means condition true (success), any non-zero means false (failure).
- `test` and `[ ... ]` return an exit status — used directly by `if`.
- Bracket form requires spaces: `[ A -eq B ]` (space after `[` and before `]`).
- `then` starts the true-block; `fi` ends the if-block (reverse of `if`).
- `case` is best when branching solely on a single variable's value.

## Quick Reference (scannable)
- if structure: `if COND; then ...; fi`
- if-else: `if COND; then ...; else ...; fi`
- if-elif: `if C1; then ...; elif C2; then ...; else ...; fi`
- test forms:
  - `test A -eq B`
  - `[ A -eq B ]`  ← must have spaces
- Numeric operators: `-eq -ne -lt -le -gt -ge`
- Condition truth: `exit status == 0` → condition is true
- Check last status: `echo $?`
- Use `case` when selecting among many values of one variable (switch-like)

## Quick pitfalls (exam-friendly reminders)
- Missing spaces in `[ ... ]` → syntax error.
- Forgetting `then` or `fi` → syntax error.
- Treat exit status 0 as true (inverted thinking leads to bugs).
- Use numeric operators shown above for integer comparisons.

#hashtags: #bash #shell #if #if-else #if-elif-else #case #test #[] #comparison #operators