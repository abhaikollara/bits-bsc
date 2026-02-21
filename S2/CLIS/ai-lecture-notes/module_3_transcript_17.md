# Linux Inode & Links — Cheatsheet
#hashtags: #inode #filesystem #stat #du #df #blocks #direct #indirect #single-indirect #double-indirect #triple-indirect #permissions #ownership #timestamps #hardlink #symlink #symboliclink #filetype #extendedattributes

---

## Key Definitions (one-line)
- inode: On-disk structure holding a file's metadata (not filename or directory entry). #inode  
- stat: Command that displays an inode's metadata for a file. #stat  
- block: Allocation unit on disk; default unit referenced here = 512 bytes. #blocks  
- direct block pointer: Inode pointer that directly references a data block. #direct  
- indirect block pointer: Pointer to a block that contains more pointers to data blocks. #indirect  
- single/double/triple indirect: 1/2/3 levels of pointer indirection to reach data blocks. #single-indirect #double-indirect #triple-indirect  
- hard link: Directory entry that references the same inode (same data) as another name. #hardlink  
- symbolic (soft) link: Separate file whose contents are a path that references another file or dir. #symlink #symboliclink  
- permissions (file mode): Read/write/execute bits for owner, group, others. #permissions  
- ownership: UID and GID stored in inode. #ownership  
- timestamps: atime (access), mtime (modify data), ctime (change metadata), birth (creation). #timestamps  
- extended attributes: Extra metadata attached to file (security/user data). #extendedattributes  
- generation number: FS-specific number tracking inode changes. #generationnumber  
- fragment block: Old FS scheme: block holding fragment pointers (fragmentation). #fragmentblock

---

## Formulas / Equations
- blocks_used = ceil(file_size / block_size)  
  - Example (transcript): block_size = 512 bytes → 4096 bytes uses 8 blocks. #blocks  
- du -k: block unit = 1024 bytes (kilobyte units). #du #blocks  
- df -H: human-readable with powers of 1000; df -h: human-readable with powers of 1024. #df

---

## Key Algorithms / Concepts (bulleted)
- Inode structure (fields) — #inode
  - file mode & type (regular/dir/symlink/special) #filetype #permissions
  - ownership: UID, GID #ownership
  - file size (bytes) #blocks
  - timestamps: atime, mtime, ctime, birth #timestamps
  - link count (# of hard links) #hardlink
  - block pointers: direct + single/double/triple indirect #direct #indirect
  - file flags, extended attributes, generation number, FS id, fragment pointers #extendedattributes #generationnumber
- Pointer levels — #direct #single-indirect #double-indirect #triple-indirect
  - Direct: inode -> data block
  - Single indirect: inode -> block of pointers -> data blocks
  - Double indirect: inode -> block -> block of pointers -> data blocks
  - Triple indirect: three levels of pointer blocks -> data blocks
- Hard links — #hardlink
  - ln source-file link-name
  - multiple directory entries reference same inode/data; deleting one name does not remove data until link count = 0
  - cannot link to directories (typical) and must remain on same filesystem
- Symbolic links — #symlink
  - ln -s source-file link-name
  - separate inode containing path; can point across filesystems; broken/dangling if target removed
- stat command — #stat
  - stat filename → shows size, allocated blocks, type, device (hex), inode number, link count, timestamps, birth time, etc.
- du command (disk usage) — #du
  - du reports per-file/directory allocated blocks (based on file size)
  - du -a : list every file's disk usage (individual files) #du  
  - du -k : show block counts in 1024-byte units (kilobytes) #du  
  - du -i : (lecture) allocates blocks evenly among links #du  
  - du -l : (lecture) represents blocks evenly among links #du  
  - du -s : show total for specified files/directories (summary) #du
- df command (filesystem free space) — #df
  - df shows free/used space on mounted filesystems (per-FS overview)
  - df -h : sizes human-readable (binary 1024) #df  
  - df -H : human-readable powers of 1000 (decimal) #df  
  - df -M : show blocks in megabytes #df  
  - df -i : show inode usage (IUsed, IFree) #df  
  - df -T : show filesystem types #df
  - df /boot : display info for mounted /boot filesystem example

---

## Important Properties / Invariants
- Inodes hold metadata, not filenames; directory entries map names → inode numbers. #inode  
- Hard links share inode and data: changes to content via any hard link affect the same data; inode link count tracks how many names exist. #hardlink  
- Symbolic links are independent files with their own inode; they store a pathname and do not share data blocks with target. #symlink  
- Direct pointers are fastest; indirect pointers allow large files at expense of extra indirection. #direct #indirect  
- Deleting a file removes a directory entry; data freed only when inode link count = 0 and no processes have it open. #inode  
- du reports disk allocation (blocks), not necessarily exact file size (sparse files, fragmentation). #du  
- df reports filesystem-level free/used capacity; df -i reports inode exhaustion (can run out of inodes even if space remains). #df

---

## Quick Reference (scannable)
Commands / Syntax:
- stat filename                     → show inode metadata (#stat)  
- ln source-file link-name          → create hard link (#hardlink)  
- ln -s source-file link-name       → create symbolic link (#symlink)  
- du [options] file/dir             → disk usage (#du)  
  - -a : list all files  
  - -k : use 1024-byte units  
  - -i : (lecture) allocate blocks evenly among links  
  - -l : (lecture) represent blocks evenly among links  
  - -s : summary (total)  
- df [options] [mountpoint]         → filesystem usage (#df)  
  - -h : human-readable (1024)  
  - -H : human-readable (1000)  
  - -M : megabyte units  
  - -i : show inodes  
  - -T : show filesystem type

Units & Examples:
- Default block unit (transcript): 512 bytes → blocks = ceil(size / 512) #blocks  
- Example: 4096 bytes = 8 blocks at 512 B block size.  
- du -k uses 1024-byte blocks (kilobytes). #du

Inode Fields (short list):
- file type & mode, uid/gid, size, link count, device id, inode number, block pointers, atime/mtime/ctime/birth, file flags, xattrs, generation, fs id, fragment pointers. #inode

Hard vs Soft (at-a-glance):
- Hard link: same inode, same data, cannot cross filesystems, cannot usually point to directories. #hardlink  
- Symlink: separate inode, stores target path, can cross FS, can be dangling after target deletion. #symlink

Notes:
- Color coding of files/links depends on terminal/LS_COLORS and distro (lecture noted colors may vary).  
- Stat and du refer to allocated blocks (not logical size for sparse files). #stat #du

---

End of cheatsheet — concise listing for quick lookup during exam.