# Shell Scripting — Week 7 Cheatsheet

Keywords: #shellscript #bash #shebang #variables #wildcards #metacharacters #read #echo #expr #arithmetic #logical-operators #special-variables #system-variables #redirection #pipes

---

## Key Definitions
- Shebang: #! /path/to/interpreter (e.g., #!/bin/bash) — specifies the interpreter for the script.  
- Comment: line starting with # (except shebang) — ignored by shell.  
- Variable: name given to a memory location that stores data; used via $name to access value.  
- Positional parameters: $0, $1, $2, ... — command-line arguments passed to script.  
- Special variables: predefined symbols that provide shell/process info (see list).  
- Wildcards (metacharacters): patterns used by the shell to match filenames: *, ?, [range], [!range].  
- Exit status: numeric return code of a command; 0 = success, non-zero = failure.

---

## Formulas / Notation
- Access value of variable: $name  
- Positional args: $0 (script), $1, $2, ...  
- Count of args: $#  
- All args (unquoted/quoted): $* / $@ (see Quick Reference)  
- Last command exit status: $?  
- Current script PID: $$  
- Last background PID: $!  
- Basic arithmetic with expr: expr $a + $b  (spaces required around operators)  
- Preferred arithmetic expansion: $(( a + b ))  (no external command)

---

## Key Commands & Concepts
- Shebang: #!/bin/bash — put as first line to indicate interpreter. #bash #shebang
- Run script:
  - Explicit interpreter: bash script.sh  (works even without shebang)
  - Executable script: chmod +x script.sh; ./script.sh  (requires shebang or executable)
- Echo: echo "text" — prints text; echo -n "prompt"  (suppresses trailing newline so prompt and read appear on same line) #echo
- Read input (interactive scripts): read var  — reads a line from stdin into var #read
- Variables:
  - Assign: name=value  (no spaces around =)
  - Use: echo "$name" or echo $name  (use quotes to preserve whitespace) #variables
- Arithmetic:
  - expr: expr $a + $b  (spaces mandatory)  #expr
  - Arithmetic expansion: result=$((a + b))  (recommended)
- Wildcards / Metacharacters:
  - * = zero or more characters
  - ? = exactly one character
  - [a-z0-9] = one character in range
  - [!...] = one character NOT in range
  Examples: file?.txt, file[1-3].txt, *.txt  #wildcards #metacharacters
- Logical operators:
  - cmd1 && cmd2  — run cmd2 only if cmd1 succeeds (exit status 0)  #logical-operators
  - cmd1 || cmd2  — run cmd2 only if cmd1 fails (non-zero exit)  #logical-operators
- Redirection & pipes (reminder):
  - >, >> (truncate/append), < (input redirect), | (pipe)  #redirection #pipes

---

## Important Properties / Rules
- Variable names:
  - Case-sensitive (NAME ≠ name).  
  - Must not contain spaces; use underscores for separation.  
  - Cannot start with a digit; may start with letter or underscore.  
  - No spaces around assignment: wrong → a = 1 ; correct → a=1.  
- Always use $ to expand a variable when you want its value (e.g., echo "$var").  
- expr requires spaces around operators; failure to space breaks the command.  
- Exit status convention: 0 ⇒ success; any non-zero ⇒ failure/error.  
- Use quotes around expansions that may contain spaces: "$var", "$@".

---

## Special & System Variables (Quick list)
- $0 — script name  
- $1, $2, ... — positional arguments  
- $# — number of positional arguments  
- $* — all positional parameters as a single word/string (when quoted: "$*" → single string)  
- $@ — all positional parameters, expands to separate quoted words (when quoted: "$@" → preserves arg separation)  
- $? — exit status of last command  
- $$ — current shell/script PID  
- $! — PID of last background command  
- $- — current shell options  
- PATH, SHELL, HOME, PWD, USER, UID — environment/system variables (usually uppercase)  #system-variables

---

## Quick Reference (scannable)
- Shebang: #!/bin/bash  (put at top)
- Comment: # this is a comment
- Create/print prompt + read input:
  - echo -n "Enter name: "  ; read name
  - echo "Hello, $name"
- Assign & print:
  - a=10 ; b=20
  - echo "sum=$(expr $a + $b)"   (or sum=$((a+b)); echo "$sum")
- Variable rules:
  - good: my_var=1, _temp=2, var2=3
  - bad: 2var=1, my var=1, var =1
- Wildcards examples:
  - ls *.txt  → all .txt files
  - ls file?.txt  → file plus exactly 1 char before .txt
  - ls file[1-3].txt  → file1.txt file2.txt file3.txt
  - ls file[!0-9].txt  → file followed by non-digit
- Logical operators:
  - mkdir dir && echo "created"    # prints only if mkdir succeeds
  - mkdir dir || echo "already exists"  # prints only if mkdir fails
- Positional args sample usage:
  - script.sh a b c
  - $0 → script.sh ; $1 → a ; $# → 3 ; "$@" → ("a" "b" "c")
- Exit codes:
  - Use exit N to return code N from script; check with $?

---

Keep this as a quick lookup during exams. For usage examples, prefer read + "$@" handling, and prefer $((...)) for arithmetic unless specifically required to use expr.