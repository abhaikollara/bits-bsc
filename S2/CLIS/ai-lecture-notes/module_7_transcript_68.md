# Linux tee — Cheatsheet
#hashtags: #tee #pipe #stdin #stdout #redirection #append #ignore-interrupt #logfile #ls #echo #file #shell

## Title
Linux tee command — capture and display command output simultaneously

---

## Key Definitions
- tee: Reads from standard input and writes to standard output and one or more files simultaneously. #tee #stdin #stdout
- pipe (|): Connects stdout of one command to stdin of another. #pipe
- redirection (>): Sends stdout to a file (overwrites). (>>) Appends to file. #redirection #file
- append (-a): Option to add output to end of file(s) instead of overwriting. #append
- ignore-interrupt (-i): Option to ignore interrupt (SIGINT) while writing. #ignore-interrupt

---

## Syntax / Formulas
- Basic: other-command | tee [options] file1 [file2 ...]
- Common options:
  - -a : append to files (not overwrite)
  - -i : ignore interrupt signals (SIGINT)

---

## Key Commands / Examples
- Capture ls output to file and still print:
  - ls -l | tee list.txt  #ls #tee
- Append a line to a log while printing:
  - echo "message" | tee -a log.txt  #echo #append #logfile
- Duplicate output to multiple files:
  - ls | tee file1.txt file2.txt  #multiple-files
- Overwrite default behavior:
  - tee file.txt  (overwrites file.txt) #redirection

---

## Important Properties / Invariants
- Writes to stdout and to all listed files (simultaneous duplication). #stdout
- By default, tee overwrites files; use -a to append. #append
- Accepts multiple file arguments — duplicates output to each file. #multiple-files
- Useful for creating logs while preserving interactive terminal output. #logfile
- tee processes data from stdin (so always used in a pipeline or with input redirection). #stdin #pipe

---

## Quick Reference (scannable)
- Syntax: cmd | tee [ -a | -i ] file1 [file2 ...]
- Overwrite file: tee file.txt  → file.txt replaced
- Append file: tee -a file.txt  → new content appended
- Ignore Ctrl+C while writing: tee -i file.txt
- Multiple files: tee f1 f2 f3  → same output saved to all
- Use when you want both terminal output and saved file (vs > which hides terminal). #redirection

---

## One-line Reminders
- Use tee to "tee-off" output to terminal + files. #tee
- Use -a to preserve existing file contents. #append
- Use -i to avoid interruption while logging. #ignore-interrupt

---

End of cheatsheet — quick search tags at top for fast lookup.