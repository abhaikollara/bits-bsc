# vi/vim Quick Cheatsheet — Deleting & Common Shortcuts
#hashtags: #vi #vim #editor #linux #commands #shortcuts #delete #navigation #insertmode #search

---

## Key Definitions
- Normal (command) mode: default mode for commands (press Esc to enter).  
- Insert mode: editing/text-entry mode (enter with i, a, I, A).  
- Motion: movement commands used with operators (e.g., w, $, 0).  
- Count prefix: a number before a command to repeat it (e.g., 3dd).

---

## Formulas / Command Patterns
- [count] + command — repeat command (e.g., 3dd deletes 3 lines).  
- operator + motion — perform operator over a motion (d + w => dw).  
- d$ or D — delete from cursor to end of line.  
- r<char> — replace the character under the cursor with <char>.

---

## Key Commands / Concepts (#hashtags included)
- Delete single char: x (delete under cursor). #x  
  - X (uppercase) deletes character before cursor. #X
- Delete line: dd (delete current line). #dd  
  - [count]dd (e.g., 3dd) deletes that many lines. #count
- Delete to end of line: D or d$ (from cursor to EOL). #D #d$  
- Delete word: dw (delete from cursor to start of next word). #dw  
- Delete word + surrounding space: daw (delete around word). #daw
- Delete from cursor to end-of-line (single-key): D. #D
- Replace single character: r<char>. #r
- Undo / Redo: u (undo), Ctrl+R (redo). #undo #redo
- Save & Quit: :wq  (write and quit). #save #wq
- Quit without saving: :q!  (force quit). #quit #q!
- Insert mode entries: 
  - i (insert at cursor) #i
  - I (insert at beginning of line) #I
  - a (append after cursor) #a
  - A (append at end of line) #A
- Navigation:
  - 0 (zero) — beginning of line. #0
  - $ — end of line. #$
  - gg — beginning of file. #gg
  - G — end of file. #G
- Search:
  - /pattern then Enter — search forward. #search #/
  - n — next match. #n

---

## Important Properties / Invariants
- vi is modal: commands only work in Normal mode; Insert mode is for typing. #modal  
- Many operators use motions (d, c, y + motion). Memorize common motions (w, $, 0, gg, G). #motions  
- Count prefixes apply to most commands (e.g., 5w, 3dd). #count  
- Single-key commands are case-sensitive (x vs X, d vs D). #case

---

## Quick Reference Table (scannable)

| Action | Command(s) |
|---|---|
| Delete char under cursor | x |
| Delete char before cursor | X |
| Replace char with <c> | r<c> |
| Delete current line | dd |
| Delete N lines | Ndd (e.g., 3dd) |
| Delete to end of line | D or d$ |
| Delete word | dw |
| Delete word + surrounding space | daw |
| Enter insert mode (at cursor) | i |
| Insert at line start | I |
| Append after cursor | a |
| Append at line end | A |
| Save & quit | :wq |
| Quit without saving | :q! |
| Undo / Redo | u / Ctrl+R |
| Go to start/end of line | 0 / $ |
| Go to start/end of file | gg / G |
| Search forward | /pattern ↵ , then n for next |

---

## Quick Tips
- Prefix with a number to repeat (e.g., 4w, 2dd). #repeat  
- Use d + motion to delete flexible ranges (d0, d$, dw, da(, etc.). #d+motion  
- When unsure, press Esc to return to Normal mode. #Esc

---

Keep this sheet to quickly find keystrokes and patterns during the exam. Practice a few commands to build muscle memory.