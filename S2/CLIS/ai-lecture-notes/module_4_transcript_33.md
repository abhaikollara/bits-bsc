# Inode — Linux file metadata structure (cheatsheet)

Keywords: #inode #filesystem #metadata #permissions #timestamps #links #direct-blocks #indirect-blocks #ACL #extended-attributes #immutable #generation-number #file-size

---

## Key Definitions
- inode: #inode — data structure representing a file/directory’s metadata (not the filename).
- file mode / permissions: #permissions — bits encoding file type + owner/group/others read/write/execute.
- owner ID / group ID: #uid #gid — numeric user and group identifiers.
- file size: #file-size — size of file contents in bytes.
- atime: #atime — last access time (read).
- mtime: #mtime — last content modification time (write).
- ctime: #ctime — last inode metadata change (permissions, ownership, link count).
- links count: #links — number of hard links referencing the inode.
- direct block pointers: #direct-blocks — pointers from inode directly to data blocks (for small files).
- indirect block pointers: #indirect-blocks — single/double/triple indirection to reach more data blocks.
- extended attributes: #extended-attributes — extra attributes/flags (e.g., compression, immutable).
- ACL: #ACL — access control list entries stored/pointed to by inode where supported.
- generation number: #generation-number — unique id to avoid accidental inode reuse.
- filesystem-specific data: #fs-specific — reserved space for FS-specific extensions.

---

## Formulas / Equations
- Permission string format: rwx rwx rwx → owner / group / others (#permissions).
- Indirection capacity (blocks):
  - Let ND = number of direct pointers, P = pointers per block (block_size / pointer_size).
  - Addressable blocks ≈ ND + P + P^2 + P^3  (#direct-blocks #indirect-blocks)
- Max file size (approx):
  - max_file_size ≈ (ND + P + P^2 + P^3) × block_size  (#file-size)
- Inode free condition:
  - if (links_count == 0 AND no process has file open) → inode and data blocks reclaimed (#links).

---

## Key Algorithms / Concepts
- #Direct-vs-Indirect:
  - Direct pointers: fast access for small files.
  - Single indirect: inode → block of pointers → data blocks.
  - Double indirect: inode → block of pointers → block of pointers → data blocks.
  - Triple indirect: one more level for very large files.
- #Hard-link semantics:
  - Hard links share same inode; directory entries map names → inode numbers; inode holds link count.
- #Filename-vs-inode:
  - Directory entries map filenames to inode numbers; inode itself does NOT store filename.
- #Timestamps management:
  - atime/mtime/ctime maintained in inode; OS policies may modify atime updates for performance (e.g., relatime).
- #Extended-attributes / #ACL:
  - Inode may contain pointers or inline space for ACL entries and security contexts (e.g., POSIX ACL, SELinux).
- #Immutable-flag:
  - Immutable prevents modifications regardless of write permissions; controlled via inode flags.

---

## Important Properties / Invariants
- Inode does not include filename; directories map names → inode numbers. (#inode)
- Link count counts hard links only; soft (symbolic) links are separate filesystem entries. (#links)
- ctime ≠ mtime: ctime changes on metadata changes (permissions, owner, link count); mtime on content write. (#ctime #mtime)
- atime updated on reads (may be disabled/relatime for performance). (#atime)
- When link count reaches 0 and the file is not open, inode + blocks are freed. (#links)
- Mode bits include file type + owner/group/other permission bits (rwx). (#permissions)
- Filesystem may add FS-specific inode fields (compression, extended features). (#fs-specific)
- Generation number protects NFS/clients from inode number reuse issues. (#generation-number)

---

## Quick Reference
- Mode representation examples: 
  - rwxr-xr-- → owner=rwx (7), group=rx (5), others=r (4). (#permissions)
- Timestamp meanings:
  - atime = last read; mtime = last content write; ctime = last metadata change. (#atime #mtime #ctime)
- Link behavior:
  - ln (hard): increments inode.links; unlink/deleting a name decrements links.
  - rm removes directory entry; actual data freed only when links==0 and no open fds. (#links)
- Block addressing order (common):
  - use direct pointers → single indirect → double indirect → triple indirect. (#direct-blocks #indirect-blocks)
- Common inode fields (compact list):
  - mode, uid, gid, size, atime, mtime, ctime, links_count, block pointers, flags, generation, ACL ptrs, fs-specific. (#inode)
- Immutable vs mutable:
  - immutable flag set → no writes/rename/permission changes allowed even if owner writable. (#immutable)
- ACL/SEC:
  - POSIX ACL entries referenced by inode; security context may be stored in inode xattrs. (#ACL #extended-attributes)

---

Keep this sheet for quick lookup of inode fields, permissions, timestamp semantics, and block addressing limits.