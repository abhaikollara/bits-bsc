# expr (Shell) — Quick Cheatsheet

Keywords: #expr #shell #bash #commandline #arithmetic #string #relational #variables #escaping #quoting #length #index #substr #operators

## Key Definitions
- expr: POSIX utility to evaluate integer or string expressions and print the result to stdout. #expr
- Arithmetic expression: uses +, -, \*, /, % between operands (requires spaces). #arithmetic #operators
- Relational expression: compares values; returns 1 if true, 0 if false. #relational
- String operations: built-in keywords `length`, `index`, `substr` for string queries. #string #length #index #substr
- Variable assignment (shell): use no spaces around `=` (e.g., A=10). #variables

## Syntax / Important Rules (short)
- Always put spaces around operators in expr: expr 10 + 20
- Quote or escape the whole expression when it contains shell-special characters: expr "A \* B" or expr A \* B
- Escape `<` and `>` (they are redirection operators): expr 5 \< 3
- Use a single `=` for string/number compare (with spaces): expr a = b
- expr uses 1-based indexing for strings (index/ substr). #1based

## Formulas / Examples
- Arithmetic:
  - expr 10 + 20 -> 30
  - expr 20 - 5  -> 15
  - expr 4 \* 3  -> 12  (escape `*`) 
  - expr 10 / 3  -> 3   (integer division)
  - expr 10 % 3  -> 1
- Relational (returns 1 if true, 0 if false):
  - expr 5 \< 3   -> 0  (escape `<`)
  - expr 5 \> 3   -> 1  (escape `>`)
  - expr 5 = 5    -> 1
- Strings:
  - expr length "hello"    -> 5
  - expr index "hello" e   -> 2   (first position of 'e'; 0 if not found)
  - expr substr "hello" 2 3 -> ell  (substr STRING POS LEN; POS is 1-based)

## Key Algorithms / Concepts (bullet)
- #ArithmeticOperations: +, -, \*, /, % — integer-only, integer division truncates.
- #RelationalOps: <, >, = — must be escaped (<, >) and spaced; return 1/0.
- #StringOps:
  - length STRING -> integer length
  - index STRING CHARS -> position of first occurrence of any char in CHARS (0 if none)
  - substr STRING POS LEN -> substring from POS (1-based) of length LEN
- #QuotingEscaping: Quote entire expr or escape special symbols to prevent shell interpretation.
- #VariableRules: assignment with no spaces (A=10); when using variables in expr, expand them: expr "$A" + "$B" or expr $A + $B

## Important Properties / Invariants
- Spaces are mandatory around expr operators; without them, expr treats token as a string.
- Relational results are numeric (1 = true, 0 = false), not boolean words.
- expr outputs plain text to stdout; capture with command substitution: result=$(expr 1 + 2)
- `*`, `<`, `>` must be escaped or quoted to avoid shell globbing/redirects.
- Indexing for strings is 1-based; index returns 0 for not-found.

## Quick Reference (scannable)
- Arithmetic operators: + - \* / %  — remember to escape `*`
- Relational: \< \> =  — returns 1 or 0
- String keywords: length, index, substr
- Common examples:
  - expr 10 + 20        -> 30
  - expr "10+20"        -> 10+20 (no spaces => string)
  - expr A=10           -> (invalid inside expr; use shell assignment `A=10`)
  - A=10; B=20; expr $A + $B -> 30
  - expr length "hi"    -> 2
  - expr index "abc" d  -> 0
  - expr substr "hello" 2 3 -> ell
- Pitfalls:
  - Forgetting spaces: expr 10+20 outputs "10+20"
  - Not escaping `*` or `<`/`>` leads to unintended shell behavior
  - Using `==` or `-eq` inside expr: use single `=` (expr syntax differs from [ ] tests)

Keep this sheet handy for quick lookup of expr syntax, operators, and common gotchas.