# Linux filesystems — Data blocks & inodes (cheatsheet)

Keywords: #inode #datablock #filesystem #linux #unlink #rm #rmdir #df #debugfs #watch #allocation #extent #blockmap #monitoring #freeing

## Key Definitions
- inode: Metadata structure for a file/dir (permissions, timestamps, size, pointers to data blocks). #inode
- data block: Unit where file contents are stored on disk. #datablock
- block allocation map: Bitmap/structure tracking free/used blocks. #blockmap
- extent-based allocation: Stores ranges (extents) of contiguous blocks for a file. #extent
- unlink: Remove a directory entry (name) that points to an inode; decreases link count. #unlink
- rm/rmdir: User commands to remove files (`rm`) or empty directories (`rmdir`). #rm #rmdir
- df: Show filesystem disk usage; `df -i` shows inode counts. #df
- debugfs: Low-level interactive tool to inspect ext filesystems (inodes/blocks). #debugfs
- watch: Re-run a command periodically (default every 2s). #watch

## Formulas / Equations
- inode usage % = (used_inodes / total_inodes) * 100
- free_inodes = total_inodes − used_inodes
- file deletion condition for freeing blocks:
  - Data blocks freed when (link_count == 0) AND (no process has file open).

## Key Algorithms / Concepts
- #Allocation strategies
  - Block allocation map: track each block (free/used) via bitmap/lists.
  - Extent-based allocation: allocate contiguous block ranges for efficiency. #extent
- #Assignment
  - New file/dir -> allocate an inode; assign data blocks as needed for content.
- #Freeing
  - Deleting/unlinking a name marks its directory entry removed; inode may be freed and blocks reclaimed when link count and open-file conditions permit.
- #Monitoring
  - Regularly check `df -h` and `df -i` (inodes) to avoid running out of space or inodes. #monitoring
- #Debugging
  - Use `debugfs` to inspect inode/block internals and run `stat <inode>` on device. #debugfs

## Important Properties / Invariants
- One inode per file/directory; inodes contain pointers to data blocks. #inode
- A file needs an inode always; data blocks needed only if size > 0 (depends on FS). #datablock
- Deallocation is reclaimable: free inodes/blocks are reusable by filesystem.
- Removing a directory:
  - `rmdir` for empty dir
  - `rm -r` for recursive removal of non-empty dir. #rmdir #rm
- Link count (inode.nlink) controls when inode/blocks can be freed (and open file handles delay freeing).
- `df -i` shows inode exhaustion risk even when disk space remains. #df

## Quick Reference (scannable)

Commands
- unlink file
  - Syntax: `unlink <filename>` — removes one directory entry (decrements links). #unlink
- rm file
  - Syntax: `rm <filename>` — remove file (wrapper that typically calls unlink); `rm -r <dir>` recursive. #rm
- rmdir directory
  - Syntax: `rmdir <directory>` — remove only empty directory. #rmdir
- df (disk usage)
  - Show disk space: `df -h`
  - Show inode usage: `df -i` — outputs total, used, free, %iused. #df
  - Example (from lecture): total inodes = 494,328; used = 2; ~1% used.
- debugfs (inspect ext fs internals)
  - Syntax: `debugfs -R "stat <inode>" /dev/sda1` — run command and exit. #debugfs
  - Use for reading inode metadata, block pointers, extents.
- watch (monitor repeatedly)
  - Syntax: `watch df -i` — runs `df -i` every 2 seconds (default). #watch
  - Useful to observe inode/disk changes live.

Quick checks
- To see inode shortage risk: run `df -i` and check %iused.
- To monitor in real time: `watch -n 2 "df -h; df -i"`
- To inspect a suspected corrupted / inconsistent inode: `debugfs -R "stat <inode>" /dev/<device>`

Notes to remember (short)
- Deleting a file name does not immediately free blocks if link_count > 0 or the file is open. #unlink
- Always monitor both space and inodes; running out of inodes prevents creating new files even if space exists. #monitoring
- Extent allocation reduces fragmentation for large files. #extent

(tags used in this cheatsheet: #inode #datablock #filesystem #linux #unlink #rm #rmdir #df #debugfs #watch #allocation #extent #blockmap #monitoring #freeing)