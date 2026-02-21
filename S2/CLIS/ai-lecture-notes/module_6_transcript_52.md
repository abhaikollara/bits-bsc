# Searching & Substitution in vi Editor — Cheatsheet

Keywords: #vi #vim #search #substitute #regex #regular-expressions #case-insensitive #case-sensitive #commands #normal-mode #command-mode

## Key Definitions
- Normal mode: vi mode for navigation and searching (press Esc to ensure).
- Command-line mode: invoked with ":" for commands like substitution.
- Search mode: initiated with "/" to type a search pattern.
- Pattern: a regular expression used to match text.
- Substitute command: :s (line) or :%s (whole file) to replace text.
- Flag: option after substitute (e.g., g, c) that modifies behavior.

## Common Commands (one-line)
- /pattern → start forward search for pattern (press Enter to run).
- n → go to next occurrence (forward).
- N → go to previous occurrence (backward).
- : → enter command-line mode.
- :s/old/new/ → replace first occurrence on current line.
- :s/old/new/g → replace all occurrences on current line.
- :%s/old/new/g → replace all occurrences in whole file.
- :%s/old/new/gc → replace all in file, confirm each change interactively.

## Regex Tokens / Notation (vi/vim)
- . → any single character (#regex)
- * → zero or more of previous atom (#regex)
- ^ → start of line (#regex)
- $ → end of line (#regex)
- \d → digit (in vim “magic” mode; works in many vim regexes) (#regex #digits)
- + → one or more (in basic vi/vim regex must escape: \+ ) — alternative: use very-magic mode \v and then +
- Note: vi/vim uses slightly different escaping rules; \+ is common for "one or more".

Examples:
- /^start → match lines beginning with "start"
- /end$ → match lines ending with "end"
- :%s/\d\+/NUMBER/g → replace digit sequences with NUMBER (use \d\+ or adjust regex magic)

## Case Sensitivity Modifiers
- /\cpattern → case-insensitive search (forces ignore case) (#case-insensitive)
- /\Cpattern → case-sensitive search (forces case-sensitive) (#case-sensitive)
- These modifiers are placed inside the search pattern.

## Important Properties / Invariants
- Searches are started from Normal mode using "/".
- n moves forward; N moves backward relative to the original search direction.
- :s operates on current line by default; prefix with range (e.g., % for whole file) to change scope.
- g flag on substitute = all matches in the addressed range/line; without g only first match per line is replaced.
- gc flags = global + confirm each replacement interactively.
- Regular expressions can be used in search and substitute; be cautious with metacharacters and escaping.
- Always preview or confirm large substitutions to avoid unintended replacements.

## Quick Reference (scannable)
- Open file: vi filename
- Start search: /pattern  (Enter)
- Next / previous match: n / N
- Case-insensitive search: /\cterm
- Case-sensitive search: /\Cterm
- Replace first on line: :s/old/new/
- Replace all on line: :s/old/new/g
- Replace whole file: :%s/old/new/g
- Replace whole file with confirm: :%s/old/new/gc
- Replace digits with word NUMBER: :%s/\d\+/NUMBER/g
- Common meta-chars: . * ^ $ \d \+
- Caution: use g flag carefully — can produce unintended global changes.

Hashtags (major concepts & commands): #vi #vim #search #substitute #regex #regular-expressions #case-insensitive #case-sensitive #normal-mode #command-mode #n #N #s #%s #gc #g

Note: vi/vim flavor differences exist for regex escaping (e.g., + often needs escaping as \+). If a pattern doesn't work, try escaping quantifiers or using very-magic mode (\v).