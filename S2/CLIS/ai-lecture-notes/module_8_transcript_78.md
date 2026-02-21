# Interactive Shell Scripts — Read Input Cheatsheet
#keywords: #shell #bash #interactive #read #echo #stdin #stdout #variables #signals #CtrlC #kill #timeout #prompt #I/O

## Key Definitions
- Interactive script: a script that exchanges data with the user (input and/or output). #interactive
- stdin: standard input stream (typically keyboard). #stdin
- stdout: standard output stream (typically console). #stdout
- read: shell builtin that reads a line from stdin and assigns it to variable(s). #read
- echo: prints text to stdout. #echo
- Ctrl+C: keyboard interrupt that sends SIGINT to kill process (manual termination). #CtrlC #signals
- kill: command to send signals (e.g., terminate) to processes. #kill
- timeout: remote connection/session may expire causing script to stop waiting. #timeout
- Variable assignment (by read): input tokens mapped to variables in order. #variables

## Syntax / Formulas / Equations
- Basic read:
  - read var
- Read multiple values:
  - read var1 var2
- Prompt + read (single statement):
  - read -p "Prompt text: " var
- Print:
  - echo "text $var"
- Data flow directions:
  - script -> user: echo (stdout)
  - user -> script: read (stdin)

## Key Algorithms / Concepts
- Making a script interactive:
  - Use echo to ask for input; use read to capture it. #interactive #echo #read
- Waiting behavior when read expects input:
  - Script blocks (waits) until input + Return. #stdin
- Handling multiple inputs:
  - read can split a line into multiple variables (space-separated). #read #variables
- Single-step prompt+read:
  - read -p displays prompt and reads input in one step. #read #prompt
- Outcomes if user provides no input:
  - Wait indefinitely until input. #blocking
  - User can kill process (Ctrl+C or kill). #CtrlC #kill
  - Remote session may timeout and terminate waiting. #timeout

## Important Properties / Invariants
- read reads a single line (terminated by Return) from stdin and assigns to variables in sequential order. #read
- If fewer variables than fields: last variable gets the remainder. #variables
- If more variables than fields: extra variables become empty. #variables
- echo writes output immediately to stdout; useful to prompt or display results. #echo
- Combining prompt and read reduces lines and makes script concise: read -p. #prompt

## Quick Reference (scannable)
- Prompt then read (two lines)
  - echo -n "Enter name: "
  - read name
- Prompt+read (one line)
  - read -p "Enter two numbers (a b): " a b
- Read two values into x and y:
  - read x y
  - echo "x=$x, y=$y"
- Print result (example sum):
  - echo "Sum = $((x + y))"
- Blocking behavior:
  - While read waiting → script pauses until Return or termination. #blocking
- Terminate waiting:
  - Ctrl+C (SIGINT) from same terminal. #CtrlC
  - kill <pid> from another shell. #kill
  - remote session timeout/disconnect. #timeout

## Examples (compact)
- Single value:
  - read -p "Name: " name
  - echo "Hello, $name"
- Two values:
  - read -p "Enter two numbers: " x y
  - echo "x=$x y=$y"

#hashtags (all major items): #interactive #shell #bash #read #echo #stdin #stdout #variables #prompt #CtrlC #kill #timeout #signals

