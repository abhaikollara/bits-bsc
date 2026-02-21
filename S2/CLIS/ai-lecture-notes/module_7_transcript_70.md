# Week 7 Cheatsheet — vi editor recovery, Linux I/O redirection & common text utilities

#Keywords
#vi #vim #swapfile #backup #registers #undo #redirection #stdin #stdout #stderr #devnull #wc #sort #head #tail #grep #pipe #tee #linux #commands

---

## Key Definitions (one-liners)
- Swap file (.swp): auto-created temp file by vi when editing unsaved content — used for recovery after a crash.  
- Backup file (.bak): explicit copy of a file created in a vi session when backup is enabled.  
- Register: small named storage in vi (names 0–9, A–Z) holding deleted/yanked text.  
- Undo/Redo: revert or reapply edits (undo key used in vi).  
- stdin (fd 0): standard input.  
- stdout (fd 1): standard output.  
- stderr (fd 2): standard error.  
- /dev/null: "black hole" — discard output (no storage).  
- Pipe (|): connect stdout of one command to stdin of another.  
- tee: duplicate output to screen and one or more files.

---

## Formulas / Notation / File descriptors
- stdin = 0, stdout = 1, stderr = 2  
- Redirect stdout: command > file  
- Append stdout: command >> file  
- Redirect stderr: command 2> file  
- Redirect both stdout+stderr to same file: command &> file  (or command >file 2>&1)  
- Send output to black hole: command > /dev/null  (or 2> /dev/null for errors)  
- Pipe: cmd1 | cmd2  
- tee: cmd | tee file1 file2   (append: tee -a)

---

## Key Commands / Concepts (short bullets)
- vi swap/recovery
  - Swap file appears as filename.swp when you re-open an edited-but-unsaved file.
  - Recover: vi -r filename  (prompts to recover from the .swp).
  - If you press Enter at the prompt without recovering, unsaved edits are lost.
- vi backups (per session)
  - Enable backup for session: in command mode type: :set backup
  - Set extension: :set backupextension=.bak
  - Saved backup file appears as filename.bak after write/quit (wq).
- Registers (vi/vim)
  - Numbered registers: 0–9 (transcript: used to store deleted/yanked text).
  - Lettered registers: A–Z (also usable).
  - Deleted/yanked contents can be pasted from a register (examples in lecture: 1p, 2p to paste recent deletions).
  - Inspect registers: :registers (or :reg) shows contents.
- Undo / Redo
  - Use undo key (lecture uses U / undo) to revert recent edits; repeat to step back through changes.
- Redirection & appending
  - Overwrite output: cmd > file  (creates file if missing)
  - Append output: cmd >> file
  - Example: ls > o.txt  (save listing), ls >> o.txt (append another listing)
- Error redirection & combining
  - Redirect stderr: cmd 2> err.txt
  - Send stderr to same destination as stdout: cmd >log.txt 2>&1  (or cmd &>log.txt)
  - Use /dev/null to discard output or errors: cmd > /dev/null  (stdout discarded), cmd 2> /dev/null (errors discarded)
- Pipes
  - Connect commands: ls -l | grep pattern   (grep reads output of ls -l)
- tee (duplicate output)
  - Show output and write to files: cmd | tee out.txt
  - Multiple destinations possible: cmd | tee file1 file2
  - Append mode: tee -a
- wc (word count)
  - wc -w file  → number of words
  - wc -l file  → number of lines
  - wc -c file  → number of bytes/characters
- sort (line sorting)
  - sort file
  - Options:
    - -r : reverse (descending)
    - -n : numeric sort
    - -k N : sort by field/key N
    - -u : unique (remove duplicate output lines)
    - -f : case-insensitive
    - -o out.txt : write sorted output to file
- head / tail
  - head -n N file : first N lines
  - head -c N file : first N bytes
  - tail -n N file : last N lines
  - tail -c N file : last N bytes
  - tail -f file : follow file — show appended lines in real time (useful for logs)
- grep (search/filter)
  - grep pattern file(s)
  - Common options:
    - -i : case-insensitive
    - -r : recursive (search directory and subdirectories)
    - -l : print filenames containing matches (no matching lines)
    - -v : invert match (show non-matching lines)
    - -c : count matching lines
    - -n : show line numbers for matches
  - Use regex/patterns to extract structured data (e.g., emails).
- Practical examples (short)
  - Recover vi swap: vi -r na.txt
  - Create session backup: in vi: :set backup | :set backupextension=.bak | :wq
  - Redirect ls output: ls > o.txt
  - Append with ls -lt: ls -lt >> o.txt
  - Discard ping output: ping host > /dev/null
  - Compile and suppress errors: gcc prog.c 2>/dev/null && echo "compilation done"
  - Pipe + grep example: ls -l | grep fifo
  - Duplicate output to screen and file: somecmd | tee out.txt

---

## Important Properties / Invariants
- Swap file only exists when edits are unsaved and a crash/abnormal close occurs. Reopen prompts recovery.  
- Backup files are only created when backup is explicitly enabled for the session (or via config).  
- Standard descriptors: 0(stdin), 1(stdout), 2(stderr) — use these numbers when redirecting.  
- Pipes pass stdout of the left command as stdin to the right command (stderr unaffected unless redirected).  
- /dev/null discards data; use for suppressing unwanted output.  
- tail -f is for live monitoring (logs); head shows start of files.  
- grep options allow fast filtering/search across files/directories (use -r for recursion, -l to list files only).

---

## Quick Reference (scannable)
- vi recovery: vi -r filename  (.swp = swap file)  #vi #swapfile  
- Make backup in session: :set backup ; :set backupextension=.bak ; :wq  #backup  
- Registers: 0–9, A–Z — store deleted/yanked text; view with :reg  #registers  
- Undo: undo key (repeat to step back)  #undo  
- File descriptors: stdin=0 stdout=1 stderr=2  #stdin #stdout #stderr  
- Redirect stdout: >   (overwrite)  
- Append stdout: >>  (append)  
- Redirect stderr: 2>  ; combine: >file 2>&1  or &>file  
- Discard output: > /dev/null  or 2> /dev/null  #devnull  
- Pipe: cmd1 | cmd2  (stdout->stdin)  #pipe  
- tee: cmd | tee file  (show+save) ; tee -a to append  #tee  
- wc: -w words, -l lines, -c bytes  #wc  
- sort: -r -n -k <field> -u -f -o out  #sort  
- head/tail: head -n / -c ; tail -n / -c ; tail -f (follow)  #head #tail  
- grep: -i -r -l -v -c -n  — pattern/regex search  #grep

---

Keep this sheet handy for quick lookup of commands, options, redirects, and vi recovery steps during the open-book exam. If you want, I can convert this into a single-page PDF or a one-column printable format.