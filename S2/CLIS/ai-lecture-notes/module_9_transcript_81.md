# Bash test / [ ] Cheatsheet
#hashtags: #bash #shell #test #brackets #conditionals #if #comparison #integeroperators #stringoperators #fileoperators #exitstatus #read #modulus

---

## Title
Bash "test" Command and Square-Bracket [ ] Expressions — Quick Reference

---

## Key Definitions (one-line)
- test: builtin that evaluates a command, expression, or file test; returns exit status 0 (true) or 1 (false).  
- [ ... ]: POSIX synonym/alias for test (must have surrounding spaces and closing ]).  
- exit status ($?): numeric status of last command; 0 = true/success, non‑0 = false/failure.  
- integer comparison operators: operators used to compare numeric values inside test/[ ].  
- file test: test of filesystem properties (regular file, directory, executable, etc.).  
- modulus (%): arithmetic remainder operator (used via arithmetic expansion $((...)) or ((...))).  
- read: builtin to read user input into a variable.

---

## Syntax / Forms
- test expression
- [ expression ]    (must have spaces: [ x -eq y ] )
- if test ...; then ... fi
- if [ ... ]; then ... fi
- Use $? to check last command exit status.

Examples:
- test 10 -gt 5
- [ "$num" -eq 0 ]
- if [ "$n" -eq 0 ]; then echo "zero"; fi

---

## Formulas / Notations
- test true -> exit code 0  
- test false -> exit code 1  
- check status: echo $?  (0 means true)  
- arithmetic expansion: $(( expression ))  
- modulus example: remainder=$(( n % 2 ))

---

## Key Operators (Quick Tables)

Integer comparisons (use inside test/[ ])
- -eq : equal
- -ne : not equal
- -gt : greater than
- -lt : less than
- -ge : greater or equal
- -le : less or equal

String tests
- =   : string equality (in test/[ ])
- !=  : string inequality
- -z  : string length is zero
- -n  : string length is non-zero

File tests (common)
- -e : file exists
- -f : file exists and is regular file
- -d : file exists and is directory
- -x : file is executable
- -r : readable
- -w : writable
- -s : size > 0 (non-empty)

Logical / other
- !   : logical NOT (negation)
- -a  : logical AND (supported but can be ambiguous)
- -o  : logical OR  (supported but can be ambiguous)
- Prefer separate tests combined with && and || in shell scripts for clarity.

---

## Key Algorithms / Concepts (bulleted)
- #input-checking: Use read to get user input; perform numeric comparison with test/[ ].
- #parity-check: Compute remainder and compare to 0 for even/odd:
  - remainder=$(( n % 2 )); [ "$remainder" -eq 0 ]
  - or: if (( n % 2 == 0 )); then ... (arithmetic context)
- #control-flow: Use test/[ ] inside if statements to drive conditional behavior.
- #file-validation: Use file test operators (e.g., -f, -x) to check file type/permissions before operations.
- #exit-status: Use $? immediately after a command to inspect success/failure.

---

## Important Properties / Invariants
- Spaces matter: [ and ] must be separated by spaces from the expression.
- Quote variables: use "$var" inside test to avoid word-splitting and empty-string errors.
- test/[ ] return 0 on true, 1 on false (check with $?).  
- Use $((...)) or ((...)) for arithmetic; test only does string-tokenized comparisons.
- File tests test filesystem metadata, not contents (except -s for non-empty).

---

## Quick Reference (scannable)

Usage examples:
- Numeric compare: [ "$a" -gt "$b" ]
- Equality: [ "$s1" = "$s2" ]
- Not equal: [ "$s" != "" ]  or [ -n "$s" ]
- Null/empty: [ -z "$s" ]
- File exists: [ -e "/path" ]
- Regular file: [ -f "/path" ]
- Directory: [ -d "/path" ]
- Executable: [ -x "/path" ]
- Non-empty file: [ -s "/path" ]

Parity example:
- read -p "Enter n: " n
- if [ $((n % 2)) -eq 0 ]; then echo "even"; else echo "odd"; fi

Check last command:
- some_cmd
- echo $?   # 0 = success/true

Best practices (short):
- Always quote variables inside [ ]. Example: [ "$var" -eq 0 ]
- Ensure spaces around [ and ]
- Prefer arithmetic context (( ... )) for complex numeric expressions
- Use logical && / || between commands for clearer control flow when combining tests

---

End of cheatsheet — concise lookup for using test and [ ] in Bash.