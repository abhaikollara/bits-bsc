# Bash Logical Operators & File Tests — Cheatsheet
#keywords: #bash #logical-operators #if-statement #AND #OR #NOT #short-circuit #test #file-operators #-e # -f # -d # -x

## Key Definitions (one-line)
- Logical AND (&&): true only if both sub-expressions are true.  
- Logical OR (||): true if at least one sub-expression is true.  
- Logical NOT (!): negates the truth of an expression.  
- Short-circuit evaluation: second operand not evaluated if result determined by first.  
- Test expression brackets: [[ ... ]] indicate a compound/complex condition.  
- File test operators: unary checks that test file/directory properties (e.g., -e, -f, -d, -x).

## Formulas / Syntax (quick)
- Compound tests:
  - if [[ expr1 && expr2 ]]; then ... fi
  - if [[ expr1 || expr2 ]]; then ... fi
  - if [[ ! expr ]]; then ... fi
- Numeric comparisons:
  - a -eq b  (equal), -ne (not equal), -gt (greater), -lt (less), -ge (>=), -le (<=)
- File tests:
  - -e file  (exists)
  - -f file  (regular file)
  - -d file  (directory)
  - -x file  (executable)

## Key Concepts / Examples
- #Logical-AND:
  - Use && (two ampersands) inside [[ ... ]] for combined requirement.
  - Example (two-digit check): [[ $n -gt 9 && $n -lt 100 ]]
- #Logical-OR:
  - Use || (two pipes) inside [[ ... ]] for either/or checks.
  - Example (out-of-range check): [[ $n -lt 10 || $n -gt 99 ]]
- #Logical-NOT:
  - Use ! to invert a condition: [[ ! -e "$file" ]]  (true when file does not exist)
- #Short-circuit:
  - AND: if first expr is false, second is not evaluated.
  - OR: if first expr is true, second is not evaluated.
- #File-tests:
  - Example (exists): if [[ -e "$name" ]]; then echo "exists"; else echo "no"; fi
  - Example (is file): [[ -f "$name" ]]; then ...
  - Example (is directory): [[ -d "$name" ]]; then ...
  - Example (is executable): [[ -x "$name" ]]; then ...

## Important Properties / Invariants
- Complex condition typically enclosed with double square brackets [[ ... ]] (signals compound tests).
- Logical operators inside [[ ... ]] are boolean operators for test expressions.
- Short-circuiting can avoid errors (e.g., skip second test that would fail when first false/true).
- Use numeric test operators (-gt, -lt, etc.) for integers, not > or < without quotes/escaping.
- File tests return true/false; handle both cases to avoid script errors.

## Quick Reference (scannable)
- Logical
  - &&  — AND (both true)
  - ||  — OR  (any true)
  - !   — NOT (invert)
- Numeric compare
  - -eq, -ne, -gt, -lt, -ge, -le
- File tests
  - -e file  — exists
  - -f file  — is regular file
  - -d file  — is directory
  - -x file  — is executable
- Example one-liners
  - Two-digit check: if [[ $n -gt 9 && $n -lt 100 ]]; then echo "valid"; fi
  - Out-of-range check: if [[ $n -lt 10 || $n -gt 99 ]]; then echo "wrong input"; fi
  - File exists: if [[ -e "$file" ]]; then echo "found"; else echo "not found"; fi
- Notes
  - First operand may prevent second from running (short-circuit).
  - Always enclose complex conditions in [[ ... ]] for readability and safety.

#tags: #bash #logical-operators #if-statement #file-tests #-e # -f # -d # -x #short-circuit