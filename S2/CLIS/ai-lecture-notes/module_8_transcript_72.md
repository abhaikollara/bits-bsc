# Shell Script Basics — Quick Cheatsheet
#keywords: #shell #shellscript #bash #shebang #comments #linecontinuation #semicolon #exitstatus #echo #chmod #permissions #execution #stdout #scripting

## Key Definitions
- Shebang (#shebang): First-line marker starting with #! specifying the interpreter (e.g., #!/bin/bash).
- Shell script (#shellscript): A plaintext file containing shell commands and logic to be executed by a shell.
- Comment (#comments): Line beginning with # (ignored by shell; except shebang uses #!).
- Line continuation (#linecontinuation): Ending a line with backslash \ to join with next line.
- Command separator (#semicolon): Semicolon ; separates multiple commands on one line.
- Exit status (#exitstatus): Integer return code from a script/command (0 = success, non‑zero = error).
- Standard output (#stdout): Default stream for normal program output (e.g., echo prints to stdout).
- Execute permission (#permissions): File permission bit required to run file directly (set via chmod).

## Formulas / Notation
- Exit codes range: 0 = success; 1–255 = failure/error (shell uses unsigned 8-bit).
- Last command status variable: $? contains the exit status of most recently run command.
- Shebang format: #! /path/to/interpreter [optional-arg]

## Key Concepts / Commands (#bash #echo #chmod #execution)
- Shebang usage:
  - Place as first line: #!/bin/bash (or #!/usr/bin/env bash).
  - Kernel uses shebang when executing file directly (./script).
- Comments:
  - Use #: # this is a comment
  - Shebang is an exception: starts with #! and is not a regular comment.
- Line continuation:
  - Use backslash at end of line: echo "long \
    line"
- Command separator:
  - Use semicolon: cmd1; cmd2 (executes sequentially).
- Exit status:
  - Explicit exit: exit N
  - If no exit, script returns exit status of last executed command.
  - Check with: echo $?
- Printing:
  - echo "Hello World" prints to stdout.
- Execution methods:
  - Invoke interpreter explicitly: bash script.sh
  - Make executable and run directly:
    - chmod +x script.sh
    - ./script.sh
  - If run via interpreter explicitly, shebang ignored for interpreter selection.
- Permissions:
  - Add execute bit: chmod +x script.sh
  - Common mode for executables: chmod 755 file (owner rwx, group/others rx)
- Interpreter selection rules (priority):
  - If run with interpreter: interpreter chosen by command (bash script.sh).
  - If run directly (./script): kernel reads shebang to choose interpreter; if missing, default shell behavior varies.

## Important Properties / Invariants
- Shebang must be the very first line to be recognized as interpreter directive.
- Comments (starting with #) do not affect execution.
- Backslash at EOL is the only portable line-joining mechanism in shell scripts.
- Semicolon is equivalent to a newline for separating commands on same line.
- Scripts without execute bit can still run by calling an interpreter explicitly.
- Exit codes are limited to 0–255; larger values are truncated modulo 256.
- $? is updated after each command — read it immediately if needed.

## Quick Reference (scannable)
- Create script header:
  - #!/bin/bash
- Basic hello world:
  - echo "Hello World"
  - exit 0
- Run script (two ways):
  - bash script.sh
  - chmod +x script.sh
  - ./script.sh
- Make executable:
  - chmod +x script.sh
  - chmod 755 script.sh (common)
- Check last exit status:
  - echo $?
- Explicit exit:
  - exit N  # N in [0..255]
- Line continuation:
  - command arg1 arg2 \
    arg3
- Multiple commands same line:
  - cmd1; cmd2; cmd3
- Comment:
  - # comment text
- Shebang examples:
  - #!/bin/bash
  - #!/usr/bin/env bash

Keep this sheet near your exam sheet for quick lookup of syntax and execution rules. #scripting #shell #bash #shebang #chmod #exitstatus