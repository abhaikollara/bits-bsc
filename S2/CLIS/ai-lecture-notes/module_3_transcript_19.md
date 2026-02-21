# Navigating & Listing Files (UNIX/Linux) — Cheatsheet
#keywords: #filesystem #paths #pwd #mkdir #cd #ls #relative-path #absolute-path #dot #dotdot #tilde #hidden-files

## Key Definitions
- pwd: print working directory — shows current directory (absolute path). #pwd  
- mkdir: make directory — create new directory. #mkdir  
- cd: change directory — move to another directory. #cd  
- ls: list directory contents. #ls  
- Absolute path: full path from root (starts with `/`). #absolute-path  
- Relative path: path relative to current directory (no leading `/`). #relative-path  
- . (dot): entry referring to the current directory. #dot  
- .. (dotdot): entry referring to the parent directory. #dotdot  
- ~ (tilde): shorthand for the current user's home directory. #tilde #home  
- Hidden files: filenames starting with `.`; shown with `ls -a`. #hidden-files

## Formulas / Notation (quick)
- Absolute path example: /home/sai/my_directory  
- Relative path example: my_directory/subdir/file.txt  
- Home shortcut: ~ ≡ /home/username  
- Navigation depth: cd dir1/dir2/dir3  (can jump multiple levels in one command)

## Key Commands / Concepts
- pwd — show current directory (absolute). #pwd
- mkdir <name> — create directory named <name>. #mkdir
- cd <dir> — change to directory <dir> (relative or absolute). #cd
- cd .. — go to parent directory (via `..`). #dotdot
- cd . — stay in the same directory (via `.`). #dot
- cd ~  or cd  — go to home directory. #tilde #home
- ls — list files in current directory. #ls
- ls <path> — list files in given path without cd. #ls
- ls -l -a -h (common combined option: -lah)  
  - -l: long format (permissions, owner, size, date)  
  - -a: include hidden files (names starting with `.`)  
  - -h: human-readable sizes (e.g., K, M). #hidden-files
- Path types:  
  - Absolute: starts with `/` — independent of cwd. #absolute-path  
  - Relative: starts from current working directory — does not start with `/`. #relative-path

## Important Properties / Invariants
- Every directory has `.` (self) and `..` (parent) entries automatically. #dot #dotdot  
- `pwd` always returns an absolute path. #pwd  
- `cd` with an absolute path ignores current directory; with relative path it is resolved from cwd. #cd  
- `ls <dir>` lists contents without changing cwd. #ls  
- `cd` can accept multiple-level paths in one command (no need to cd step-by-step). #cd

## Quick Reference (scannable)
- Show current dir:
  - pwd
- Create directory:
  - mkdir mydir
- Enter directory:
  - cd mydir         (relative)
  - cd /a/b/c        (absolute)
  - cd ~             (home)
  - cd               (also goes to home)
- Move up:
  - cd ..            (parent)
  - cd ../..         (grandparent)
- List files:
  - ls               (names)
  - ls -l            (detailed)
  - ls -a            (include hidden)
  - ls -lah /path    (detailed + human sizes + hidden)
  - ls ./subdir      (list subdir from cwd)
- Examples:
  - mkdir project
  - cd project
  - pwd  → /home/sai/project
  - ls -lah ~/public_html
  - cd /var/log/apache2
  - cd ../../        (go up two levels)

Keep this sheet for quick lookup of commands, path rules, and common ls options.