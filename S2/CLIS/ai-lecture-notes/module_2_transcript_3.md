# Linux file editing & basic file commands — Cheatsheet
#keywords: #vi #vim #ls #pr #mkdir #mv #cp #rm #cd #pwd #hidden-files #tab-completion #file-colors #human-readable #sorting #insert-mode #command-line

---

## Key Definitions
- vi filename — open file in VI (modal) editor. #vi #vim  
- Insert mode — VI mode for typing text (entered with i). #insert-mode  
- Normal mode — VI mode for commands (press ESC to enter). #vi  
- ls — list directory contents. #ls  
- pr — paginate/print file contents with options for page length, header, line numbers. #pr  
- mkdir name — create a directory. #mkdir  
- mv src dst — move/rename file or directory. #mv  
- cp src dst — copy file or directory. #cp  
- rm file — remove (delete) a file (permanent). #rm  
- cd dir — change current directory; cd .. goes to parent. #cd  
- pwd — print working directory (current path). #pwd  
- Hidden files — filenames starting with . (dot); shown by ls -a. #hidden-files  
- Tab-completion — press Tab to auto-complete filenames/paths. #tab-completion

---

## Formulas / Notation
- Command syntax: command [options] [arguments]  
- Combine options: ls -l + -h + -a => ls -lha

---

## Key Commands & Options (scannable)
- vi filename
  - i — enter Insert mode. #vi #insert-mode
  - ESC :w — save file. #vi
  - ESC :wq — save and quit. #vi
- ls
  - ls -l — long listing (permissions, owner, group, size, mod time). #ls
  - ls -a — show hidden files (dotfiles). #ls #hidden-files
  - ls -h — human-readable sizes (with -l: 6K, 2M, etc.). #human-readable
  - ls -t — sort by modification time (newest first). #sorting
  - Combine: ls -lha — long + human-readable + all. #ls
  - Color meaning (common defaults): blue = directory, green = executable, white = regular file. #file-colors
- pr
  - pr -l N filename — set lines per page to N (default 66). #pr
  - pr -h "Header" filename — set/modify header. #pr
  - pr -n filename — number lines. #pr
  - Options can be combined (e.g., pr -n -l 3 file). #pr
- mkdir name — create directory. #mkdir
- mv src dst — move or rename file/directory (use full/relative paths). #mv
- cp src dst — copy file to destination. #cp
- rm filename — permanently delete file (no recycle). Use with caution. #rm
- cd path — change directory; cd .. = parent, cd . = current. #cd
- pwd — show current directory path. #pwd

---

## Important Properties / Invariants
- VI is modal: must switch modes (Insert vs Normal) to edit vs issue commands. #vi #insert-mode
- ls -l shows permission string (e.g., -rwxr-xr-x), owner, group, size, timestamp. #ls
- Hidden files begin with '.' and are not shown unless using -a. #hidden-files
- Tab-completion speeds navigation and reduces typing errors. #tab-completion
- mv moves (removes source from origin) while cp leaves original intact. #mv #cp
- rm permanently deletes files — no undo by default. Back up critical files. #rm
- Options can be combined; order usually irrelevant for POSIX utilities. #ls #pr

---

## Quick Reference (one-line facts)
- Open VI: vi file.txt
- Insert text: In Normal mode press i → type → ESC to stop inserting
- Save: ESC :w
- Save & quit: ESC :wq  (or :x)
- Quit without saving: ESC :q! 
- List files: ls
- List long: ls -l
- Show hidden: ls -a
- Human sizes: ls -lh
- Sort by time: ls -lt (or ls -t)
- All options: ls -lha (long + human + all)
- Show current dir: pwd
- Change dir: cd target_dir
- Create dir: mkdir name
- Move file: mv file target_dir/
- Copy file: cp file target_dir/
- Remove file: rm file
- Print file with page length: pr -l N file
- Number lines: pr -n file
- Set header: pr -h "Header" file

---

## Safety Tips
- Double-check target paths before mv, cp, rm. #mv #cp #rm  
- Use backups or version control for important files.  
- Use ls to verify before/after file operations. #ls

---

Tags for quick find: #vi #vim #ls #pr #mkdir #mv #cp #rm #cd #pwd #hidden-files #tab-completion #file-colors #human-readable #sorting