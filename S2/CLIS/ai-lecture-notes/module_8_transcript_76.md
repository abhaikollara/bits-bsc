# Bash Variables — Types, Usage & Common System Variables
#hashtags: #variable #bash #shell #environment #systemvariable #uservariable #ENV #echo #BASH #BASH_VERSION #BASHPID #HOME #PATH #PWD

## Key Definitions
- Variable: Named memory location (container) that holds a value which can change.
- System variable / Environment variable: Shell/OS-created variable required for shell operation (maintained by system).
- User-defined variable: Variable created and maintained by the programmer/user for scripts.
- Shell variable: Variable attached to a shell instance (e.g., stores shell path or settings).
- Memory location: Unique address in primary memory referred to by a variable name.

## Formulas / Syntax (quick reference)
- Access value: $VARNAME  (use dollar sign before name to read value)
- List environment variables: env
- Print variable: echo $VARNAME
- Note: System variables are conventionally in ALL CAPS.

## Key Concepts
- Purpose of variables: store data in memory, allow changing parts of commands dynamically.
- Types in Bash:
  - #systemvariable / #environment: created by OS/shell, used by shell to function.
  - #uservariable: created by user for scripts/programs.
- Viewing/printing:
  - Use env to list environment variables.
  - Use echo $VAR to print a variable’s value.

## Important System Variables (quick table)
| Variable | Meaning / stored value | Example command |
|---|---:|---|
| BASH | Absolute path to the current bash shell invoked | echo $BASH |
| BASH_VERSION | Version of the bash shell | echo $BASH_VERSION |
| BASHPID | Process ID (PID) of current bash process | echo $BASHPID |
| HOME | User’s home directory path | echo $HOME |
| PATH | Colon-separated list of directories to search for commands | echo $PATH |
| PWD | Present working directory | echo $PWD |

## Important Properties / Invariants
- System variables are defined in capital letters (convention).
- The shell relies on environment variables to function correctly.
- A variable holds one value at a time (value can change).
- To access a variable’s value you must prefix its name with $ (e.g., $HOME).
- env shows the environment variable list maintained by the system/shell.

## Quick Reference (scannable)
- List env vars: env
- Print var: echo $VARNAME
- Access syntax: $VARNAME
- Naming: SYSTEM variables => ALL_CAPS
- Types: #systemvariable (OS/shell) vs #uservariable (user-created)
- Common vars: $BASH, $BASH_VERSION, $BASHPID, $HOME, $PATH, $PWD

(Use this sheet to quickly locate commands and meanings during an open-book exam.)