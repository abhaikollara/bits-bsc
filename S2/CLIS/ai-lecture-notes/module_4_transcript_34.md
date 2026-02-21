# File Systems: Superblock, Inodes, and Links — Cheatsheet

Keywords: #filesystem #superblock #inode #inodes #hardlink #symlink #symboliclink #links #metadata #Linux #data-storage #ln #ls #stat

---

## Key Definitions
- File system (#filesystem): Structures and rules for organizing, storing, and retrieving files on a storage device.
- Superblock (#superblock): File-system metadata block that stores global FS parameters and integrity info (size, block count, inode count, flags).
- Inode (#inode): Per-file metadata structure describing a file/dir (ownership, permissions, timestamps, size, block pointers).
- Hard link (#hardlink): Directory entry that references the same inode as another name (same inode number).
- Symbolic (soft) link (#symlink #symboliclink): Special file that stores a pathname reference to another file.
- Metadata (#metadata): Data about files (permissions, owner, size, timestamps, pointers) stored in superblock & inodes.

---

## Formulas / Equations
- Blocks required for a file: blocks = ceil(file_size / block_size)
- Generic max file size via inode pointers:
  max_size ≈ (D + S * P + Dbl * P^2 + Trp * P^3) * block_size
  - D = number of direct pointers
  - S/Dbl/Trp = 1 if single/double/triple indirect present (or counts of pointers)
  - P = pointers per block = block_size / pointer_size
  (Used to compute limits for inodes with direct/indirect pointers.)
- free_space = total_blocks - used_blocks (tracked in superblock/bitmaps)

---

## Key Concepts / Items (#hashtags included)
- Purpose of a file system (#filesystem): organize data, provide names/paths, manage free space, enforce permissions.
- Superblock (#superblock):
  - Stores FS-wide metadata: total size, block size, inode count, free block/inode counters, mount state, FS type, UUID.
  - Critical for integrity (fsck may use alternate superblocks).
- Inodes (#inode):
  - Contain metadata (mode, uid/gid, timestamps), link count, size, and pointers to data blocks (direct and indirect).
  - Directory entries map filenames → inode numbers.
  - Link count in inode indicates number of directory entries pointing to it.
- Links (#hardlink #symlink):
  - Hard link: another directory entry pointing to same inode (same data); link count increments; cannot span filesystems; usually cannot link directories.
  - Symbolic link: a separate inode containing a path string; can point across filesystems; can be dangling.
- Creating links (#ln #ln -s):
  - Hard link: ln target linkname
  - Symbolic link: ln -s target linkname
- Inspecting inodes and links (#ls #ls -i #stat):
  - ls -i shows inode number
  - stat filename shows inode metadata and link count
- Superblock recovery (#fsck): filesystem check utilities use superblock/alternate copies to repair metadata.

---

## Important Properties / Invariants
- Inode uniqueness: each inode is unique; filenames are directory entries mapping to inode numbers.
- Link count consistency: inode.link_count == number of directory entries pointing to that inode.
- Hard links share the same inode and data blocks; deleting one name decrements link count, data freed only when link count hits 0 and no open file handles exist.
- Symbolic links contain a pathname; resolution occurs at path traversal time.
- Superblock is essential: corrupted superblock can render FS unusable; alternate superblocks (if present) are backups.
- Directories are special files that map name → inode; modifying directory entries updates inode link counts.

---

## Quick Reference (scannable)
- Commands:
  - Create hard link: ln <target> <linkname>  #hardlink #ln
  - Create symlink: ln -s <target> <linkname>  #symlink #ln
  - Show inode number: ls -i <file>  #ls
  - Show inode metadata: stat <file>  #stat
  - Check/repair FS: fsck /dev/xxx  #fsck #superblock
- Hard vs Soft Links (quick table):

  | Property | Hard Link (#hardlink) | Symbolic Link (#symlink) |
  |---|---:|---|
  | References inode directly | Yes | No (stores path) |
  | Cross-filesystem | No | Yes |
  | Can point to directories | Usually no | Yes |
  | Can be dangling | No | Yes |
  | Shares inode number | Yes | No |

- Typical inode fields to expect: inode_number, mode (type+perm), uid/gid, size, atime/mtime/ctime, link_count, block_pointers.
- Calculating required blocks: blocks = ceil(file_size / block_size).
- Common problems to remember:
  - Dangling symlink: target removed → symlink broken.
  - Orphan inode (link_count = 0 but allocated): recovered by fsck if unreferenced.
  - Superblock corrupt: use backup/alternate superblock when available.
- Use ls -li to display inode and long listing in one view.

---

Keep this sheet near your exam materials for quick lookup of #superblock, #inode, and link behavior in #Linux file systems.