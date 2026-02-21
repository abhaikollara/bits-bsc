# Bash For-Loop Cheatsheet
#hashtags: #bash #shell #forloop #for-in #c-style #loops #range #braceexpansion #variables #syntax #increment #decrement

---

## Key Definitions
- for loop: A construct to repeat commands over a list or range.  
- for-in loop: Iterates over a specified list of values (space-separated).  
- C-style for loop: Three-part loop (initializer; condition; step) similar to C.  
- list: Sequence of items separated by spaces used by for-in.  
- brace expansion / range: `{start..end}` (optionally `{start..end..step}`) producing a list of values.  
- initializer: Expression run once before loop (C-style).  
- condition / loop test: Boolean check evaluated each iteration (C-style).  
- accounting expression / step: Update run after each iteration (C-style).

---

## Syntax / Formulas
- For-in style:
  - Syntax: for <var> in <list>; do <commands>; done
  - Example: for item in one two three; do echo $item; done
- For-in range (brace expansion):
  - `{start..end}` -> sequence from start to end
  - `{start..end..step}` -> sequence with increment/decrement (step can be negative)
  - Examples: `{1..10}`, `{1..10..2}`, `{10..1..-1}`
- C-style for:
  - Syntax: for (( init; condition; step )); do <commands>; done
  - Example: for (( i=1; i<=10; i++ )); do echo $i; done
- Keywords: for, in, do, done

---

## Key Algorithms / Concepts
- Iteration over explicit lists: for x in a b c; do ...
- Iteration over variable words: for w in $var; do ...  (each space-separated word)
- Iteration over numeric ranges via brace expansion: for n in {start..end[..step]}; do ...
- C-style numeric iteration for fine-grained control: for (( init; cond; step )); do ...

---

## Important Properties / Invariants
- #for-in:
  - Items are separated by spaces (word-splitting defines items).
  - List items can be integers, characters, strings, mixed types.
  - Can iterate over words from a variable (word-splitting applies).
  - Brace expansion produces a literal list before loop execution.
- #c-style:
  - Uses round parentheses with three expressions separated by semicolons.
  - Initializer runs once; condition checked each iteration; step runs after each iteration.
  - Syntax and operators resemble C (e.g., i++, i+=2).

---

## Quick Reference (scannable)
- Basic for-in:
  - for x in a b c; do cmd "$x"; done
- From variable words:
  - line="learn bash loops"
  - for word in $line; do echo "$word"; done
- Range (ascending):
  - for i in {1..10}; do echo $i; done
- Range with step:
  - for i in {1..10..2}; do echo $i; done
- Range descending:
  - for i in {10..1..-1}; do echo $i; done
- C-style numeric:
  - for (( i=1; i<=10; i++ )); do echo $i; done
- Keywords reminder:
  - for / in / do / done

---

Keep this sheet handy for syntax lookups and quick examples during an open-book exam.