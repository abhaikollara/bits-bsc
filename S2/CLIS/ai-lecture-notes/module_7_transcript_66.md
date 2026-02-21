# grep Cheatsheet — Search & Filter Text in Linux
#grep #linux #regex #regular_expressions #search #filter #log_analysis #text_processing #recursive #case_insensitive #invert_match #count #line_numbers #list_files #stdin

---

## Title
grep — powerful text search/filter tool for files and input streams

---

## Key Definitions
- grep: command-line tool to locate lines matching a pattern in files or input streams.  
- Pattern (PATTERN): the text or regular expression grep matches.  
- Regular expressions (#regex): patterns describing sets of strings; grep supports them.  
- Input stream (#stdin): data piped into grep (e.g., cat file | grep PATTERN).  
- Match: a line that contains text conforming to PATTERN.

---

## Syntax / Quick Pattern
- Basic syntax: grep [options] PATTERN [FILE...]
- Use quoted PATTERN to protect shell meta-characters: grep 'pattern' file

---

## Options Summary (quick reference)
| Option | Effect |
|---|---|
| -i | Case-insensitive search (#case_insensitive) |
| -r | Recursive search in directories (#recursive) |
| -l | List file names that contain the pattern (#list_files) |
| -v | Invert match — show non-matching lines (#invert_match) |
| -c | Count matching lines per file (#count) |
| -n | Show line numbers with matching lines (#line_numbers) |

(Flags may be combined, e.g., grep -rin 'TODO' /path)

---

## Key Algorithms / Concepts
- Pattern matching using regular expressions (#regex)
- Line-based search: grep processes input line-by-line and prints matching lines
- Recursive directory traversal: grep -r descends into subdirectories and searches files
- Filtering in pipelines: grep reads from stdin if FILE omitted (e.g., ps aux | grep ssh) (#stdin)
- Inverted selection: exclude lines matching a pattern with -v

---

## Important Properties / Invariants
- grep prints whole matching lines (unless combined with other tools/options).  
- -i affects only case-sensitivity, not pattern semantics.  
- -r searches files under a directory path (including subdirectories).  
- -l lists only file names (no matching lines) when pattern found.  
- -c reports counts, not content; when multiple files are searched, output shows counts per file.  
- -v returns lines that do NOT match the pattern (useful to exclude entries).  
- grep supports standard regex syntax (basic/extended depending on flags like -E, not covered here).

---

## Quick Reference / Examples
- Search for literal "error" in logfile:
  - grep 'error' logfile.txt
- Case-insensitive search for "warning":
  - grep -i 'warning' logfile.txt
- Recursive search for "config" in directory:
  - grep -r 'config' /path/to/dir
- List file names containing "password":
  - grep -l 'password' /path/to/dir/*
- Count matches of "failed" in file:
  - grep -c 'failed' logfile.txt
- Show matching lines with line numbers:
  - grep -n 'pattern' file.txt
- Invert match (show lines without "success"):
  - grep -v 'success' log.txt
- Combined flags example (recursive, case-insensitive, show line numbers):
  - grep -rin 'TODO' /project

---

## Quick Patterns / Tips
- Use quotes around PATTERN to avoid shell expansion.  
- Omit FILE to read from stdin (useful in pipes).  
- Combine with other tools (sed/awk/xargs) for extraction or batch operations.  
- For extended regex, use grep -E (not detailed in transcript).  

---

Keep this sheet handy for log analysis, filtering outputs, and quick text searches.