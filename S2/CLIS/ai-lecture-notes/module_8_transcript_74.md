# Shell Metacharacters & Redirection — Cheatsheet
#hashtags: #shell #metacharacter #redirection #stdin #stdout #pipe #append #quoting #escape #comment #conditional-execution #sequential-execution #command-substitution #wc #greater-than #less-than #semicolon #ampersand #double-ampersand #double-pipe #backslash #backquote #single-quote #double-quote #newline #space #tab

---

## Key Definitions (one-line)
- Metacharacter: a character the shell treats specially (terminates/controls words) unless quoted.  
- stdout: standard output stream (file descriptor 1).  
- stdin: standard input stream (file descriptor 0).  
- Redirection: sending stdout/stdin to/from files using special symbols.  
- Pipe: connect stdout of one command to stdin of another.  
- Quoting: using single/double quotes or backslash to prevent special treatment of metacharacters.  
- Escape (backslash \): makes the next character literal.  
- Command separator (;): run commands sequentially, regardless of success.  
- Conditional AND (&&): run second command only if first succeeds (exit status 0).  
- Conditional OR (||): run second command only if first fails (non-zero exit status).  
- Comment (#): marks the rest of the line as a comment.  
- Backquote (`...`): command substitution (execute enclosed command and use its output).

---

## Formulas / Notation (quick mapping)
- command > file         — redirect stdout to file (overwrite)  
- command >> file        — append stdout to file  
- command < file         — take stdin from file  
- cmd1 | cmd2            — pipe: stdout(cmd1) → stdin(cmd2)  
- cmd1 ; cmd2            — run cmd1 then cmd2 (always)  
- cmd1 && cmd2           — run cmd2 only if cmd1 exits 0 (success)  
- cmd1 || cmd2           — run cmd2 only if cmd1 exits non-zero (failure)  
- # comment text         — comment; ignored by shell  
- `command` or $(command) — command substitution (backquote mentioned)  
- \char                  — escape char so it's treated literally

---

## Key Algorithms / Concepts (bulleted)
- Redirection: use > (overwrite) and >> (append) to send stdout to files. #> #>> #redirection  
- Input redirection: use < to feed a file as stdin to a command. #< #stdin  
- Pipes: use | to chain commands, passing output → input. Commands run concurrently; data flows via pipe buffer. #pipe  
- Sequential execution: use ; to run commands one after another regardless of exit status. #semicolon #sequential-execution  
- Conditional execution:  
  - && (AND): next runs only on success of previous. #&& #conditional-execution  
  - || (OR): next runs only on failure of previous. #|| #conditional-execution  
- Quoting / escaping: prevent metacharacter interpretation with single quotes, double quotes, or backslash. #quoting #backslash #single-quote #double-quote  
- Comments: # begins a comment to end-of-line. #comment  
- Command substitution: use backquotes (`...`) (transcript) to use command output as text. #backquote #command-substitution

---

## Important Properties / Invariants
- Quoted metacharacters are treated as literal characters (no special meaning). #quoting  
- Whitespace (space, tab, newline) and metacharacters terminate words unless quoted/escaped. #space #tab #newline  
- Exit status convention: 0 = success; non-zero = failure — used by && and ||. #exit-status  
- Semicolon (;) does not check exit status — both commands always run. #semicolon  
- && short-circuits on failure; || short-circuits on success. #&& #||  
- A pipe connects stdout of left command to stdin of right command (no file intermediate). #pipe  
- Appending (>>) preserves existing file contents and adds output to end. #append

---

## Quick Reference (scannable)
- > file         : overwrite file with command stdout     — e.g., cat file1 > out.txt  #>  
- >> file        : append stdout to file                  — e.g., echo Hello >> out.txt  #>> #append  
- < file         : use file as stdin                      — e.g., wc < temp.txt  #< #stdin  
- cmd1 | cmd2    : pipe output to next command            — e.g., cat temp.txt | wc  #pipe #wc  
- cmdA ; cmdB    : run A then B (always)                  — e.g., date ; who  #semicolon  
- cmdA && cmdB   : run B only if A succeeds               — e.g., mkdir d && cd d  #&&  
- cmdA || cmdB   : run B only if A fails                  — e.g., test -f f || echo "missing"  #||  
- # text         : comment the rest of the line           — e.g., # this is a comment  #comment  
- `cmd` or $(cmd): substitute output of cmd into line     — e.g., echo `date`  #backquote #command-substitution  
- \char          : escape a special character             — e.g., echo \$HOME prints $HOME  #backslash  
- Quoting rules:  
  - 'single quotes'  — everything literal, no expansion  #single-quote  
  - "double quotes"  — literal except $, `, \ (some expansion)  #double-quote

---

Examples from lecture (copyable)
- cat file > temp.txt        — write output to temp.txt  #>  
- echo Theekshna >> temp.txt — append string to file     #>>  
- wc < temp.txt              — count words from file     #< #wc  
- cat temp.txt | wc          — pipe cat → wc             #pipe #wc  
- cmd1 ; cmd2                — run cmd1 then cmd2        #semicolon  
- cmd1 && cmd2               — run cmd2 only if cmd1 succeeds  #&&  
- cmd1 || cmd2               — run cmd2 only if cmd1 fails     #||

---

Keep this sheet near your reference material for quick lookup of metacharacter behavior and common redirection/pipe patterns.