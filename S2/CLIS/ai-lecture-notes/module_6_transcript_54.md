# vi/vim Editor Cheatsheet
#hashtags: #vi #vim #editor #vi-editor #modes #navigation #editing #copy-paste #search #replace #regex #regular-expressions #backup #swapfile #undo #redo #marks #indentation #line-numbers #commands #command-line #grep #crash-recovery

---

## Title
vi/vim Quick Reference — modes, navigation, editing, search/replace, regex basics, backups & recovery

---

## Key Definitions (one-line)
- Normal mode: Default mode for navigation and commands (press Esc to enter). #modes #normal
- Insert mode: Typing mode (enter with i, I, a, A, o, O). #insert
- Command-line mode: Run colon commands (start with `:`). #command-line
- Yank: Copy a line/selection (yy y). #yank #copy #yy
- Paste: Insert yanked/deleted text (p or P). #paste #p
- Delete: Remove text (x=char, dw=word, dd=line). #delete #dd #dw #x
- Swap file (.swp): Hidden auto-save file holding unsaved edits for crash recovery. #swapfile #.swp
- Backup file (.bak / .ba~ / custom): Explicit backup copy when set. #backup
- Mark: Save a cursor position (ma) and return with `\`a or 'a. #marks
- Regex: Pattern syntax used for searches (./^/$/*/+ etc.). #regex #regular-expressions
- Repeat last normal-mode command: `.` (dot). #repeat

---

## Formulas / Notations / Regex symbols
- .  → any single character (dot). #regex
- ^  → start of line. #regex
- $  → end of line. #regex
- *  → zero or more occurrences. #regex
- +  → one or more occurrences. #regex
- [0-9]+  → one or more digits. #regex
- [A-Za-z]+  → one or more letters (upper/lower). #regex
- \c / \C  → case-insensitive / case-sensitive in some contexts (vim search flags). #regex

---

## Key Commands & Concepts
- Modes
  - Enter insert: i, I, a, A, o, O. #i #I #a #A #o #O
  - Return to normal: Esc. #Esc
  - Command-line: `:` then command (e.g., `:w`, `:q`). #:
- File save / quit
  - Save: `:w` (#:w)
  - Quit: `:q` (#:q)
  - Save+Quit: `:wq` or `:x` (#:wq #:x)
  - Quit without saving: `:q!` (#:q!)
- Navigation (normal mode)
  - h (left), j (down), k (up), l (right). #h #j #k #l
  - gg → go to top; G → go to end. #gg #G
  - `$` → end of line, `0` → line start. #$
- Editing basics (normal mode)
  - dd → delete current line. #dd
  - Ndd → delete N lines (prefix with number). #dd
  - yy → yank (copy) line. #yy
  - p → paste after cursor (P to paste before). #p #P
  - x → delete character under cursor. #x
  - dw → delete word from cursor. #dw
  - d$ → delete from cursor to end of line/file (d followed by `$` deletes to line end; dG deletes to file end). #d$
  - r{char} → replace character under cursor with {char}. #r
  - J (capital) → join current line with next. #J
- Undo / Redo
  - u → undo last change. #u
  - Ctrl-r → redo. #Ctrl-r
- Repeating & counts
  - . → repeat last normal-mode command. #.
  - Prefix with number to repeat (e.g., 4>> to indent 4 lines). #counts
- Indentation
  - > (shift-right) and < (shift-left) in normal/visual mode; prefix N to affect N lines (`N>`). #indentation #>
- Marks
  - ma → mark current position as mark 'a'. #ma
  - `a  or 'a → jump back to mark a (backtick vs apostrophe differences: exact pos vs start of line). #`a #'a
- Search & Replace
  - Search forward: `/pattern` then n (next), N (previous). #/ #n #N
  - Replace on current line: `:s/old/new/` (#:s)
  - Replace globally in file: `:%s/old/new/g` (#:%s #g)
  - With confirmation: `:%s/old/new/gc` (ask on each). #:%s #gc
- Command-line options (when launching vi)
  - `vi +N file` → open file and place cursor at line N. #+N
  - `vi -n file` → no swap file (disable .swp). #-n
  - `vi -r file` → recover a swap file (.swp) — use `vi -r filename`. #-r
  - `vi -c "command"` → run ex command after opening (e.g., `-c "w my.bak"`). #-c
  - `vi -i` → can control creation/usage of viminfo (depends on config). #-i
- Swap & Backup behavior
  - On normal editing: vim creates .swp (hidden swap) storing unsaved changes. #.swp
  - On crash: open vim shows recovery option or use `vi -r file` to recover. #-r #recovery
  - To enable explicit backups: `:set backup` and `:set backupdir` or `:set backupext=.ba` / `:set backupcopy` (session-dependent). #backup #set
  - Example backup extension: filename.ba~ or filename.bak depending on settings. #backup
- Misc
  - `:set number` / `:set nonumber` → show/hide line numbers. #:set-number
  - `.` (dot) repeats last normal-mode edit. #.
  - Use visual mode (v, V, Ctrl-v) for block/line/char selections (not covered in transcript but useful). #visual

---

## Quick Reference Table (most-used commands)
| Action | Command (normal or command-line) | Mode |
|---|---:|---|
| Enter insert | i / I / a / A / o / O | normal → insert |
| Save | :w | command-line |
| Quit | :q / :q! / :wq | command-line |
| Move left/down/up/right | h / j / k / l | normal |
| Go to top / end | gg / G | normal |
| Delete line | dd (Ndd for N lines) | normal |
| Yank (copy) line | yy | normal |
| Paste | p / P | normal |
| Delete char | x | normal |
| Delete word | dw | normal |
| Replace char | r{c} | normal |
| Join lines | J | normal |
| Undo / Redo | u / Ctrl-r | normal |
| Repeat last | . | normal |
| Mark / jump | ma  → `a / 'a | normal |
| Search | /pattern → n / N | normal |
| Replace (current line) | :s/old/new/ | command-line |
| Replace (whole file) | :%s/old/new/g (add c for confirm) | command-line |
| Show numbers | :set number / :set nonumber | command-line |
| Recover swap | vi -r filename | shell |
| No swap mode | vi -n filename | shell |
| Open at line | vi +N filename | shell |
| Execute command on open | vi -c "cmd" filename | shell |

---

## Important Properties / Invariants
- Normal-mode commands (no colon) are required for most navigation & editing (must press Esc first). #modes
- Colon commands run in command-line mode and affect files/settings (start with `:`). #:
- Numeric prefixes apply to many commands (e.g., 3dd deletes 3 lines). #counts
- `.` repeats the last normal-mode change only (not command-line commands). #.
- Swap files exist only for unsafely-closed sessions; graceful save+quit removes the swap. #.swp
- Use `:%s/.../g` for global replace; add `c` for confirmation per match. #:%s

---

Keep this sheet near your exam materials; use the Quick Reference Table for rapid lookup. Good luck.