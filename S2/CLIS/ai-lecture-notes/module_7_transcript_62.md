# /dev/null (Linux) — Quick Cheatsheet
#Keywords: #devnull #/dev/null #stdout #stderr #stdin #redirection #bash #shell #scripting #background #IO #quiet

---

## Key Definitions
- /dev/null: special character device that discards all data written to it and returns EOF on read. #devnull
- stdout (1): standard output file descriptor. #stdout
- stderr (2): standard error file descriptor. #stderr
- stdin (0): standard input file descriptor. #stdin
- Redirection: shell operators that change where fd 0/1/2 point (>, 2>, &>, 2>&1). #redirection
- Quiet/silent mode: executing a command with its output/error sent to /dev/null. #quiet

---

## Formulas / Syntax (common patterns)
- Redirect stdout only:
  - command > /dev/null
- Redirect stderr only:
  - command 2> /dev/null
- Redirect both stdout and stderr (POSIX-safe):
  - command > /dev/null 2>&1
  - (order matters: 2>&1 must come after stdout redirection)
- Bash shorthand (non-POSIX):
  - command &> /dev/null
- Run quietly in background:
  - command > /dev/null 2>&1 &
- Read from /dev/null:
  - returns EOF immediately (no output)

---

## Key Concepts / Usage
- Suppress unwanted output in scripts and CLI: send output to /dev/null. #scripting
- Separate stdout vs. stderr control: use > vs. 2>. #stdout #stderr
- Merge streams: use 2>&1 to point stderr to where stdout currently points. #merge
- Bash-specific &> is shorthand for merging both streams. #bash
- Running background jobs: redirect outputs to avoid terminal clutter. #background
- Common examples:
  - echo "msg" > /dev/null            (discard stdout)
  - ls nonexist 2> /dev/null         (discard errors only)
  - make > /dev/null 2>&1            (run make quietly)

---

## Important Properties / Invariants
- Writes to /dev/null are discarded (no storage). #discard
- Reads from /dev/null immediately give EOF. #EOF
- /dev/null is a device file (character device), available system-wide. #linux
- 2>&1 semantics: duplicates fd 2 to the current target of fd 1; placement matters. #fd
- &> is convenient but not portable to all shells (POSIX sh vs bash). #portability

---

## Quick Reference (scannable)

| Command syntax                      | Effect                                  | Portable? |
|-------------------------------------|-----------------------------------------|-----------|
| command > /dev/null                 | Discard stdout only                      | Yes       |
| command 2> /dev/null                | Discard stderr only                      | Yes       |
| command > /dev/null 2>&1            | Discard stdout and stderr (portable)     | Yes       |
| command &> /dev/null                | Discard stdout and stderr (bash only)    | No (bash) |
| command > /dev/null 2>&1 &          | Quietly run command in background        | Yes       |
| cat /dev/null                       | Immediately EOF (no data)                | Yes       |

Tips:
- Always put 2>&1 after the stdout redirection: wrong order (2>&1 > /dev/null) will not redirect stderr to the file.
- Use 2>/dev/null when you only want to hide error messages but still see normal output.
- Use &>/dev/null for brevity in bash scripts, but prefer > /dev/null 2>&1 for POSIX compatibility.

---

#Tags: #devnull #/dev/null #stdout #stderr #stdin #redirection #bash #shell #scripting #background #ls #rm #echo #make