# Linux Links Cheatsheet — Symbolic (Soft) vs Hard Links

#hashtags
#symbolic_link #soft_link #symlink #hard_link #inode #readlink #ln #ls #filesystem #dangling_link #symlink_chain #directory_entry #permissions #rm

---

## Key Definitions
- Symbolic link (symlink / soft link): a file that stores a path pointer to another file or directory.
- Hard link: an additional directory entry that references the same inode (same data) as the original file.
- Inode: filesystem metadata structure identifying file contents and attributes (st_nlink = link count).
- Dangling link: a symlink whose target path does not exist.
- Absolute path: full path from filesystem root (e.g., /home/user/dir/file).

---

## Commands / "Formulas"
- Create hard link: ln <target> <linkname>
- Create symbolic link: ln -s <target> <linkname>
- List long format (shows links): ls -l
- Show symlink target or resolved path: readlink <symlink>
- Resolve to final absolute path (follow chain): readlink -f <symlink>
- Remove file: rm <file> (affects entries/inode as below)

Filesystem/link relations:
- st_nlink = number of hard links to an inode
- File blocks freed when (st_nlink == 0) AND no process has it open

---

## Key Concepts
- #symlink points to a path string; can point to files or directories; can cross filesystems.
- #hard_link points to the same inode (same file contents/metadata); cannot span filesystems; typically cannot link directories.
- #readlink -f resolves symlink chains until it reaches a non-link file and prints absolute path.
- #ls -l displays symlinks with "-> target" and shows file types/colors (symlink often blue).
- Deleting the original file:
  - For #hard_link: other hard links still access the data (inode persists while st_nlink>0).
  - For #symlink: symlink becomes a #dangling_link if target removed.
- Permissions:
  - Symlink has its own directory entry and mode but not meaningful file permissions for target access; access controlled by target permissions.
  - Hard links share the same inode permissions; changing permissions affects all hard links.
- Operations on hard links (write/chmod) affect same underlying data.
- Symlink can form a chain (symlink -> symlink -> ... -> file); readlink -f follows chain.

---

## Important Properties / Invariants
- Hard links: multiple directory entries -> single inode; st_nlink increments per hard link.
- Symlinks: point to path string; no st_nlink increment on target.
- Deleting a filename removes a directory entry; only when inode link count reaches zero and no open descriptors are left are blocks freed.
- Symlinks are lightweight pointers — can become invalid if target moved/removed.
- Hard links cannot reference directories (to avoid cycles) and cannot cross filesystem boundaries.
- readlink -f resolves all symlinks in path and returns an absolute path or nothing if final target missing.

---

## Quick Reference (scannable)
- Create:
  - Hard: ln file.txt hl
  - Soft: ln -s /path/to/file.txt sl
- Inspect:
  - ls -l -> shows "name -> target" for symlink
  - readlink sl -> print symlink target (relative/path)
  - readlink -f sl -> print final absolute path, following any symlink chain
- Effects of rm file.txt:
  - Hard link hl remains usable (data intact)
  - Symlink sl becomes dangling (points to removed path)
- When to use:
  - Use #symlink when you need pointer across filesystems or to directories or want an easily-updated path pointer.
  - Use #hard_link when you want another indistinguishable directory entry to the same file data (same inode).
- Limitations:
  - Hard links: no directories, no cross-filesystem
  - Symlinks: can be dangling, stores path not inode
- Permissions:
  - chmod on inode affects all hard links
  - chmod on symlink typically affects target (or is ignored) — check system semantics

---

## Mini Comparison Table

| Feature | #symbolic_link (symlink) | #hard_link |
|---|---:|---:|
| Points to | path string | inode (same data) |
| Cross-filesystem | Yes | No |
| Can link dirs | Yes | Typically No |
| Affected by target deletion | Becomes dangling | Still usable |
| ls -l shows target | Yes (->) | No |
| readlink -f useful | Yes (resolves chain) | N/A |

---

Keep this as a quick lookup: ln/ln -s to create, ls -l and readlink/readlink -f to inspect, remember symlink stores path (can break), hard link shares inode (same file).