# Vi Editor — Modes & Essential Commands (cheatsheet)
#hashtags: #vi #vim #editor #NormalMode #InsertMode #CommandMode #ExCommandMode #navigation #search #replace #save #quit #editing #yank #paste

## Key Definitions
- Normal mode: Default modal state for navigation and issuing commands.
- Insert mode: Mode for inserting text (entered with i).
- Command mode: Ex/colon mode for file operations like save/quit (entered with :).
- Ex Command mode: Advanced command-line mode (starts with :), used for search/replace and other Ex commands.
- Cursor navigation: Movement in Normal mode via h/j/k/l (left/down/up/right).

## Formulas / Command Patterns
- Open file: vi filename
- Enter Insert mode: i
- Return to Normal mode: Esc
- Command/Ex mode prompt: :
- Search (transcript form): :/pattern Enter
  - Common alternative: /pattern Enter (forward search)
- Replace (global): :%s/old/new/g
  - Case-sensitive by default (capital/lower matters)

## Key Commands & Concepts
- Opening:
  - vi filename — open/create file (#vi #editor)
- Mode switching:
  - Normal → Insert: i (#InsertMode)
  - Any mode → Normal: Esc (#NormalMode)
  - Normal → Ex/Command: : (#CommandMode #ExCommandMode)
- Navigation (Normal mode): 
  - h = left, j = down, k = up, l = right (#navigation)
- Basic editing (Normal mode):
  - Delete character: x (#editing)
  - Delete line: dd (#editing)
  - Copy (yank) line: yy (#yank)
  - Paste after cursor: p (#paste)
- File operations (Ex/Command mode):
  - Save: :w (#save)
  - Quit: :q (#quit)
  - Save & quit: :wq or :x (#save #quit)
  - Force quit (discard changes): :q! (#quit)
- Search & replace (Ex mode):
  - Search: :/pattern Enter (or /pattern) (#search)
  - Replace all occurrences in file: :%s/old/new/g (#replace)
  - Replace with case matching — by default case-sensitive (watch capitalization)

## Important Properties / Invariants
- Vi is modal: same keys do different things depending on mode (#NormalMode #InsertMode).
- Editor opens in Normal mode by default.
- Esc always returns you to Normal mode from Insert or other modes.
- Ex/Command mode commands begin with : and execute when Enter is pressed.
- Search/replace using :%s is file-wide unless range is specified.
- Case sensitivity: searches and :s replacements are case-sensitive unless modified.

## Quick Reference (one-line commands)
- Open: vi filename
- Insert mode: i
- Back to Normal: Esc
- Move: h (←), j (↓), k (↑), l (→)
- Delete char: x
- Delete line: dd
- Yank line: yy
- Paste: p
- Save: :w
- Quit: :q
- Save & quit: :wq or :x
- Force quit: :q!
- Search (lecture form): :/word Enter
- Common search: /word Enter
- Replace all: :%s/old/new/g
- Replace (case-sensitive): ensure pattern matches exact case (e.g., L vs l)

## Examples (compact)
- Open file: vi ABC.TXT
- Search for "list": :/list Enter  (if case differs, search :/List)
- Replace all "list" → "enumerate": :%s/list/enumerate/g
- If "List" (capital L) present: :%s/List/enumerate/g

Keep this sheet near your notes for quick lookup during the exam.