# Linux text tools: wc & grep — Cheatsheet
#hashtags: #wc #grep #linux #commandline #textprocessing #regex #BRE #ERE #pipes #shell

---

## Key Definitions
- wc: count lines, words, and bytes/characters in files or stdin. (#wc)
- grep: search for lines matching a pattern or regular expression in files or streams. (#grep #regex)
- Pattern: string or regular expression passed to grep. (#pattern)
- BRE / ERE: Basic / Extended Regular Expressions used by grep (-E for ERE). (#BRE #ERE)
- Fixed-string: literal string matching (grep -F). (#fixedstring)

---

## Formulas / Syntax (quick)
- wc basic: wc [options] [file...]
  - Default output: <lines> <words> <bytes> <file>
  - Example: `6 18 93 employee.txt` ⇒ 6 lines, 18 words, 93 bytes/characters
  - Flags: -l (lines), -w (words), -c (bytes), -m (characters)
- grep basic: grep [options] PATTERN [file...]
  - With stdin: command | grep PATTERN
  - Recursive: grep -r PATTERN dir/
  - Extended regex: grep -E PATTERN
  - Fixed strings: grep -F PATTERN
- Complexity: O(n) in input size for both tools (scan input once).

---

## Key Algorithms / Concepts
- #wc:
  - wc -l file : count lines
  - wc -w file : count words
  - wc -c file : count bytes
  - wc -m file : count characters (multibyte-aware)
  - Multiple files: prints counts per file + total
  - Use with pipe: somecommand | wc -l  (count lines of output)
- #grep:
  - grep PATTERN file : show lines containing PATTERN
  - grep -i : case-insensitive search
  - grep -r : recursive search through directories
  - grep -v : invert match (show non-matching lines)
  - grep -n : prefix each matching line with its line number
  - grep -l : list file names that contain matches
  - grep -w : match whole words only
  - grep -c : count matching lines per file
  - grep -o : print only matching part(s) of line
  - grep -E / -F : use extended regex / fixed-strings
  - Common use: piped filtering (e.g., ps aux | grep process)

---

## Important Properties / Invariants
- grep is line-oriented: returns whole matching lines (unless -o).
- By default grep matches substrings (use -w to restrict to whole words).
- grep uses basic regex (BRE) by default; -E enables ERE.
- Case sensitive by default (use -i to ignore case).
- Exit codes: 0 = match found, 1 = no match, 2 = error.
- wc default order: lines, words, bytes. Use flags to select specific counts.
- Use -m (characters) vs -c (bytes) when multi-byte characters (UTF-8) matter.

---

## Quick Reference (options)
- wc:
  - -l : lines
  - -w : words
  - -c : bytes
  - -m : characters
- grep:
  - -i : case-insensitive
  - -r / -R : recursive
  - -v : invert match
  - -n : show line numbers
  - -l : list matching file names only
  - -w : match whole words
  - -c : count matching lines
  - -o : output only matched text
  - -E : extended regex (egrep)
  - -F : fixed-string (fgrep)
  - --color=auto : highlight matches

---

## Quick Examples
- wc:
  - `wc file.txt` → prints "<lines> <words> <bytes> file.txt"
  - `wc -l file.txt` → number of lines
  - `ls | wc -l` → number of items in current directory
- grep:
  - `grep "00" employee.txt` → lines containing "00"
  - `grep -n "00" employee.txt` → same + line numbers
  - `grep -i "error" *.log` → case-insensitive across files
  - `grep -r "TODO" src/` → recursive search in src/
  - `grep -v "header" file.txt` → show lines that do NOT contain "header"
  - `grep -o "pattern" file | wc -l` → count total matches (not just lines)

---

## Tips / Pitfalls
- Use -w to avoid substring matches (e.g., "art" matching "start").
- For Unicode characters, -m (chars) differs from -c (bytes).
- grep -r follows directory traversal; use --exclude / --include to filter files.
- Combine tools: grep → cut/awk/sed → wc for more complex pipelines.
- Reference: `man grep` and `man wc` for full option lists and behavior.

---

End of cheatsheet — keep this nearby during exams for quick lookup.