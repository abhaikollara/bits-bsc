# vi editor — Quick Cheatsheet
#hashtags: #vi #vim #text-editor #modal-editing #normal-mode #insert-mode #visual-mode #ex-mode #navigation #editing #search-and-replace #copy-paste #registers #macros #undo-redo

---

## Key Definitions
- Modal editor: editor with distinct modes (different keys do different things). #modal-editing  
- Normal mode: default mode for navigation and commands. #normal-mode  
- Insert mode: type text; enter with i/a/o. #insert-mode  
- Visual mode: select text (char/line/block) for commands. #visual-mode  
- Ex/Command-line mode: run commands starting with : or / ? . #ex-mode  
- Operator: command that acts on a text object or motion (e.g., d, c, y). #operators  
- Motion: movement command used by operators (e.g., w, $, t). #navigation  
- Register: named storage for yanks/deletes (", "a, etc.). #registers  
- Macro: recorded sequence of commands stored in a register (q<reg> ... q). #macros

---

## Command Pattern / Formula
- General form: [count] [operator] [motion]  
  - Example: 3dw = delete 3 words  
- Repeat last change: . (dot)  
- Substitute (line scope): :[range]s/pattern/replacement/[flags]  
  - Common: :%s/foo/bar/gc (global + confirm)

---

## Essential Commands (Quick Reference)
Navigation
- h / j / k / l = left / down / up / right  
- w / b / e = next word / back / end of word  
- 0 / ^ / $ = line start / first non-blank / line end  
- gg / G = top / bottom of file  
- Ctrl-d / Ctrl-u = half-page down / up  
- f<char> / t<char> = find / till char; F/T reverse  
- % = jump to matching bracket

Insert & Replace
- i / I = insert before cursor / line-start insert  
- a / A = append after cursor / line-end append  
- o / O = open new line below / above  
- r<char> = replace one char; R = enter replace mode

Editing / Operators
- x = delete char; X = delete before cursor  
- dd = delete line; D or d$ = delete to EOL  
- dw / dW = delete word  
- cw = change word (delete + insert)  
- c$ = change to end of line  
- s / S = substitute/delete and enter insert / line substitute

Yank & Paste
- y / yy = yank (copy) motion / line  
- p = paste after cursor; P = paste before cursor  
- "ay = yank into register a; "ap = paste from register a

Visual Mode
- v = char-wise select; V = line-wise; Ctrl-v = block-wise  
- > / < = indent selection; y/d/c = yank/delete/change selection

Search & Replace
- /pattern (enter) = forward search; ?pattern = backward  
- n / N = next / previous match  
- :%s/pat/repl/g = replace all in file; flags: g (global), c (confirm), i (ignore-case)

Files & Ex Commands
- :w = save; :q = quit; :wq or :x = save & quit; :q! = quit discard  
- :e <file> = open file; :r <file> = read file into buffer  
- :set number / nonumber = toggle line numbers

Undo / Redo
- u = undo (per change)  
- Ctrl-r = redo

Registers & Marks
- "a, "b = explicit register usage for yank/delete/paste  
- ma = set mark a at current cursor; `a = jump to exact position; 'a = jump to start of line of mark

Macros
- q<reg> = start recording into register; q = stop  
- @<reg> = play macro once; @@ = repeat last macro

Misc
- :!cmd = run shell command; :w !sudo tee % = save with sudo (when needed)  
- & = repeat last :s with same flags

---

## Important Properties / Invariants
- Modal behavior: keys do different things per mode — know current mode. #modal-editing  
- Operators compose with motions (operator + motion); counts apply to both. #operators  
- Changes are atomic units for undo (u undoes last change). #undo-redo  
- Dot (.) repeats the last change exactly — powerful for repetitive edits.  
- Registers persist across operations until overwritten; unnamed register holds latest yank/delete. #registers  
- Visual modes: char/line/block change semantics (block for column edits). #visual-mode

---

## Quick Reference Table (Most-Used)
| Action | Command(s) |
|---|---|
| Enter insert | i / a / o |
| Save / Quit | :w / :q / :wq / :q! |
| Undo / Redo | u / Ctrl-r |
| Yank / Paste | y / yy / p / P |
| Delete / Change | x / dd / dw / c(w/motion) |
| Repeat last change | . |
| Search | /pattern ?pattern ; n / N |
| Substitute line/file | :s/pat/repl/flags ; :%s/... |
| Record macro | q<reg> ... q ; play: @<reg> |
| Set mark / jump | ma ; `a / 'a |

---

## Exam Quick Tips
- If unsure of mode: press Esc to return to Normal mode.  
- Use counts to scale commands (e.g., 5>> to indent 5 lines).  
- Combine dot (.) and macros to automate repetitive sequences.  
- Use :%s with g and c flags for file-wide safe replacements.  
- Use registers ("a, "b) to hold important clips; prefix with " when y/d/p.

---

Keep this sheet near your workstation — practice common combos (dw, cw, yyp, :%s) until muscle memory builds.