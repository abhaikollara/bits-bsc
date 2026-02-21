# vi Editor Cheatsheet
#vi #editor #linux #terminal #text-editor #modes #navigation #editing #commands #save #quit #delete #copy #paste #redirection #options

## Key Definitions
- Normal mode: Default mode for navigation and issuing commands. (aka command mode)
- Insert mode: Mode to insert/edit text (enter with i).
- Command-line mode: Mode for file-level commands (enter with :).
- Buffer: The in-memory contents of the file you are editing.
- Redirection: Shell operator to write command output to a file (e.g., vi --help > abc.txt).

## Startup Options (as in transcript)
- -r : recover file after crash (#-r)
- -c cmd : run a command after opening the file (#-c)
- -n : open file in read-only mode (#-n)
- -i {ext} : set backup extension (#-i)
- +N : open at line N (# +N)
- --help : show usage (#--help)

## Common Commands / Keybindings
- Open file: vi filename (#vi)
- Show help and save output: vi --help > abc.txt (#redirection)
- Enter Insert mode: i (#i)
- Exit to Normal mode: Esc (#esc)
- Enter Command-line mode: : (colon) (#colon)

Command-line (type after colon):
- :w  — write (save) file (# :w)
- :q  — quit (# :q)
- :wq — save and quit (# :wq)
- :q! — quit without saving (# :q!)

Normal-mode navigation:
- Arrow keys — move cursor (#arrows)
- h — left (#h)
- j — down (#j)
- k — up (#k)
- l — right (#l)

Normal-mode editing:
- x — delete character under cursor (#x)
- dd — delete current line (#dd)
- yy — yank (copy) current line (#yy)
- p — paste after cursor (#p)

## Important Properties / Invariants
- Modal behavior: Only one mode active at a time; Esc returns to Normal.
- : commands are issued from Command-line mode (start with colon).
- dd / yy operate on whole lines. x operates on single character under cursor.
- p pastes after the cursor/line (use P to paste before).
- Normal mode is required to run navigation and most editing commands.
- Insert mode shows -- INSERT -- (or similar) in the status area.

## Quick Reference (scannable)
- Start:
  - vi file.txt
  - vi --help > abc.txt
- Modes:
  - Normal (default) → i → Insert → Esc → Normal → : → Command-line
- Save / Quit:
  - Save: :w
  - Quit: :q
  - Save & quit: :wq
  - Quit w/o saving: :q!
- Navigation:
  - Left/Down/Up/Right: h / j / k / l (or arrow keys)
- Edit:
  - Delete char: x
  - Delete line: dd
  - Copy(yank) line: yy
  - Paste: p
- Startup options:
  - Recover: -r
  - Run command: -c 'cmd'
  - Read-only: -n
  - Backup ext: -i{ext}
  - Start at line: +N
- Tips:
  - Use Esc to ensure you’re in Normal mode before command keys.
  - Use :w before :q to avoid losing changes.
  - Use redirection to capture command output: command > file

## Search/Find (note from standard vi usage)
- Enter Command-line mode then use /pattern or ?pattern (not in transcript but common in vi)

Hashtags for quick search: #vi #editor #modes #normal-mode #insert-mode #command-line-mode #navigation #h #j #k #l #x #dd #yy #p #w #q #wq #q! #-r #-c #-n #-i #+N #--help #redirection

(Concise reference for exam use — focus on commands and mode transitions.)