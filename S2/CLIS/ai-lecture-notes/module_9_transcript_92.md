# Shell Scripting Cheatsheet (Decision making, loops, arrays, I/O)
#hashtags: #shell #bash #scripting #if #elif #else #case #for #while #until #break #continue #arrays #string #test #comparison #redirection #fileio #slicing #patternmatching

---

## Key Definitions (one-liners)
- test / [ ] / [[ ]] — evaluate a condition (returns exit status 0 = true).  
- if / then / fi — single-decision block; ends with fi.  
- elif — else-if ladder (multiple mutually exclusive checks).  
- else — default branch for if / elif ladder.  
- case / esac — multi-pattern branch (like switch); patterns end with `;;`.  
- for in — iterate over a list or array elements.  
- C-style for — numeric loop form: arithmetic init/cond/inc.  
- while / until — looping constructs (until runs while condition is false).  
- break — exit the innermost loop.  
- continue — skip rest of current iteration and continue loop.  
- array — ordered collection of elements of same type in bash (declare -a).  
- redirection — `< file` (input), `>` (overwrite output), `>>` (append).  
- read — read a line from stdin (use `read -r` to avoid backslash escapes).  
- expr / $(( )) — arithmetic evaluation; prefer `$(( ))`.  
- pattern `|` in case — acts as OR between patterns; `*)` is default.

---

## Syntax & Quick Examples
- Variables: use `$var` to access; assignment: `var=value` (no spaces).
- if:
  - Single-line: `if [ condition ]; then command; fi`
  - Multi-branch:
    ```
    if [ cond1 ]; then
      ...
    elif [ cond2 ]; then
      ...
    else
      ...
    fi
    ```
  - Use `[[ ... ]]` when variables may contain spaces or for extended tests.
- case:
  ```
  case $var in
    pattern1) commands ;;
    pattern2|pattern3) commands ;;
    *) default ;;
  esac
  ```
- for-in:
  ```
  for item in a b c; do
    echo "$item"
  done
  ```
- C-style for:
  ```
  for ((i=1; i<=5; i++)); do
    echo $i
  done
  ```
- while / until:
  ```
  while read line; do
    ...
  done < file         # input redirection

  until [ condition ]; do
    ...
  done
  ```

---

## Comparison Operators (quick table)
- Integer comparisons (use with test/[ ] / [[ ]]):
  - -eq (==), -ne (!=), -gt, -ge, -lt, -le
- String comparisons:
  - `=` or `==` (in `[[ ]]`) — equal  
  - `!=` — not equal  
  - -z str — true if length is zero  
  - -n str — true if length is non-zero
- Boolean/exit status: test returns 0 for true, non-zero for false.
- Important: always include spaces around [ and ]: `[ "$a" -gt 10 ]`

---

## Arrays (bash)
- Declare: `declare -a arr` or `arr=(Java Python PHP)`
- Access:
  - All elements: `${arr[@]}` or `${arr[*]}`
  - Index: `${arr[2]}` (0-based)
  - Length (#elements): `${#arr[@]}`
  - String length of element: `${#arr[index]}`
- Append:
  - Single: `arr+=(JavaScript)`
  - Multiple: `arr+=("CSS" "SQL")`
- Insert by index: `arr[3]="JavaScript"`
- Delete:
  - Element: `unset 'arr[2]'`
  - Entire array: `unset arr`
- Slicing:
  - `${arr[@]:start:length}` e.g. `${arr[@]:1:3}`
  - Negative start counts from end (example: `${arr[@]: -3}` gives last 3 elements; note the space before negative offset in some shells)

---

## I/O & File Processing
- Input redirection to loop: `while read -r line; do ...; done < input.txt`
- Output redirection:
  - Overwrite: `cmd > file`
  - Append: `cmd >> file`
- Example: print even numbers from file:
  ```
  while read -r n; do
    if (( n % 2 == 0 )); then echo "$n"; fi
  done < integers.txt
  ```
- Prefer `$(( ))` for arithmetic: `(( i % 2 == 0 ))` or `res=$((i * i))`

---

## Break vs Continue (semantics)
- break — immediately exit the current loop (for/while/until).
- continue — skip remaining commands in current iteration and proceed to next iteration.

---

## Common Pitfalls / Important Properties
- Use spaces around brackets: `[ "$x" = "" ]` (missing spaces -> syntax error).
- `[ ... ]` vs `[[ ... ]]`:
  - `[[ ]]` is safer: supports pattern matching, `==` with glob, and avoids word-splitting for variables with spaces.
  - Use `[[ ]]` when variables may contain spaces or for advanced tests.
- Test return values: 0 = true, non-zero = false.
- In `if [ ... ]; then` you must place `;` or newline before `then`.
- In `case` patterns, separate alternatives with `|` and terminate commands with `;;`.
- When slicing negative offsets, some expansions require a space before the negative number: `${arr[@]: -3}`.
- Use `read -r` to avoid interpretation of backslashes.
- Prefer `$(( ))` over `expr` for clarity and reliability.

---

## Quick Reference (one-line cheats)
- Check integer: `[ "$a" -gt 10 ]`
- Check string empty: `[ -z "$s" ]`
- Check string non-empty: `[ -n "$s" ]`
- String equal: `[[ "$a" == "$b" ]]`
- If template: `if [[ cond ]]; then ... fi`
- Case template: `case $v in pat) ... ;; *) ... ;; esac`
- For-in: `for x in "${arr[@]}"; do ...; done`
- C-for: `for ((i=0;i<n;i++)); do ...; done`
- While-file: `while read -r line; do ...; done < file`
- Append to array: `arr+=(new)`
- Array all items: `${arr[@]}` ; length: `${#arr[@]}`
- Overwrite file: `> file` ; Append: `>> file`

---

Keep this sheet handy for syntax lookups in the exam — practice writing small scripts to internalize semicolons, `fi`/`done`/`esac` endings, and correct bracket spacing.