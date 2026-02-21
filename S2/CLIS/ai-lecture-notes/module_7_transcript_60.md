# Standard Output Redirection & Appending — Cheatsheet
#hashtags: #stdout #standardoutput #redirection #append #pipe #piping #bash #shell #ls #grep #echo #files #logging #backup #filedescriptors #stdin #stderr

---

## Key Definitions
- STDOUT: Standard output stream (default destination = terminal). #stdout #standardoutput  
- Redirection: Changing where a command's output goes (file, another command). #redirection  
- Append: Add output to end of an existing file (do not overwrite). #append  
- Pipe: Send stdout of one command as stdin to another command (|). #pipe #piping  
- File descriptor: Integer identifier for I/O streams (1 = stdout, 2 = stderr, 0 = stdin). #filedescriptors

---

## Syntax / Formulas (quick patterns)
- Redirect stdout (replace): command > file
- Append stdout: command >> file
- Pipe stdout to another command: command1 | command2
- Explicit fd redirection: command 1> file   (same as >) ; command 2> file (stderr)
- Combine stdout+stderr to file: command &> file  (bash) or command > file 2>&1

---

## Key Algorithms / Concepts
- Output capture: Use > or >> to store command output into files (#logging, #backup).  
  - Example: ls > list.txt  — store directory listing (overwrites). #ls #files
  - Example: echo "note" >> list.txt  — append line to list.txt. #echo
- Appending vs Overwriting:  
  - > truncates/overwrites file. #redirection  
  - >> appends to existing file (creates file if missing). #append
- Piping (connect commands):  
  - command1 | command2 — passes stdout of command1 into stdin of command2. #pipe  
  - Example: ls /usr/bin | grep zip > zipfiles.txt  — filter and save results. #ls #grep
- Use cases: creating logs, backups of output, filtering output before saving. #logging #backup

---

## Important Properties / Invariants
- Default STDOUT destination = terminal; redirection changes that for the command. #stdout  
- > creates the target file if it doesn't exist; truncates if it does. #redirection  
- >> creates the target file if it doesn't exist; preserves existing content and appends. #append  
- Pipe (|) transfers only stdout by default (stderr not piped unless redirected). #pipe #stderr  
- Order matters: redirections and pipes are set up by the shell before executing commands. #bash  
- File permissions affect ability to create/overwrite files (may require sudo). #files
- Use explicit fd (1,2) when you need to separate or combine stdout/stderr. #filedescriptors

---

## Quick Reference (scannable)
- Overwrite file: cmd > file
- Append to file: cmd >> file
- Pipe to filter: cmd1 | cmd2
- Save filtered output: cmd1 | cmd2 > out.txt
- Append filtered output: cmd1 | cmd2 >> out.txt
- Redirect stderr only: cmd 2> errors.log
- Redirect both to same file: cmd > all.log 2>&1   OR   cmd &> all.log (bash)
- Check contents: cat file.txt
- Example workflows:
  - Snapshot directory: ls > list.txt        (#backup)
  - Add a log line: echo "update" >> list.txt (#logging)
  - Filter & save: ls /usr/bin | grep zip > zipfiles.txt (#ls #grep)

---

Keep this sheet handy during open-book exams for quick lookup of redirection/appending patterns and examples.