# Linux filesystems & I/O cheatsheet
#keywords: #inode #filesystem #filedescriptor #open #read #write #close #fcntl #strace #lsof #tmpfs #dd #dup #dup2 #dumpe2fs #debugfs #ulimit #O_NONBLOCK #inode-table #superblock

---

## Title
Linux filesystem internals, inodes, file deletion, file descriptors & sysadmin tools

---

## Key Definitions (one-line)
- inode: unique numeric descriptor for a file (stores metadata & block pointers, NOT the filename) #inode
- directory entry: mapping (filename ↔ inode number) stored in a directory #directory
- inode table: filesystem structure storing inode metadata (link count, block pointers, timestamps, etc.) #inode-table
- data block: disk block(s) storing the actual file content #datablock
- hard link: directory entry that points to an inode; increases inode link count #hardlink
- file descriptor (FD): non-negative integer handle the OS gives a process to reference an open file/device #filedescriptor
- open file / open file table: kernel structures representing an opened file (FD -> open-file-entry -> inode) #openfile
- superblock: filesystem-wide metadata (total inodes, blocks, block size, mount info) #superblock
- tmpfs: in-memory temporary filesystem (volatile, fast, shrinks/grows with RAM) #tmpfs
- non-blocking I/O: file/FD mode allowing I/O calls to return immediately if they would block (O_NONBLOCK) #O_NONBLOCK

---

## Formulas / Notation / Quick facts
- reserved FDs: 0 = stdin, 1 = stdout, 2 = stderr (first user-assigned FDs start at 3) #stdin #stdout #stderr
- dd syntax (common): dd if=<input> of=<output> bs=<blocksize> status=progress  #dd
- dup(2) / dup2(2) syscall patterns:
  - newfd = dup(oldfd)        — duplicate to lowest unused FD #dup
  - dup2(oldfd, newfd)       — duplicate into specific newfd (closes newfd first if open) #dup2
- fcntl usage: flags = fcntl(fd, F_GETFL); fcntl(fd, F_SETFL, flags | O_NONBLOCK)  #fcntl #O_NONBLOCK

---

## Key Algorithms / Concepts (bulleted)
- Path resolution → inode (component-wise):
  - start at root (inode e.g. 2), split path into components, for each component: lookup directory entry → get inode number → read inode → continue. #path-resolution #inode
- File deletion flow:
  - remove directory entry (filename → inode mapping)
  - decrement inode link count
  - if link count > 0 → inode/data remain
  - if link count == 0 and no open references → free inode and free data blocks (made available for reuse)
  - if file still open by process → free delayed until last reference closed/exited #file-deletion
- Data recovery implication:
  - deletion frees blocks but does not zero them; data persists until overwritten (possible recovery until overwritten). #data-recovery
- FD lifecycle:
  - open() returns FD; use read()/write() with FD; close(fd) releases FD back to kernel.limit. #open #read #write #close
- Duplicating FDs:
  - dup/dup2 let one open file be referenced by multiple FDs (useful to redirect stdout/stderr to files or pipes). #dup #dup2
- fcntl and O_NONBLOCK:
  - use fcntl to get/set flags (non-blocking I/O, advisory locks, etc.); O_NONBLOCK enables async-style behavior (no waiting on read/write). #fcntl #O_NONBLOCK
- tmpfs:
  - stores files in RAM, fast, volatile (data lost on reboot), useful for temp data / caches. #tmpfs

---

## Important Properties / Invariants
- Filenames live in directories; inodes do not contain the filename. #inode
- Multiple directory entries (hard links) can reference the same inode; inode has a link count. #hardlink
- Inode numbers and data blocks are reused after being freed (no guarantee of uniqueness over time). #inode-reuse
- A file is only truly freed when link count == 0 AND no process has it open. #file-lifecycle
- FD numbers are per-process and small integers (0..); kernel maps FDs to open-file structures. #filedescriptor
- tmpfs uses RAM: fast but limited and volatile (risk of memory pressure). #tmpfs

---

## Common syscalls / commands (quick ref)
- Syscalls (C / kernel): open(), read(), write(), close(), dup(), dup2(), fcntl()  #open #read #write #close #dup #dup2 #fcntl
- strace: strace -e trace=open,close,read,write <cmd> (trace syscalls & signals) #strace
- lsof: list open files (filter by PID, user, path, port) #lsof
- ulimit: show/set per-shell resource limits (max file size, open files, stack, etc.) #ulimit
- dd: low-level copy/clone disks & partitions — dd if=/dev/sdX of=image.img bs=4M status=progress  #dd
- dumpe2fs: sudo dumpe2fs /dev/xxx or dumpe2fs <mountpoint> — dump ext* filesystem superblock info #dumpe2fs
- debugfs: interactive debugging of ext* FS (dangerous; admin use only) #debugfs
- watch: watch -n <secs> <command> — continuously run and display command output (e.g., watch -n2 df -h) #watch
- df -h: show filesystem usage (type column shows fs type like ext4, tmpfs, xfs, btrfs, zfs) #df

---

## Quick Reference (scannable)
- FD reserved: 0=stdin, 1=stdout, 2=stderr; user FDs start ≥3 #stdin #stdout #stderr
- Delete file steps: remove dir entry → link_count-- → if link_count==0 && no open refs → free data blocks + free inode #file-deletion
- Recoverability: data recoverable until overwritten (blocks are freed but not zeroed) #data-recovery
- Duplicate FD: dup(oldfd) → lowest unused FD; dup2(oldfd,newfd) → force newfd to refer to oldfd #dup #dup2
- Make FD non-blocking:
  - flags = fcntl(fd, F_GETFL)
  - fcntl(fd, F_SETFL, flags | O_NONBLOCK) #fcntl #O_NONBLOCK
- tmpfs: fast, volatile, uses RAM; good for temp/caches; data lost on reboot; watch memory usage #tmpfs
- dd common template: dd if=<source> of=<dest> bs=<blocksize> status=progress (use carefully) #dd
- View filesystem superblock: sudo dumpe2fs <device|mountpoint>  #dumpe2fs
- Trace syscalls: strace -o trace.txt -e trace=open,close,read,write <cmd>  #strace
- List open files: lsof -p <PID>  OR lsof +D <directory>  #lsof
- Monitor FS usage: watch -n 2 df -h  or watch -n 2 'dumpe2fs ...' (admin) #watch

---

## Filesystems to remember
- ext4: common Linux filesystem (superblock, journaling) #ext4
- xfs: high-performance, scalable for large filesystems #xfs
- btrfs: copy-on-write, snapshots, multi-device #btrfs
- zfs: advanced features, checksums, snapshots, pooling (not native everywhere) #zfs
- tmpfs: in-memory temporary fs (volatile) #tmpfs

---

Keep this cheat sheet handy for quick lookups on path→inode resolution, deletion semantics, FD rules, and the admin commands (strace / lsof / dumpe2fs / debugfs / dd / watch / ulimit).