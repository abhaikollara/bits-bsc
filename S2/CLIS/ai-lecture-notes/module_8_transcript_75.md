# Shell Special Variables — Quick Reference
#keywords: #shell #bash #special-variables #positional-parameters #script #arguments #pid #exit-status #$0 #$1 #$$ #$# #$* #$@ #$?

## Key Definitions
- Special variable: a variable with predefined meaning in the shell/scripting environment.  
- Positional parameter: argument passed to a script, referenced by an integer index (e.g., $1).  
- Script name ($0): the name/path of the running script.  
- Argument count ($#): total number of positional parameters.  
- All arguments ($* / $@): the list of all positional parameters.  
- Process ID ($$): PID of the current shell/process.  
- Exit status ($?): exit code of the last executed command (0 = success).

## Formulas / Notation
- $# = number of arguments (integer ≥ 0)  
- $n = nth argument (n is positive integer)  
- $0 = script name (may be path or basename)  
- $$ = PID of current shell/process  
- $? = exit status (0 → success; nonzero → error)  
- Use braces for multi-digit positional indexes: ${10}, ${11}, ...

## Key Variables / Concepts
- $0 — script filename or command used to invoke the script. (#$0)  
- $1, $2, ... $n — positional parameters (first, second, …). (#$1)  
- $# — number of positional parameters. (#$#)  
- $* — all positional parameters as a single word (unquoted) or single string when quoted. (#$*)  
- $@ — all positional parameters but preserves separation when quoted ("$@"). (#$@)  
- $$ — process ID of the current shell. (#$$)  
- $? — exit status of the most recently executed command. (#$?)  

## Important Properties / Invariants
- $0 may include path or just the name depending on how invoked.  
- If no arguments: $# = 0; $1, $2, ... are empty/unset.  
- Quoting difference:
  - "$*" expands to all args as one string: "arg1 arg2 arg3".  
  - "$@" expands each arg as separate quoted word: "arg1" "arg2" "arg3".  
- Positional parameters beyond $9 must be referenced with braces: ${10}.  
- $? is set immediately after a command; executing another command (including echo) changes it.  
- $$ is constant within the script (the shell’s PID).  
- Exit status convention: 0 = success; nonzero = error (shell builtin/command-dependent codes).

## Quick Reference (table)
| Variable | Meaning | Typical example |
|---|---:|---|
| $0 | Script/command name | echo "$0" |
| $1 | 1st argument | echo "$1" |
| $2 | 2nd argument | echo "$2" |
| $n | nth argument | echo "${n}" |
| $# | Number of args | if [ $# -lt 1 ]; then ... fi |
| $* | All args (single word if quoted) | echo "$*" → "a b c" |
| $@ | All args (preserve boundaries when quoted) | for x in "$@"; do ...; done |
| $$ | PID of current shell | echo $$ |
| $? | Exit status of last command | cmd; echo $? |

## Quick Tips
- Use "$@" for safe iteration over args (preserves spaces). (#$@)  
- Check exit with if [ $? -ne 0 ]; then ... fi — but prefer conditional constructs directly (if cmd; then ...). (#$?)  
- Use ${N} when N >= 10 (avoid ambiguity).  
- $# is useful for validating required args.

(End of cheatsheet)