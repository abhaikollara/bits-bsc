# Inodes & Linux File System Layout — Cheatsheet

Keywords: #inode #filesystem #Linux #Unix #superblock #bootblock #inodetable #datablocks #directory #hardlink #permissions #UID #GID #timestamps #blockpointers #partition #MBR

---

## Key Definitions
- inode: index node — metadata record for a file (excludes file name and file data).
- inode number: unique identifier for a file within a filesystem.
- inode table/list: collection of all inode records in a filesystem.
- data block: disk block that contains actual file contents.
- block pointer: pointer(s) in an inode that reference data blocks.
- superblock: metadata describing the filesystem state (size, free blocks, inode info).
- boot block (MBR in disk): first sector that holds bootstrap code and partition info.
- directory file: maps filenames → inode numbers (holds name→inode entries).
- hard link: directory entry that points to an inode; multiple hard links share one inode.
- UID / GID: file owner (user id) and group id stored in inode.
- timestamps: access (atime), modification (mtime), change (ctime) stored in inode.

---

## Formulas / Notation
- File identity: (filesystem_ID, inode_number)
- Typical timestamp set: {atime, mtime, ctime}
- Directory minimum links: links ≥ 2 ('.' points to self, '..' points to parent)
- Allocation rule: Each allocated data block → belongs to exactly one file

---

## Key Algorithms / Concepts
- #inode lookup sequence:
  - filename → directory entry → inode number → inode record → block pointers → data blocks
- #ls commands to view inode:
  - ls -i or ls -li → show inode numbers in directory listing
- #file-metadata stored in inode:
  - type, permissions, owner (UID), group (GID), size, timestamps, link count, block pointers
- #filesystem-layout (high-level order in a partition):
  - Boot block (MBR) → Superblock → Inode list/table → Data blocks
- #block-allocation invariant:
  - Partial-block slack is not shared — a block is owned by a single file

---

## Important Properties / Invariants
- Inode does NOT store filename(s) — name→inode mapping lives in directories. (#directory)
- One inode per filesystem object (file or directory). (#inode)
- Multiple filenames (hard links) can map to the same inode; inode holds link count. (#hardlink)
- Directories always have at least two links: '.' and '..'. (#directory)
- Data blocks referenced by an inode contain actual content; inode stores block pointers. (#datablocks #blockpointers)
- Superblock tracks filesystem capacity, free block list, next free index, inode count/free inodes. (#superblock)
- Each allocated data block is exclusive to one file even if not fully filled. (#datablocks)

---

## Quick Reference (Scannable)
- Show inode numbers: ls -i | ls -li
- File identity: use (filesystem_ID, inode_number)
- Inode contains: {type, perms, UID, GID, size, atime, mtime, ctime, link_count, block_pointers}
- Directory ↔ inode mapping: directory entries = (name → inode_number)
- Partition filesystem layout:
  - Boot block (bootstrap/MBR)
  - Superblock (fs metadata & free lists)
  - Inode list/table (inode records)
  - Data blocks (file contents)
- Directory links: '.' = self, '..' = parent (hence links ≥ 2)
- Deallocation rule (exam-relevant): free blocks/inodes tracked by superblock; blocks not shared among files

---

Tags (major concepts): #inode #filesystem #superblock #bootblock #inodetable #datablocks #directory #hardlink #permissions #UID #GID #timestamps #blockpointers #MBR

--- 
(Use this sheet to quickly locate: what an inode holds, how names map to inodes, and the on-disk layout order.)