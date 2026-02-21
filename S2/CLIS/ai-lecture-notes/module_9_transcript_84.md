# Case Statement (Linux shell) — Cheatsheet
#hashtags: #case #shell #bash #if-elif #multilevel-if #patternmatching #default #string #integer #switch

---

## Key Definitions
- case statement: branching construct that selects a block based on a single expression's value.  
- if-elif ladder (multilevel-if): series of if/elif/else checks; alternative to case.  
- pattern: value or glob used to match the expression in a case branch.  
- default (star): `*` pattern that matches when no other pattern does.

---

## Syntax (quick template)
- General:
  ```
  case <expression> in
    pattern1) commands ;; 
    pattern2|pattern3) commands ;;
    *) default-commands ;;
  esac
  ```
- Notes:
  - Use `|` to separate multiple patterns for one branch.
  - Terminate each branch with `;;`.
  - End the construct with `esac`.

---

## Formulas / Notation
- First-match wins: evaluation stops when a matching pattern is found.
- Expression types: #integer or #string (case works for both).
- Efficiency: case is generally more efficient than repeated #if-elif when all branches depend on the same variable.

---

## Key Concepts / Usage
- Use #case when all branches depend on the value of a single variable.
- Use `*` as the default branch (fallback) when no patterns match.
- Patterns support shell-style globbing (basic wildcards) — useful for matching ranges/sets of values.
- Branch grouping: `patternA|patternB)` executes the same commands for multiple matches.
- Input examples from lecture:
  - Numeric option example: `3` → prints "information technology".
  - Unknown numeric `4` or `5` → falls to `*` and prints "other branch".
  - String example: input `"CSE"` → matches and prints "computer science and engineering".
  - Unknown string `"PHY"` → falls to `*` and prints "other branch".

---

## Important Properties / Invariants
- Single-expression dispatch: case examines one expression and compares against patterns.
- Order matters: put more specific patterns before more general ones.
- Deterministic: the first matching pattern determines the executed block.
- Can match both strings and numbers (both treated as text for matching).
- Cleaner and often more efficient than multiple `if/elif` blocks when branching on one value.

---

## Quick Reference (scannable)
- Start: `case <expr> in` — End: `esac`
- Branch end: `;;`
- Multiple patterns: `a|b|c)`
- Default/fallback: `*)`
- When to use:
  - Use #case if: many branches, all depend on same variable.
  - Use #if-elif if: branches have different conditions not tied to a single value.
- Behavior:
  - Checks patterns sequentially → first match executed → then exits case.
  - If no match → `*` executes (if present); otherwise no branch runs.
- Inputs:
  - Works for both numeric and text inputs (treated as strings for matching).

---

Keep this sheet next to your exam questions as a quick lookup for #case syntax, patterns, and when to prefer it over #if-elif.