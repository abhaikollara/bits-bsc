# Linux Files & Directories — Cheatsheet
#hashtags: #linux #filesystem #files #directories #paths #hierarchy #bash #commands #create #update #delete #move #copy #ls #cd #pwd #mkdir #rmdir #touch #rm #cp #mv #cat #echo #redirection #globbing

---

## Key Definitions
- File: named collection of bytes stored on disk. #file  
- Directory: container that lists names and links to files and other directories. #directory  
- Filesystem: hierarchical organization of files and directories on storage. #filesystem  
- Root (/): top-level directory of the filesystem hierarchy. #root  
- Working directory: current directory for the shell; shown by `pwd`. #cwd #pwd  
- Absolute path: full path from root (starts with `/`). #absolutepath  
- Relative path: path relative to current directory (no leading `/`). #relativepath  
- `.` : current directory. #dot  
- `..` : parent directory. #dotdot  
- Hidden file: filename beginning with `.`; not shown by default by `ls`. #hiddenfile

---

## Formulas / Syntax Patterns
- Path syntax: /root/subdir/.../file or ./subdir/file or ../sibling/file  
- Command general form: command [options] <operands>  
- Redirection: `>` overwrite, `>>` append  (e.g., `echo hi > file`) #redirection  
- Globbing (wildcards): `*` (any chars), `?` (one char), `[...]` (set) #globbing

---

## Key Commands & Concepts (quick bullets)
- Navigation
  - `pwd` — print working directory. #pwd  
  - `cd <dir>` — change directory; `cd ~` to home, `cd -` previous. #cd
  - `ls` — list directory contents; common flags: `-l`, `-a`, `-h`. #ls
- Create files & directories
  - `touch <file>` — create empty file or update timestamp. #touch  
  - `mkdir <dir>` — create directory; `-p` for parent dirs. #mkdir
- Read/update file contents
  - `cat <file>` — print file contents. #cat  
  - `echo "text" > file` — write (overwrite) text to file. #echo #redirection  
  - `echo "text" >> file` — append text to file. #redirection
- Copy, move, rename
  - `cp src dst` — copy file(s); `-r` recursive for directories. #cp  
  - `mv src dst` — move or rename files/dirs. #mv
- Delete
  - `rm file` — remove file; `rm -r dir` remove directory recursively; `rmdir dir` remove empty dir. #rm #rmdir
- Info & metadata
  - `stat <file>` — status information (size, timestamps, inode). #stat (if available)  
  - `file <file>` — identify file type. #file
- Permissions & ownership (reference)
  - `ls -l` shows permission bits and owner/group. #permissions  
  - `chmod`, `chown` — change permissions/owner (syntax not expanded here). #chmod #chown

---

## Important Properties / Invariants
- Filesystem is hierarchical (tree) with unique absolute paths. #hierarchy  
- Filenames are case-sensitive on typical Linux filesystems.  
- Directories link names to inodes (names can point to same inode via hard links; symbolic links are special files) — (reference). #inode #symlink  
- `mkdir -p` avoids intermediate errors; `rm -r` is destructive — use with care. #safety  
- Hidden files begin with `.` and require `ls -a` to list. #hiddenfile
- Relative operations depend on current working directory scope. #cwd

---

## Quick Reference (commands table)
- Navigation
  - `pwd` — show cwd
  - `cd <dir>` — change dir (`cd ..`, `cd -`, `cd ~`)
  - `ls` — list (`-l` long, `-a` all, `-h` human sizes)
- Create / Read / Write
  - `touch file` — create empty or update timestamp
  - `mkdir dir` — create dir (`-p` parents)
  - `cat file` — display file
  - `echo text > file` — overwrite file
  - `echo text >> file` — append to file
- Copy / Move / Rename / Delete
  - `cp src dst` — copy (`-r` for dirs)
  - `mv src dst` — move/rename
  - `rm file` — remove file
  - `rm -r dir` — remove dir recursively
  - `rmdir dir` — remove empty dir
- Search & meta
  - `ls -l` — permissions, owner, size, date
  - `stat file` — detailed metadata
  - `file file` — detect type

Safety tips (quick):
- Preview before delete: `ls` the target first.  
- Use `rm -i` or `-v` for interactive/verbose removal.  
- Use `cp -r` and `mv` carefully across filesystems (behavior differs).

---

Use this as a compact reference during the exam — commands, flags, and path rules are the most-queried items. Keep practicing commands in a shell to internalize behavior.