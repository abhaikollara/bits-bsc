# Linux Links & Basic File Commands — Cheatsheet
#hashtags: #linux #bash #commands #ln #hardlink #symlink #inode #pwd #ls #filesystem #directory #file #file-management

---

## Key Definitions (one-line)
- ln: create a link (hard or symbolic) between files/directories. #ln  
- hard link: an additional directory entry pointing to the same inode/data blocks as the original file. #hardlink  
- symbolic link (symlink): a special file that stores a pathname referencing another file/directory. #symlink  
- inode: filesystem metadata structure representing a file’s data blocks and attributes (shared by hard links). #inode  
- pwd: print working directory — shows current absolute path. #pwd  
- ls: list directory contents. #ls

---

## Syntax / Quick Examples
- Create hard link: ln <source> <target>  
  Example: ln ./TWO/employee.txt emp
- Create symbolic link: ln -s <source> <target>  
  Example: ln -s ./TWO/employee.txt semp
- Print working directory: pwd
- List files: ls [options] [directory]  
  Example: ls -lha TWO

---

## Important Properties / Invariants
- Hard link:
  - Shares same inode as original → same data blocks and inode metadata (link count increases). #hardlink #inode
  - Modifying data via any hard link changes the same underlying file data.
  - Deleting one hard link removes one directory entry; file data remains until link count = 0.
  - Cannot (normally) cross filesystem boundaries (source and target must be same filesystem). #filesystem
  - Generally cannot create hard links to directories (restricted to avoid cycles).
- Symbolic link:
  - Is a separate file containing path to target; does not share inode/data blocks of target. #symlink
  - Can point across filesystems and to non-existent targets (dangling symlink).
  - If target is deleted, symlink becomes broken (dangling) and does not provide file data.
  - Modifying target via symlink affects original file (because symlink resolves to target at access time).
- ls and pwd:
  - pwd prints absolute path of current working directory.
  - ls shows directory entries; options change formatting and visibility.

---

## ls Options (quick reference)
- -l : long listing (permissions, owner, size, date, name). #ls  
- -a : show all files including hidden (dotfiles). #ls  
- -h : human-readable sizes (e.g., 1K, 2M). #ls  
- -t : sort by modification time (newest first). #ls  
- Combine: ls -lha -t

---

## Filesystem / Link Behavior Table

| Action | Hard Link | Symlink |
|---|---:|:---|
| Shares inode/data | Yes | No |
| Cross-filesystem | No | Yes |
| If target removed | Underlying data remains until all links removed | Symlink becomes dangling |
| Can link directories | Usually no | Yes (but can produce loops) |
| Creation command | ln src target | ln -s src target |

(#hardlink #symlink #filesystem)

---

## Quick Reference — One-page Rules
- Create hard link: ln source target → target is a new name for same inode. #ln  
- Create symlink: ln -s source target → target is a pointer file containing source path. #ln #symlink  
- Check current dir: pwd → prints absolute path. #pwd  
- List files: ls [dir]  
  - Use -l for details, -a for hidden, -h for human sizes, -t to sort by mod time. #ls  
- Deleting a link:
  - rm <hard-link-name> removes one directory entry; file data removed only when no links remain.
  - rm <symlink-name> removes the symlink only; target unaffected.
- To tell link types: ls -l → symlinks show “-> target”, hard links appear as regular files with same inode number (use ls -i to display inode). #inode

---

## Minimal Commands Checklist (copy into exam)
- ln src tgt        → create hard link
- ln -s src tgt     → create symbolic link
- rm linkname       → remove link (hard or symlink)
- pwd               → show absolute current directory
- ls -l -a -h -t dir → detailed listing (combine options)

---

Keep this sheet for quick lookup of #ln, #hardlink, #symlink, #pwd, and #ls behaviors and options.