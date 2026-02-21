# Vi/Vim — Auto-recovery, Backup & Version-control Cheatsheet

#keywords: #vi #vim #viminfo #swap #backup #backupext #backupdir #versioncontrol #git #vimrc #autosave

## Key Definitions
- vim: "Vi IMproved" (modern vi implementation).  
- .vimrc: per-user Vim configuration file (~/.vimrc).  
- .viminfo: file that stores persistent session info (history, marks, registers).  
- swap file (.swp): temporary file used for crash recovery (unsaved edits).  
- backup: an automatic copy of the file made when saving (preserves previous version).  
- backupext (backupextension): extension added to backup files (default: ~).  
- backupdir: directory where backup files are stored.  
- :recover / -r: commands to recover from swap files.  
- Version control: tracking file history; Vim backups provide a basic form; use Git for full VCS.

## Formulas / Notation
- Vim option syntax: set <option> or set <option>=<value>  
- Example viminfo format (option string): '100,<1000,s10,h'  
  - 100 = max saved lines; <1000 = max chars per line; s10 = save session every 10s; h = include history

## Key Concepts / Commands
- Enabling/disabling options (in command mode, press Esc then type):
  - :set backup         — enable backups (#backup)
  - :set nobackup       — disable backups
  - :set backupext=.bak — set backup extension to .bak (#backupext)
  - :set backupdir=~/.vim/backups — set centralized backup directory (#backupdir)
  - :set viminfo='100,<1000,s10,h' — configure viminfo behavior (#viminfo)
- Common actions:
  - :w                 — write/save file
  - :q / :q!           — quit / force quit
  - vim filename       — open file in vim
  - git init; git add <file>; git commit -m "msg" — external VCS workflow (#git, #versioncontrol)
- Recovery:
  - Swap files (.swp) used for crash recovery — use :recover or vim -r to restore
  - viminfo stores persistent session data (history, marks, registers) across normal exits

## Important Properties / Invariants
- Default backup suffix is tilde (~). Backup files typically named file.txt~ unless changed. (#backup)
- By default backup files are created in the same directory as the original file unless backupdir is set. (#backupdir)
- Vim automatically updates .viminfo on normal exit; abnormal exits (crash) may still leave swap files for recovery. (#viminfo, #swap)
- Setting backup preserves the previous version of the file at each save (basic versioning). (#versioncontrol)
- For robust versioning/history use an external VCS (Git) — Vim backups are not a replacement. (#git)

## Quick Reference (scannable)

Options & example .vimrc lines
- set viminfo='100,<1000,s10,h'    — configure auto-recovery/history (#viminfo)
- set backup                       — enable backup files (#backup)
- set nobackup                     — disable backup files
- set backupext=.bak               — change backup file extension (#backupext)
- set backupdir=~/.vim/backups     — store backups centrally (#backupdir)
- set swapfile                     — enable swap file creation (default) (#swap)
- set noswapfile                   — disable swap files

Commands (in Vim command mode; press Esc then :)
- :set backup
- :set nobackup
- :set backupext=.bak
- :set backupdir=~/.vim/backups
- :w    — save file
- :recover or vim -r <file> — recover from swap file

Basic Version-control workflow (recommended)
- Initialize: git init
- Stage: git add <file>
- Commit: git commit -m "meaningful message"
- Use Vim for editing, Git for history and branching (#git, #versioncontrol)

File locations / names
- ~/.vimrc     — user Vim config
- ~/.viminfo   — viminfo file (session/history)
- default backup: <filename>~ or <filename>.bak (if backupext set)
- swap files: .<filename>.swp (in file dir or swapdir if configured)

Notes (exam-friendly)
- Backups = simple local copy on save; useful for quick rollback. (#backup)  
- Swap = crash recovery; use :recover if Vim or system crashes. (#swap)  
- viminfo stores persistent history/marks across sessions; configure with set viminfo. (#viminfo)  
- Prefer Git for real version control; Vim can call external commands and works well inside a Git workflow. (#git)

End of cheatsheet.