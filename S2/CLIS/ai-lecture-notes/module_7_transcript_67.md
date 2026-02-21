# Linux Pipe Command — Cheatsheet
#hashtags: #pipe #linux #shell #bash #filters #stdin #stdout #stderr #pipeline #grep #sort #uniq #wc #awk #xargs #ps #kill #ls #cat #tee #cut #head #tail #pipefail

## Key Definitions
- Pipe (|): connect stdout of one command to stdin of the next. #pipe
- Pipeline: sequence of commands joined by |. #pipeline
- Filter: a command that reads stdin, writes transformed output to stdout (e.g., #grep, #sort). #filters
- stdout (fd 1): standard output stream. #stdout
- stdin (fd 0): standard input stream. #stdin
- stderr (fd 2): standard error stream (not piped by default). #stderr
- Pipe buffer: kernel buffer used to transfer data between processes (no temp files). #pipe
- Exit status of pipeline: by default the last command’s exit code; use `set -o pipefail` to detect failures earlier. #pipefail

## Syntax / Formulas / Notation
- Basic pipeline: command1 | command2 | command3
- Redirect stderr into pipe:
  - Bash shorthand: command |& cmd2   (equivalent to 2>&1 |)
  - Explicit: command 2>&1 | cmd2
- Ensure pipeline fails if any command fails:
  - set -o pipefail
- Common pattern: producer | filters... | consumer

## Key Commands / Concepts (quick bullet points)
- #ls | #grep
  - ls -l | grep 'pattern' → filter listing lines matching pattern
- #cat | #grep | #wc
  - cat file | grep 'pattern' | wc -l → count matching lines (wc -l)
- #sort | #uniq
  - cat file | sort | uniq → sorted unique lines
  - uniq requires sorted input for full de-duplication; use `uniq -c` to count
- #ps | #grep | #awk | #xargs
  - ps aux | grep firefox | awk '{print $2}' | xargs kill -9  
    → find PIDs for processes with "firefox" and force-kill
- #awk
  - awk '{print $n}' → extract nth whitespace-separated column
- #xargs
  - xargs -r -n1 command → run command with arguments from stdin; -r avoid running if no input
- #tee
  - cmd | tee file | nextcmd → split stream: write to file and pass through
- Common text utilities: #cut, #head, #tail, #tr, #sed

## Important Properties / Invariants
- Each pipeline stage runs as its own process; stages execute concurrently. #pipeline
- Order of lines is preserved through standard text filters (unless a filter reorders them, e.g., #sort). #filters
- No intermediate temp files (efficient for large streams); uses kernel pipe buffer. #pipe
- stderr is not piped by default — must redirect if you want it included. #stderr
- Pipeline exit code behavior:
  - Default: exit code = last command’s exit code
  - With `set -o pipefail`: non-zero if any stage fails → better for scripts. #pipefail
- Quoting matters: protect patterns and whitespace when piping to commands that interpret them. #shell

## Quick Reference (scannable)
- Basic:
  - command1 | command2
- Common flags:
  - grep: -i (ignore-case), -v (invert), -E (extended regex), -F (fixed strings)
  - sort: -n (numeric), -r (reverse)
  - uniq: -c (count), -d (duplicates), -u (unique)
  - wc: -l (lines), -w (words), -c (bytes)
  - awk: '{print $1}' (column 1)
  - xargs: -n1 (one arg per command), -r (no run if empty), -I{} (replace token)
  - ps: ps aux or ps -ef (full listings)
  - kill: -9 (SIGKILL), prefer graceful term first (kill PID)
- Examples:
  - List files with "file" in name: ls -l | grep 'file'
  - Count pattern matches: grep 'pattern' file | wc -l
  - Unique sorted list: sort file | uniq
  - Kill processes by name: ps aux | grep name | awk '{print $2}' | xargs kill
  - Pipe stderr: cmd 2>&1 | grep 'error'  OR  cmd |& grep 'error'
  - Split output to file and next cmd: cmd | tee out.txt | othercmd
- Performance notes:
  - Streaming via pipes is memory-efficient for large data (no temp files).
  - Excessive use of external commands may cost CPU; combine work in single tool (e.g., awk) when possible.

Keep this cheatsheet next to your terminal: focus on patterns (producer | filters | consumer) and common flags for quick composition.