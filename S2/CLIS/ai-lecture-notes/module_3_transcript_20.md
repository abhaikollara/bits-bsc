# File & Directory Creation and Deletion (Linux)
#keywords: #file #directory #filesystem #create #delete #touch #mkdir #rm #rmdir #ls #recursive #force #interactive

## Key Definitions
- touch: create an empty file or update file timestamp.
- mkdir: create a new directory.
- ls: list files and directories in current directory.
- rm: remove (delete) files (and directories with options).
- rmdir: remove an empty directory.
- -R / -r (recursive): apply operation recursively into subdirectories.
- -f (force): do not prompt, ignore nonexistent files, suppress errors.
- -i (interactive): prompt before each removal.

## Command Syntax (quick "formulas")
- Create file: touch filename
- Create directory: mkdir dirname
- List files: ls [options]
- Delete file: rm filename
- Delete multiple files: rm file1 file2 ...
- Delete directory (recursive): rm -r directory
- Force recursive delete: rm -rf directory
- Interactive recursive delete: rm -r -i directory
- Remove empty directory: rmdir dirname

## Key Concepts / Actions
- Create file:
  - touch sample.txt
  - editors (vi, gedit) can also create/edit files
- Create directory:
  - mkdir my_folder
- Delete file:
  - rm sample.txt (permanent deletion)
- Delete multiple files:
  - rm file1 file2 file3
- Delete directory:
  - rmdir dir  — only if dir is empty
  - rm -r dir — removes dir and all nested files/dirs
  - rm -rf dir — force remove without prompts
  - rm -r -i dir — ask confirmation for each item while recursing
- Verification:
  - Use ls to confirm creation/deletion

## Important Properties / Invariants
- rm deletes permanently (no trash/recycle by default) — irreversible from shell.
- rmdir only succeeds on empty directories.
- rm without -r will not delete directories.
- -f suppresses prompts and errors; -i requests confirmation; be cautious combining.
- Recursive deletion traverses into subdirectories and removes everything therein.
- Always verify targets before using rm -r or rm -rf.

## Quick Reference (scannable)
| Command | Effect | Example |
|---|---:|---|
| touch file | create empty file or update timestamp | touch sample.txt |
| mkdir dir | create directory | mkdir newdir |
| ls | list directory contents | ls |
| rm file | delete file (permanent) | rm example.txt |
| rm file1 file2 | delete multiple files | rm a.txt b.txt |
| rmdir dir | delete empty directory only | rmdir olddir |
| rm -r dir | delete dir and contents recursively | rm -r my_folder |
| rm -rf dir | force delete dir and contents (no prompts) | rm -rf my_folder |
| rm -r -i dir | recursive delete with confirmation per item | rm -r -i dir1 |

## Safety Tips / Patterns
- Prefer rm -r -i when unsure (prompts per file/dir).
- Double-check with ls before destructive commands.
- Avoid rm -rf / and be cautious with wildcards (*).
- If you need recoverable deletions, use a trash utility or move to a designated backup directory rather than rm.
- When removing nested dirs, confirmations occur per-level/item when -i is used (you may be asked for each nested directory/file).

# End of cheatsheet — quick look-up tags: #touch #mkdir #ls #rm #rmdir #recursive #force #interactive #filesystem #delete #create