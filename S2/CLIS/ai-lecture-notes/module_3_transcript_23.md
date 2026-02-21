# Linux disk-usage & links — Cheatsheet
#hashtags: #df #du #ncdu #readlink #unlink #ls #symlink #hardlink #diskusage #filesystem

---

## Key Definitions
- df: show filesystem disk space usage (per mounted filesystem).  
- du: estimate disk usage of files/directories (per path).  
- ncdu: ncurses-based interactive disk-usage explorer.  
- symbolic link (symlink): a filesystem entry that points to another pathname (can be dangling, crosses filesystems). #symlink  
- hard link: another directory entry pointing to the same inode (same file contents, cannot cross filesystems, not for dirs normally). #hardlink  
- readlink: print the target of a symbolic link. #readlink  
- unlink: remove a name (link) from the filesystem. #unlink  
- ls -A / ls -l: list files (incl. hidden); long listing shows link targets and file types. #ls

---

## Formulas / Notation
- Human-readable sizes: -h shows sizes in KB/MB/GB (powers of 1024 for GNU tools). #units  
- df columns (typical): Filesystem | Size | Used | Avail | Use% | Mounted on  
- du summary flags: -s (summarize per argument), -c (show grand total). #du

---

## Key Commands & Usage (quick reference)
| Command | Syntax | Purpose / Notes |
|---|---:|---|
| df | df -h | Show disk usage per filesystem in human-readable form. #df |
| du | du -h <path> | Show sizes of files/dirs (human-readable). #du |
| du (summary) | du -s <path> | Show only total size for each argument. #du |
| du (grand total) | du -c <paths> | Include grand total at end. #du |
| ncdu | ncdu <path> | Interactive, navigable disk usage explorer. Use arrows/enter to drill down. #ncdu |
| readlink | readlink <symlink> | Print the target of a symlink. #readlink |
| unlink | unlink <path> | Remove a directory entry (link) — works for hard links and symlinks (removes the name). #unlink |
| ls (all) | ls -A | List all files except . and .. (includes hidden). #ls |
| ls (long) | ls -l | Long listing; leading char shows type (l = symlink) and for symlink shows "-> target". #ls |

---

## Important Properties / Invariants
- df reports per mounted filesystem; du reports by directory content (can differ due to mount points, sparse files, or reserved space). #df #du
- du counts space used by data referenced in the directory tree you give; files on other mounts under that path may not be included unless you traverse mounts. #du
- Symlink characteristics:
  - stores a pathname; can point to anything (file/dir); can be dangling; visible as type 'l' in ls -l. #symlink
  - Can cross filesystem boundaries. #symlink
- Hard link characteristics:
  - multiple names --> same inode; file data persists until last link (name) is removed. #hardlink
  - Cannot normally link across filesystems; linking to directories is restricted. #hardlink
- unlink removes a single name; if it was the last name, the inode/data are freed (subject to open file descriptors). #unlink
- readlink only prints the link target; does not resolve recursively by default (use readlink -f to canonicalize). #readlink

---

## Quick Reference / Patterns
- Common flags:
  - df -h : human-readable filesystem usage. #df
  - du -h : human-readable per-file/dir sizes. #du
  - du -sh : concise total for a path (s + h). Example: du -sh /var/log
  - du -hc * : sizes for each entry + grand total. #du
  - ncdu /path : interactive explore and sort by size. #ncdu
  - readlink -f <path> : print canonical absolute path (resolves symlinks). #readlink
  - ls -l : long format (look for leading 'l' for symlinks). #ls
- To list only symlinks in a directory:
  - find . -maxdepth 1 -type l -ls
  - or ls -l | grep '^l'  (quick heuristic). #symlink
- To remove a link safely:
  - unlink <symlink> or rm <symlink>
  - unlink <hardlink-name> removes that name; data remains if other hard links exist. #unlink
- When disk usage looks inconsistent:
  - Check df vs du: df shows filesystem-level free space; du sums directory usage — differences indicate other mounts, deleted-but-open files, reserved blocks, or sparse files. #df #du
- Use sudo when inspecting root-owned dirs: sudo du -sh /root

---

Keep this sheet nearby for fast lookup of command syntax, flags, and link behavior.