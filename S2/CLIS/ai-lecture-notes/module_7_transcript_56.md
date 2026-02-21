# Vi/Vim Crash Recovery Cheatsheet
#hashtags: #vi #vim #recovery #swapfile #undo #autorecovery #backup #vimrc #viminfo #commands

## Key Definitions
- Swap file: .filename.swp — temporary file created while editing to store unsaved changes. #swapfile  
- Undo history: in-memory (or persistent if configured) record of edits allowing undo/redo. #undo  
- Auto recovery: use of saved recovery info (viminfo/undo files) to restore unsaved work after a crash. #autorecovery  
- Backup file: a saved copy of the previous file version created when saving (controlled by `set backup`). #backup  
- viminfo: file that stores registers, command/history, marks, etc.; its size can be limited (KB). #viminfo  
- .vimrc: user configuration file (~/.vimrc) to enable recovery/backup settings. #vimrc

## Formulas / Notations
- Swap filename pattern: .<original_filename>.swp  
- Example viminfo size setting (transcript example): viminfo maxsize = 1000 (kilobytes)  
- Time complexity: N/A (editor actions; not algorithmic complexity)

## Key Concepts / Commands
- Recover from swap file:
  - Automatic swap creation: .document.txt.swp while editing document.txt. #swapfile
  - Recover via command: vim -r <file>  (or vim -r .<file>.swp) — attempts recovery. #commands
  - Open file normally: Vim will prompt to recover if a swap exists. #commands
- Undo / Redo:
  - Undo: u  (in normal mode). #undo
  - Redo: CTRL+R (in normal mode). #undo
  - Navigate undo history to restore desired state. #undo
- Auto recovery / persistent history:
  - Configure via ~/.vimrc; viminfo and persistent undo settings control auto-recovery. #vimrc #viminfo
  - Example limits: remember up to 1000 lines/history; max viminfo file size 1000 KB (example). #viminfo
- Backups:
  - Enable backup: :set backup  (or add to ~/.vimrc). #backup
  - Backup creates copy before writing file (helps after crash). #backup

## Important Properties / Invariants
- Swap files live in the same directory by default; they are removed on clean exit. #swapfile  
- Swap contains unsaved edits; opening a file with an existing swap will prompt recovery options. #swapfile  
- Undo history is available in-session; to persist across sessions, enable persistent undo (undofile) in config. #undo  
- viminfo controls what history/registers are saved between sessions and has size limits (KB). #viminfo  
- Backups provide the last saved version; swap provides unsaved changes. #backup #swapfile

## Quick Reference (Scannable)
- Swap filename: .<file>.swp  
- Common prompts when swap exists: options include (R)ecover, (E)dit anyway, (D)elete swap, (Q)uit. #swapfile
- Commands:
  - Open file normally: vim document.txt  #commands
  - Recover: vim -r document.txt  OR vim -r .document.txt.swp  #commands
  - Manual recover from within vim: :recover  (then :w to save recovered file)  #commands
  - Save file: :w  (write changes)  #commands
  - Enable backup (session/config): :set backup  / add to ~/.vimrc  #backup #vimrc
  - Undo: u  — Redo: CTRL+R  #undo
- Config tips (put in ~/.vimrc):
  - set backup                  " enable backup files  #backup  
  - set undofile                " enable persistent undo (recommended)  #undo  
  - set viminfo='1000,<1000     " example: remember 1000 lines/history, max viminfo size 1000 KB  #viminfo
- Recovery workflow (crash -> restore):
  1. cd to file directory.  
  2. Check for swap: ls -a | grep .<file>.swp  (swap exists => recovery possible). #swapfile  
  3. Run: vim -r <file>  OR open file in vim and choose Recover when prompted. #commands  
  4. Inspect recovered buffer, use u/CTRL+R to navigate undo history. #undo  
  5. Save recovered content: :w [newname] (optionally back up old file). #commands

Keep these handy in your exam notes: swap files (.swp), vim -r for recovery, u / CTRL+R for undo/redo, :w to save, and set backup / viminfo / undofile in ~/.vimrc to reduce future data loss.