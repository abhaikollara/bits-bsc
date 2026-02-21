# Standard Error Redirection (Shell/Bash)  
#keywords: #stderr #stdout #redirection #bash #shell #pipes #filedescriptors #2> #2>&1 #&> #>/dev/null #append #grep

## Key Definitions
- stdin (fd 0): standard input stream.  
- stdout (fd 1): standard output stream (normal program output).  
- stderr (fd 2): standard error stream (error/diagnostic messages).  
- redirection: send a file descriptor to a file or another descriptor (e.g., 2>error.log).  
- pipe (|): sends stdout of left command to stdin of right command (stderr unaffected unless redirected).

## Notation / File descriptors
- 0 = stdin, 1 = stdout, 2 = stderr  
- > : redirect (truncate) stdout (same as 1>)  
- >> : append stdout (same as 1>>)  
- 2> / 2>> : redirect/append stderr  
- 2>&1 : duplicate fd 2 to point where fd 1 currently points  
- &> / &>> (bash): redirect both stdout+stderr (truncate/append)

## Common Commands / Examples
- Redirect stderr to a file:
  - command 2> error.log
  - e.g., ls nonexistingdir 2> error.log
- Redirect stdout and stderr to separate files:
  - command > out.txt 2> error.log
  - e.g., ls /usr/bin > file.txt 2> error.log
- Combine stdout and stderr into one file:
  - command > output.log 2>&1
  - bash shorthand: command &> output.log
- Pipe combined stdout+stderr to another command:
  - command 2>&1 | grep pattern
  - e.g., ls nonexist 2>&1 | grep bin
- Discard output:
  - stdout: command > /dev/null
  - stderr: command 2> /dev/null
  - both: command &> /dev/null
- Append instead of overwrite:
  - stderr append: command 2>> error.log
  - both append (bash): command &>> output.log
  - combined append without &>>: command >> out.log 2>&1

## Important Properties / Invariants
- Default destination for stdout/stderr: terminal (tty).  
- Pipes only carry stdout by default; redirect stderr to pipe explicitly (2>&1 | ...).  
- Order matters: 
  - Correct to combine both to file: command > out 2>&1 (redirect stdout to file, then make stderr go to same place).
  - Wrong order example: command 2>&1 > out — this makes stderr point to the original stdout (usually terminal), then redirects stdout to file, leaving stderr going to terminal.
- & notation (2>&1) duplicates file descriptors, not strings — it follows current target of fd 1 at time of duplication.
- > truncates file; >> appends.

## Quick Reference Table
| Action | Syntax | Notes |
|---|---:|---|
| Redirect stdout (truncate) | command > out.txt | same as 1>out.txt |
| Append stdout | command >> out.txt | 1>>out.txt |
| Redirect stderr (truncate) | command 2> err.log | |
| Append stderr | command 2>> err.log | |
| Redirect both (bash) | command &> all.log | bash shorthand |
| Redirect both (portable) | command > all.log 2>&1 | portable POSIX form |
| Pipe stderr+stdout | command 2>&1 \| other | sends both into pipe |
| Discard stderr | command 2> /dev/null | |
| Discard both | command &> /dev/null | |

## Quick Patterns / Cheats
- Capture only errors: cmd 2>errors.txt
- Capture only normal output: cmd >out.txt
- Capture both: cmd >all.txt 2>&1
- Send errors to stdout (so they flow into a pipe): cmd 2>&1 | grep ...
- Keep stdout to terminal, send errors to file: cmd 2>err.log
- Keep errors to terminal, send stdout to file: cmd >out.txt
- Append instead of overwrite: replace > with >>

Keep this sheet near your exam for fast lookup of syntax and common pitfalls (especially the order rule for 2>&1).