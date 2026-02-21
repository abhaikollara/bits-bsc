# Bash conditionals cheatsheet
#hashtags: #Bash #shell #if #else #fi #elif #conditionals #comparison #arithmetic #modulus #expr #arithmetic-expansion #exit-status

---

## Title
Bash if / if-elif-else / fi — syntax & usage

---

## Key Definitions (one-line)
- if statement: branch that executes a "true" block when CONDITION is true.
- else: block executed when if-condition is false.
- elif: "else if" — additional condition checked if previous were false.
- fi: terminator for if/elif/else block.
- CONDITION: any test/command whose exit status determines true (0) or false (non‑0).
- exit status: 0 means success/true, non‑0 means false/failure.
- modulus operator (%): returns remainder of integer division.
- expr: external command for arithmetic (older style).
- (( )): arithmetic evaluation/compound expression (preferred for readability).

---

## Syntax (quick snippets)
- Basic if-else
  ```
  if CONDITION; then
    # true block
  else
    # false block
  fi
  ```
- If-elif-else ladder
  ```
  if COND1; then
    CMD1
  elif COND2; then
    CMD2
  else
    CMD_else
  fi
  ```
- Numeric comparison with test/[ ]
  ```
  if [ "$n" -gt 0 ]; then ...
  ```
- Arithmetic expression (recommended)
  ```
  if (( n % 2 == 0 )); then echo "even"; else echo "odd"; fi
  ```

---

## Comparison operators (numeric)
| Operator | Meaning |
|---:|---|
| -eq | equal |
| -ne | not equal |
| -gt | greater than |
| -ge | greater or equal |
| -lt | less than |
| -le | less or equal |

(When using (( )) you can use standard C-style operators: ==, !=, >, >=, <, <=, %, etc.)

---

## Formulas / Mappings
- CONDITION true  -> exit status 0
- CONDITION false -> exit status != 0 (commonly 1)
- Even/odd check: n % 2 == 0 => even; otherwise odd
- Using arithmetic:
  - (( expr )) returns exit 0 if expr evaluates non-zero; in tests use comparisons for boolean

---

## Key Algorithms / Concepts (bulleted)
- #if: single decision between two blocks (#true-block, #false-block)
- #elif ladder: chain multiple mutually exclusive checks; first true branch executed
- #else: fallback executed only if all prior conditions false
- #(( )) arithmetic expansion: preferred for integer math and readability vs #expr
- #expr: older arithmetic tool — often replaced by (( )) or $(( ))
- Exit-status-driven control: any command/test can be CONDITION (not just comparisons)

---

## Important Properties / Invariants
- fi is required to close an if block.
- Only the first true branch in an if/elif chain executes; remaining branches skipped.
- else is optional.
- For [ ... ] tests, spaces around brackets and operators are required (e.g., [ "$a" -lt 0 ]).
- (( )) treats expression semantics; no extra quoting needed for integers.
- Numeric operators differ between [ ] (use -gt/-lt) and (( )) (use >/<).
- Return/print of exit status: true -> 0, false -> non‑0 (commonly 1).

---

## Quick Reference (scannable)
- Basic pattern: if COND; then ...; else ...; fi
- If-elif: if A; then X; elif B; then Y; else Z; fi
- Even test:
  - if (( n % 2 == 0 )); then echo even; else echo odd; fi
- Positive/negative/zero:
  - if [ "$n" -lt 0 ]; then echo negative
  - elif [ "$n" -gt 0 ]; then echo positive
  - else echo zero; fi
- Common numeric comparisons: -eq, -ne, -gt, -ge, -lt, -le
- Use (( )) for arithmetic: (( n += 1 )), (( n % 2 ))
- Condition truth: command exit status 0 == true
- Debug tip: check $? immediately to inspect last command’s exit code

---

Keep this page for fast lookup of syntax, operators, and common conditional patterns in Bash.