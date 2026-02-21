# Inodes & Directory Permissions (Linux) — Cheatsheet
#hashtags: #inode #directory #directory-entry #filesystem #permissions #access-control #chmod #link #hardlink #dot #dotdot #ls #chmod

---

## Key Definitions
- inode: Filesystem metadata object (permissions, owner, timestamps, pointers to data).
- directory inode: An inode whose data blocks contain directory entries (names + inode numbers).
- directory entry: Fixed-size record mapping a file name to an inode number.
- link (hard link): A directory entry (name) that references an inode; multiple links can reference same inode.
- link count: Number of directory entries (names) pointing to an inode; when 0 the inode is removed.
- dot (.): Directory entry pointing to the directory itself.
- dot-dot (..): Directory entry pointing to the parent directory.

---

## Formulas / Fixed Sizes / Notation
- Directory entry size = 16 bytes
- Directory entry layout (classic): first 2 bytes = inode number; remaining bytes = filename (component)
- Max component (filename) length = 14 characters
- Inode number field = 2 bytes ⇒ max inode id = 2^16 - 1 = 65535
- Permission bits numeric breakdown: rwx = 4 + 2 + 1
  - 7 = rwx, 6 = rw, 5 = rx, 4 = r, 0 = ---
- Example: chmod 755 dir ⇒ owner=7 (rwx), group=5 (r-x), others=5 (r-x)

---

## Key Concepts / Items
- #inode
  - Stores: permissions, ownership (UID/GID), timestamps, link count, pointers to data blocks.
- #directory
  - Represented by an inode whose data blocks store directory entries (name ↔ inode number).
- #directory-entry
  - 16 bytes each; maps filename (≤14 chars) to 2-byte inode number.
- #dot / #dotdot
  - Every directory contains "." (self) and ".." (parent) entries with inode numbers.
- #link / #hardlink
  - File names are links; multiple directory entries can reference the same inode.
  - Deleting a name decrements link count; inode removed only when count = 0.
- #permissions (for directories)
  - Read (r): list names (ls) — view entries only.
  - Write (w): create, delete, rename entries within the directory (subject to file perms).
  - Execute (x): traverse/access directory contents (cd, open files inside).
- #chmod
  - Command to change permissions; e.g., chmod 755 directory

---

## Important Properties / Invariants
- The only connection stored in a directory entry between name and contents is the inode number (first 2 bytes).
- Same inode can appear in multiple directories (hard links).
- Removing a directory entry does not remove the inode unless link count hits zero.
- Read without execute: can list names but cannot access/traverse contents.
- Execute without read: can traverse and access files if you know names, but cannot list directory contents.
- Write on directory allows create/delete/rename; to remove a file also requires write on directory and appropriate permissions on the file (depending on system policy).
- Proper permission setting is essential for confidentiality and integrity.

---

## Quick Reference (scannable)
- Directory entry (16 bytes)
  - Bytes 0–1: inode number (2 bytes)
  - Bytes 2–15: filename (≤14 chars)
- Common commands
  - View contents: ls
  - Change permissions: chmod 755 dir
- Permission effects (directory)
  - r = list (ls)
  - w = create/delete/rename entries
  - x = traverse (cd) and access contents
- Numeric permission mapping
  - 7 = rwx, 6 = rw-, 5 = r-x, 4 = r--, 0 = ---
- Typical safe default: avoid granting write to group/others; give execute only as needed.
- Link semantics
  - link count > 1: multiple names point to same inode
  - link count = 0: inode and data blocks reclaimed

---

Keep this sheet for quick lookup: inode structure facts, directory-entry layout, permission bit meanings, and the minimal commands/behaviors you’ll need during the exam.