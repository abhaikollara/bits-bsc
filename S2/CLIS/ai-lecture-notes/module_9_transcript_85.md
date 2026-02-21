# Bash String Operations in if Statements — Cheatsheet
#bash #strings #if #test #[] #test-command #string-comparison #-n #-z #equality #inequality #exit-status #quoting #read

## Key Definitions
- test / [ ]: POSIX command/alias used to evaluate conditions in if statements.  
- if statement: executes commands based on test command exit status.  
- -n: returns true if string is non-empty.  
- -z: returns true if string is empty (inverse of -n).  
- "=": string equality operator in test / [ ].  
- "!=": string inequality operator.  
- Exit status: 0 = true (condition met), non‑zero = false.

## Formulas / Notation
- exit status: true ⇨ 0, false ⇨ 1 (or any non‑zero)  
- Common pattern: if [ condition ]; then ...; fi

## Key Concepts / Operations
- #StringEquality: [ "$a" = "$b" ] → true if strings are equal (returns 0).  
- #StringInequality: [ "$a" != "$b" ] → true if strings differ.  
- #NonEmptyCheck: [ -n "$s" ] → true if s is not empty.  
- #EmptyCheck: [ -z "$s" ] → true if s is empty.  
- #ReadInput: read var to get user input, then test the variable in if.  
- #IfElse: use if ... then ... else ... fi to branch on string tests.

## Important Properties / Invariants
- #Spacing: In [ ... ] ensure spaces around brackets and tokens: [ "$a" = "$b" ] (NOT ["$a"="$b"]).  
- #Quoting: Always quote variables: "$var" to avoid word-splitting and errors when empty.  
- #POSIX vs Bash: [ ] is POSIX-compatible; use "=" for equality. [[ ]] (bash) permits == and pattern matching.  
- #ReturnValues: test returns 0 for true conditions — if interprets 0 as success/true.

## Quick Reference (scannable)
| Test expression | Meaning | Example |
|---|---:|---|
| [ -n "$s" ] | string non-empty | if [ -n "$s" ]; then echo "non-empty"; fi |
| [ -z "$s" ] | string empty | if [ -z "$s" ]; then echo "empty"; fi |
| [ "$a" = "$b" ] | strings equal | if [ "$a" = "$b" ]; then echo "same"; fi |
| [ "$a" != "$b" ] | strings not equal | if [ "$a" != "$b" ]; then echo "different"; fi |

Quick patterns:
- Read + check non-empty:
  - read s
  - if [ -n "$s" ]; then echo "true"; else echo "false"; fi
- Read two strings + compare:
  - read a b
  - if [ "$a" = "$b" ]; then echo "strings are same"; else echo "strings are different"; fi

## Exam Tips (one-liners)
- Always put spaces inside [ ] and quote variables. #Spacing #Quoting  
- Remember: test returns 0 for true — if checks for success. #exit-status  
- Use "=" with [ ]; use "==" only in [[ ]] when doing pattern matches. #POSIX

--- 
Hashtags included above for quick searching: #bash #strings #test #if #-n #-z #equality #inequality #quoting #exit-status