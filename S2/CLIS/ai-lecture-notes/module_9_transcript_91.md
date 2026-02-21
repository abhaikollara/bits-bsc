# Bash File Handling — Reading & Writing Cheatsheet

#keywords: #bash #file-handling #redirection #cat #read #while-loop #tee #stdout #input-redirection #append #overwrite #command-substitution

---

## Key Definitions
- cat: prints file(s) to stdout; can be used for command-substitution. #cat
- Redirection: changing where a command reads input from or writes output to. #redirection
- stdout: standard output stream (file descriptor 1). #stdout
- Input redirection `<`: supply a file as stdin to a command or loop. #input-redirection
- Output redirection `>`: write stdout to file (creates/overwrites). #overwrite
- Append redirection `>>`: append stdout to file (creates if missing). #append
- tee: writes stdin to both screen (stdout) and file. #tee
- Command substitution: capture command output into a variable, e.g. `var=$(cmd)` or faster `var=$(<file)`. #command-substitution
- while read loop: iterates file line-by-line using input redirection. #while-loop

---

## Formulas / Syntax (quick)
- Read whole file into variable:
  - `value=$(cat "file.txt")`  # uses cat
  - `value=$(< file.txt)`      # faster, no forked process
- Input redirection to a command:
  - `command < input.file`
- Line-by-line:
  - `while read line; do <commands>; done < input.file`
- Write output (overwrite):
  - `command > out.txt`
- Write output (append):
  - `command >> out.txt`
- tee (write & display):
  - `command | tee out.txt`
  - append with tee: `command | tee -a out.txt`

---

## Key Concepts / Usage (bulleted)
- #ReadingEntireFile
  - Use `cat` or command substitution to capture entire file content into a variable.
  - Prefer `$(< file)` for performance (no fork).
- #ReadingLineByLine
  - `while read line; do ...; done < file` — common pattern for processing each line.
- #WritingToFile
  - `>` creates file or overwrites existing file.
  - `>>` creates file or appends to existing file.
- #DisplayAndSave
  - `tee` lets you see output on terminal and save to file at same time.
  - `tee -a` appends instead of overwriting.
- #StdStreams (note)
  - Redirections above affect stdout by default. Use `2>` for stderr (not from transcript but useful).

---

## Important Properties / Invariants
- `>` overwrites file contents; existing data is lost.
- `>>` preserves existing content and appends new output.
- Using redirection (`>` / `>>`) sends command output to file only — nothing appears on terminal unless you also use `tee` or duplicate output streams.
- `while read` consumes stdin — use input redirection (`< file`) to feed a file rather than piping if you need the loop to read from the file.
- Command substitution `$(cmd)` executes cmd and captures its stdout; `$(< file)` is a shortcut that reads file directly without running `cat`.
- If target file does not exist, `>` and `>>` will create it.

---

## Quick Reference (scannable)
- Read file into var:
  - `v=$(cat "f")`  OR  `v=$(< f)`  ← faster
- Loop lines:
  - `while IFS= read -r line; do echo "$line"; done < file`
- Overwrite file:
  - `echo hi > out.txt`  (#creates or replaces)
- Append file:
  - `echo hi >> out.txt` (#creates or appends)
- Show and save:
  - `ls | tee list.txt`  (#prints and writes)
  - Append with tee: `cmd | tee -a file`
- Input redirection:
  - `cmd < input.file`
- Behavior summary table:

| Symbol/Command | Effect | Creates file? | Overwrites? | Shows on terminal? |
|---|---:|:---:|:---:|:---:|
| `>` | write stdout to file | yes | yes | no |
| `>>` | append stdout to file | yes | no (append) | no |
| `<` | feed file as stdin to command | n/a | n/a | n/a |
| `| tee file` | write stdout to file and stdout | yes | depends (tee vs tee -a) | yes |

---

Keep this sheet handy for quick commands and syntax during an open-book exam.