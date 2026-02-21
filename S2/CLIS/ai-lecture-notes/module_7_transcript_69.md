# VI/Vim Recovery & Linux IO Redirection — Cheatsheet
#hashtags: #vi #vim #editor #recovery #buffers #swapfile #undo #io #io-redirection #stdin #stdout #stderr #pipes #filters #tee #heredoc #redirection #process-substitution

---

## Key Definitions
- vi / vim: modal text editor commonly used on Unix/Linux.  
- Swap file (.swp): temporary file Vim creates to recover crashes/unsaved changes.  
- Buffer: in-memory file copy opened in the editor (multiple buffers possible).  
- Undo/Redo: u = undo, Ctrl‑R = redo; time-travel with :earlier / :later.  
- stdin / stdout / stderr: standard input (fd 0), standard output (fd 1), standard error (fd 2).  
- IO redirection: shell operators that reroute stdin/stdout/stderr to/from files or other commands.  
- Pipe: operator (|) that connects stdout of one command to stdin of another.  
- Filter: command that transforms a data stream (e.g., grep, sed, awk, sort).

---

## Formulas / Notation
- File descriptors: stdin=0, stdout=1, stderr=2  
- Redirect syntax summary:
  - cmd > file  (stdout → file, overwrite)
  - cmd >> file (stdout → file, append)
  - cmd < file  (stdin ← file)
  - cmd 2> file (stderr → file)
  - cmd > file 2>&1 (stdout and stderr → file)  
  - cmd &> file (bash shorthand for both stdout+stderr → file)
  - cmd1 | cmd2 (stdout of cmd1 → stdin of cmd2)
  - <<EOF ... EOF (here‑document: multi-line stdin)
  - <(cmd) or >(cmd) (process substitution)

---

## Key Commands & Concepts — VI / VIM Recovery (#vi #vim #recovery #buffers)
- Swap / crash recovery:
  - When opening a file with existing .swp: follow prompts or use `vim -r filename` to recover.
  - Find swap files: `ls -a | grep '\.swp'` or check /var/tmp, /tmp.
  - Recover manually: `vim -r path/to/.swp` then `:w filename` to save.
- Undo / Redo:
  - `u` = undo, `Ctrl-R` = redo
  - `:earlier 10m` / `:later 5m` = move through time-based undo history
- Buffer navigation:
  - `:ls` or `:buffers` = list buffers
  - `:bN` or `:buffer N` = switch to buffer N
  - `:bn` / `:bp` = next / previous buffer
  - `:bd N` = delete buffer N
- Restore previous version:
  - Use version control (recommended) or use `:earlier` / swap recovery; save with `:w`.
- Quick-safe editing:
  - Abort changes: `:q!` ; Save & exit: `:wq` ; Open another file: `:e filename`
- Practical tips:
  - Save often. If crash, check `.swp` and `vim -r`.
  - Use `:set backup` and `:set undofile` for persistent backups/undo.

---

## IO Redirection Operators & Examples (#io #io-redirection #pipes #filters #tee #heredoc)
- Basic examples:
  - ls > out.txt            # overwrite stdout to out.txt
  - echo "x" >> log.txt    # append to file
  - sort < unsorted.txt | uniq -c | sort -nr > freq.txt
  - grep "pattern" file | wc -l  # filter then count
- stderr handling:
  - cmd 2> err.log          # send stderr to file
  - cmd > out.log 2>&1      # combine stdout+stderr to out.log
  - cmd &> all.log          # bash shorthand: both stdout+stderr
- Pipes & filters:
  - cmd1 | cmd2 | cmd3      # sequential filters; each receives stdout of previous
  - Useful filters: #grep #sed #awk #sort #uniq #head #tail #cut #tr #wc
- tee:
  - cmd | tee file          # write stdout to terminal and file
  - cmd | tee -a file       # append to file
- Here-documents:
  - cat <<EOF > file
    multi-line
    EOF
- Process substitution:
  - diff <(cmd1) <(cmd2)    # compare outputs without temp files

---

## Important Properties / Invariants
- Order matters: redirections are evaluated left-to-right; `cmd >f 2>&1` differs from `cmd 2>&1 >f`.
- Pipe passes stdout only (use 2>&1 if you need stderr).
- Overwrite vs Append: > overwrites; >> appends.
- Filters operate on streams (stdin/stdout) — they do not alter files unless redirected.
- Vim swap files indicate unclean exit; do not blindly delete .swp — recover first when possible.
- Persistent undo requires `:set undofile` (stores undo history on disk).

---

## Quick Reference (Scannable)
- Vim recovery:
  - Open with swap message → follow prompt or `vim -r file`
  - List buffers: `:ls` | switch: `:b N` | close: `:bd N`
  - Undo/Redo: `u` / `Ctrl-R`; timeline: `:earlier` / `:later`
- Common redirections:
  - stdout → file: >
  - stdout append: >>
  - stdin ← file: <
  - stderr → file: 2>
  - combine errs: > file 2>&1  OR &> file
  - pipe: |
  - tee to file + stdout: | tee file
- Examples:
  - Save command output: ps aux > procs.txt
  - Capture errors: gcc prog.c 2> compile.err
  - Save output+errors: ./run > out.log 2>&1
  - Use filters: cat file | grep foo | sort | uniq -c > counts.txt
  - Here-doc: sqlplus user <<EOF ... EOF
- Useful filters (one-word lookup):
  - #grep #sed #awk #sort #uniq #head #tail #cut #tr #wc #tee

---

Keep this sheet for quick lookup during the exam. Practice the exact Vim commands and shell examples to internalize behavior (especially fd ordering and swap recovery steps).