# Standard Input Redirection (Linux) — Cheatsheet
#hashtags: #stdin #input-redirection #redirection #shell #linux #bash #pipes #cat #wc #grep #sort #automation

## Key Definitions (one-liners)
- STDIN: Standard input stream (file descriptor 0), default = keyboard. #stdin
- Input redirection ("<"): Shell operator that makes a command read its stdin from a file. #input-redirection
- Pipe ("|"): Sends stdout of left command to stdin of right command. #pipes
- Command reading stdin: A program that reads input from file descriptor 0 (keyboard by default). #shell

## Syntax / Formulas
- Basic input redirection:
  - command < input-file
- Pipe:
  - command1 | command2
- Combined:
  - command < file | command2
- File descriptor:
  - STDIN = 0 (redirects affect FD 0)

## Key Commands / Concepts (brief)
- cat
  - Displays file contents. Example: cat < input.txt or cat input.txt. #cat
- wc
  - Word/line/byte counts. Options: -w (words), -l (lines), -c (bytes/chars). Example: wc -w < input.txt (counts words). #wc
- grep
  - Search for patterns in input. Example in pipeline: grep example. #grep
- sort
  - Sort lines of text. Example: sort < input.txt. #sort
- Pipes + redirection
  - Use < to feed a file into a pipeline or use commands that output to pipe. Example: cat < input.txt | grep example | wc -l. #pipes
- Use cases
  - Automation, batch processing, pipelines, combining commands. #automation

## Important Properties / Invariants
- "<" directs file → command stdin; it does not change the file. #input-redirection
- Only affects commands that read from STDIN (FD 0). If a command does not read stdin, "<" has no effect. #stdin
- Many utilities accept filenames as arguments; using "<" is equivalent only if the program reads stdin when no filename is given. #shell
- You can chain redirection and pipes: redirection happens before piping into next command (shell sets up FDs then runs commands). #pipes
- STDIN is FD 0; stdout FD 1; stderr FD 2. (Useful when combining redirections.) #stdin

## Quick Reference (scannable)
- Syntax examples:
  - Read file into command: command < input.txt
  - Count words in file: wc -w < input.txt  → outputs number of words  #wc
  - Count lines matching pattern: cat < input.txt | grep example | wc -l  → outputs count of matching lines  #grep
  - Sort a file: sort < input.txt  → prints sorted lines  #sort
- Common wc options:
  - -w = words, -l = lines, -c = bytes/chars  #wc
- When to use "<":
  - Command expects interactive/STDIN input and you want to supply a file automatically. #input-redirection
- When "<" is meaningless:
  - Command only works with filenames passed as arguments and doesn't read stdin. #shell
- File descriptor note:
  - Redirecting stdin uses FD 0:  command 0< file  (equivalent to command < file)

Keep this sheet for quick lookup during open-book exams: look up syntax, which commands read stdin, and common one-line examples.