# vi/vim Misc Commands — Cheatsheet
# #vi #vim #editor #commands #search #replace #marks #indentation #linenumbers #navigation #join #split #repeat

## Key Definitions
- Normal mode: vi's default mode for navigation/commands (Esc to enter). #normal-mode  
- Insert mode: mode for inserting text (i, a, o to enter). #insert-mode  
- Command-line / Ex mode: enter with : to run commands (e.g., :s, :25). #ex-mode  
- Mark: named position in file set by m{char} and jumped to by ` or '. #marks  
- Pattern search: use /pattern to find next match. #search  
- Substitute: :s (ex command) to replace text; supports flags g, c, % etc. #substitute

## Formulas / Command Syntax (quick patterns)
- Repeat last edit: .  
- Search: /pattern <Enter>  
- Substitute (current line): :s/old/new/flags  
- Substitute (whole file): :%s/old/new/flags  
  - flags: g = global (all occurrences in line), c = confirm each (use together as gc or cg)  
- Jump to line N: :N (e.g., :25)  
- Set mark: m{a-z} (e.g., ma) — jump: `a (exact pos) or 'a (line)  
- Indent line: >> ; unindent: <<  
- Join lines: J (normal mode) or :join  
- Split line: insert newline at cursor (use i<Enter> or a<Enter>) — (transcript said 's', correct is inserting newline).  
- Toggle line numbers: :set number / :set nonumber

## Key Commands / Concepts
- #repeat
  - .  — repeat last change (works in normal mode).  
- #search
  - /pattern <Enter> — search forward for pattern. Use n (next) / N (prev) after.  
- #replace / #substitute
  - :s/old/new/g  — replace all occurrences on current line.  
  - :%s/old/new/g — replace all occurrences in file.  
  - :%s/old/new/gc — replace all in file with confirmation for each.  
- #marks
  - ma  — set mark 'a' at cursor.  
  - `a  — jump to exact cursor position at mark a.  
  - 'a  — jump to start of the line of mark a.  
- #navigation
  - :N  — go to line N (e.g., :25).  
  - :set number / :set nonumber — enable/disable line numbers.  
- #indentation
  - >>  — indent current line (can use a count, e.g., 3>>).  
  - <<  — unindent current line.  
- #join / #split
  - J  — join current line with next line.  
  - :join  — join lines (ex command).  
  - i<Enter> or a<Enter> — split line at cursor by inserting newline.  
- #misc
  - s  — delete character under cursor and enter insert (not "split line"). Use with caution.

## Important Properties / Invariants
- Commands in normal mode act immediately; many ex commands require leading colon (:). #normal-mode #ex-mode  
- :s without % affects only the current line; use range or % for more lines. #substitute  
- Flags order doesn't matter (e.g., /gc or /cg both valid). #substitute  
- Marks are single-character and local to the file (lowercase a–z). #marks  
- Indentation commands accept counts (e.g., 2>> indents two times). #indentation

## Quick Reference (scannable)
- Repeat last edit: .  
- Search forward: /pattern <Enter> ; next/prev: n / N  
- Replace (current line): :s/old/new/g  
- Replace (whole file): :%s/old/new/g ; confirm: :%s/old/new/gc  
- Go to line 25: :25  
- Toggle line numbers: :set number / :set nonumber  
- Set mark a: ma — jump: `a or 'a  
- Indent line: >>  — Unindent: <<  
- Split line at cursor: i<Enter> or a<Enter>  
- Join lines: J (normal) or :join  
- Delete char + insert: s (use carefully)  

Tags for quick search: #repeat #search #replace #substitute #marks #jump-to-line #indentation #line-numbers #join #split #dot-command

(Notes: cleaned up minor inaccuracies from transcript — primary substitute patterns and split/join commands shown as commonly used in vi/vim.)