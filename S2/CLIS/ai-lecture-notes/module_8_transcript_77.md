# User-defined Variables in Bash — Cheatsheet
#bash #shell #variables #user-defined #naming-rules #assignment #case-sensitive #null-variable #system-variables #regex #naming-conventions

## Key Definitions
- User-defined variable: A name/value pair created by the programmer in a shell script.
- System variable: Environment or shell-provided variables (commonly ALL_CAPS).
- Assignment: The syntax that gives a value to a variable (no spaces around =).
- Null variable: A variable defined with no value (empty string).
- Variable reference: Using a variable’s value (typically with $VAR).

## Formulas / Syntax / Regex
- Assignment syntax: VAR=value    (NO spaces around '=')
- Empty assignment: VAR=
- Reference: $VAR or "${VAR}"
- Valid-name regex: ^[a-zA-Z_][a-zA-Z0-9_]*$
- Common pattern: Start with letter or underscore, followed by letters/digits/underscores

## Key Concepts / Rules
- Naming rules:
  - Must start with a letter (A–Z, a–z) or underscore (_).
  - Remaining characters: letters, digits (0–9), or underscore.
  - Cannot start with a digit.
  - Case-sensitive: VAR and var are different.
- Assignment specifics:
  - No spaces around '=' — spaces break assignment (interpreted differently).
  - Use uppercase for conventional system variables; user variables often lowercase or mixed.
- Null variables:
  - Allowed: VAR= creates an empty value.
  - Printing a null var yields no output (empty).
- Avoid using characters with shell meaning:
  - Do not use ?, *, !, -, +, etc. in variable names (they have special shell semantics).

## Important Properties / Invariants
- Invariant: Variable names conform to regex ^[a-zA-Z_][a-zA-Z0-9_]*$.
- Invariant: Assignments require exact VAR=value (no whitespace).
- Invariant: Variables are case-sensitive and distinct by case.
- Convention: System/environment variables are usually ALL_CAPS (not enforced).

## Quick Reference — Examples & Common Pitfalls
- Valid examples:
  - NAME=John
  - _count=0
  - user1=alice
- Invalid examples (and why):
  - 1var=10       — starts with digit
  - my var=val    — contains space (breaks assignment)
  - name?=x       — contains special char (bad practice / error)
- Empty/null:
  - EMPTY=
  - echo "$EMPTY"   -> prints nothing
- Usage:
  - Assign: VAR=value
  - Print: echo $VAR   or   echo "$VAR"
- Remember:
  - No spaces around '='
  - Use $ to access value
  - Case matters: PATH ≠ path

Keep this as a quick checklist during the exam to verify variable naming and assignment correctness.