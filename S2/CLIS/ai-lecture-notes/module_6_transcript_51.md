# vi — Copy, Cut, Paste Cheatsheet
# #vi #copy #paste #cut #yank #put #buffer #normal-mode #visual-mode #ex-command #yy #dd #p #y$ #range

## Key Definitions (one-line)
- Normal mode: vi's default mode for navigation and commands.  
- Visual mode: selection mode entered with v to highlight text for operations.  
- Yank: copy text into vi's unnamed buffer (command: y).  
- Put: paste text from buffer into file (command: p).  
- Delete (cut): remove text and place it into buffer (command: d).  
- Buffer: temporary storage where yanked/deleted text is kept.  
- Ex commandline: colon (:) commands for ranges and other operations.

## Formulas / Command Patterns
- [count]yy  — yank (copy) count full lines (default count = 1). Example: 3yy
- [count]dd  — delete (cut) count full lines. Example: 2dd
- p — put (paste) buffer contents below the cursor/line
- y$ — yank from cursor to end of line
- :start,end y — yank lines start through end in Ex mode. Example: :5,8 y
- v + movement + y — Visual mode selection then yank selected text

## Key Commands / Concepts (bullet list)
- yy — yank (copy) current entire line into buffer (#yy #yank)
- [n]yy — yank n lines starting at current line (e.g., 3yy) (#count)
- dd — delete (cut) current entire line into buffer (#dd #cut)
- [n]dd — delete n lines (cuts to buffer)
- p — paste (put) buffer contents below current cursor/line (#p #put)
- y$ — yank from cursor position to end of line (#y$)
- :m,n y — yank lines m through n via Ex command (e.g., :5,8 y) (#ex-command #range)
- v then movement then y — select text in Visual mode and yank selection (#visual-mode)
- Start commands in Normal mode (press Esc to ensure)

## Important Properties / Invariants
- p always pastes below (after) the cursor/line (transcript focus).  
- Yanked/deleted text goes to the unnamed buffer and is available to p immediately.  
- Numeric prefix repeats the command on lines (3yy = yank 3 lines; same for dd).  
- y$ uses motion operator pattern: yank + motion (here $ = end-of-line).  
- Ex-range yank uses line numbers and requires Enter after the command.  
- Visual mode selection uses movement keys and ends with y to yank.

## Quick Reference (scannable)
- Mode: Ensure Normal mode (press Esc)
- Copy line: yy
- Copy n lines: n yy (e.g., 3yy)
- Cut line: dd
- Cut n lines: n dd
- Paste below cursor/line: p
- Copy to end of line (from cursor): y$
- Copy line range: :start,end y (e.g., :5,8 y)
- Visual copy: v → move to select → y
- Note: Yank = copy, Put = paste

## Short Examples
- Copy line 10 to current: :10y then navigate and p
- Copy chars from cursor to EOL: position cursor → y$
- Copy 4 lines starting here: 4yy → move → p

#hashtags recap: #vi #yank #put #yy #dd #p #y$ #visual-mode #normal-mode #ex-command #range #buffer

(Keep this sheet handy — all commands assume you begin in Normal mode.)