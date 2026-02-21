# Linux File System Cheatsheet
#hashtags: #Linux #filesystem #partition #blockdevice #bootblock #superblock #inode #inodeTable #datablocks #mount #links #hardlink #softlink #symboliclink #permissions #rwx #chmod #umask #ls #stat #du #df #ncdu #stickybit #setuid #setgid #commands

---

## Title
Linux File System — layout, inodes, permissions, links, and common commands

---

## Key Definitions (one-line)
- File system: mechanism that organizes and manages files and directories on a storage device. #filesystem  
- Partition: logical section of a physical disk that can hold a file system. #partition  
- Block device: hardware device that transfers data in fixed-size blocks (HDD/SSD/CD). #blockdevice  
- Boot block: block(s) holding bootstrap code required for system boot. #bootblock  
- Superblock: file-system-level metadata (size, capacity, free space, owner). #superblock  
- Inode: unique metadata record for a file (inode number); does NOT contain filename or file data. #inode #inodeTable  
- Inode table: collection of all inode entries (UID, GID, size, timestamps, permissions, link count, pointers). #inodeTable  
- Data blocks: blocks that store the actual file contents. #datablocks  
- Mount: attach a file system to the directory tree so it’s accessible. #mount  
- Hard link: a directory entry that points to the same inode as the original file (same inode number). #hardlink  
- Soft (symbolic) link: a special file that points (path) to another file; has its own inode and can span file systems. #softlink #symboliclink  
- Link count: number of directory entries (hard links) pointing to an inode; when it reaches 0 (and not open), kernel frees data. #links  
- Permission bits (r/w/x): read, write, execute for user/group/others. #permissions #rwx  
- umask: default mask used at file/directory creation to remove permission bits from default mode. #umask  
- Sticky bit: directory-special permission preventing users from deleting/renaming files unless they own them (set by +t). #stickybit  
- setuid / setgid: special bits to run executable with file owner’s or group’s privileges. #setuid #setgid

---

## Formulas / Notation
- Default creation modes:
  - Files default: 666 (rw-rw-rw-) — execute cleared by default
  - Directories default: 777 (rwxrwxrwx)
- umask effect (correct formula): resulting_mode = default_mode & (~umask)
  - Example: default file 666 & ~022 = 644 (rw-r--r--)
  - Note: lecturer phrased as “remove bits” — do not treat as simple decimal subtraction.
- Octal to bits (binary → rwx):
  - 0 = --- (0) ; 1 = --x (1) ; 2 = -w- (2) ; 3 = -wx (3)
  - 4 = r-- (4) ; 5 = r-x (5) ; 6 = rw- (6) ; 7 = rwx (7)

---

## Key Concepts & Commands (quick bullets)
- Filesystem layout (4 parts): Boot block | Superblock | Inode list (table) | Data blocks. #bootblock #superblock #inode #datablocks
- Block devices listing:
  - lsblk (or blkid / cat /proc/partitions) — shows block devices and sizes. #blockdevice
- Find mounted file systems:
  - df -h — disk free per filesystem (human-readable). #df
  - stat -f -c %T . — prints FS type of current directory (example: ext4). #stat
- File metadata:
  - stat filename — detailed inode & timestamps, size, blocks, link count. #stat #inode
- ls -l layout: filetype+permissions | link count | owner | group | size | timestamp | name
  - Filetype letters: - regular, d directory, l symlink, b block dev, c char dev, p pipe, s socket. #ls
- Permission changes:
  - chmod [symbolic] user/group/other +/- r/w/x filename
  - chmod [octal] 644 filename  (user=6 rw-, group=4 r--, others=4 r--)
  - Examples:
    - chmod u+x file  (add execute for user)
    - chmod 764 file  (user=rwx group=rw- others=r--)
- umask:
  - Set with umask 022 (shell); affects new file/dir modes.
  - Interpret: umask bits are removed from default_mode. Example: umask 022 -> files 644, dirs 755. #umask
- Disk usage tools:
  - du -sh path — disk usage of files/dirs. #du
  - df -h — free space on filesystems. #df
  - ncdu — interactive curses-based disk usage navigator (scan/delete/sort). #ncdu
- Links:
  - Create hard link: ln source target  (same inode; cannot cross filesystems). #hardlink
  - Create symbolic link: ln -s target linkname  (separate inode; can cross filesystems; becomes dangling if target removed). #softlink #symboliclink
  - Remove a link: rm linkname or unlink linkname
  - Hard link behavior: link count increments; data freed only when link count = 0 (and no process holds it). #links
- Special permission bits:
  - setuid: chmod u+s file (executable runs with file owner privileges). #setuid
  - setgid: chmod g+s file (executable runs with file group privileges; on directories, new files inherit group). #setgid
  - sticky bit: chmod +t dir (on directories prevents deletion/rename by non-owners). #stickybit

---

## Important Properties / Invariants
- Inode does NOT contain filename or file data — directory entries map filename -> inode number. #inode #inodeTable
- A directory is a file that stores mappings of names → inode numbers. #filesystem
- Hard links = same inode number; soft links = separate inode pointing to a path. #hardlink #softlink
- Hard links cannot span filesystems; symbolic links can. #hardlink #softlink
- Deleting a directory entry removes a name; file data persists while link count > 0 (and while open by processes). #links
- ls -l permission string: first char = file type; next 9 chars = user/group/other (rwx groups). #ls

---

## Quick Reference (tables & snippets)

Permission octal → rwx
- 7 = rwx | 6 = rw- | 5 = r-x | 4 = r-- | 3 = -wx | 2 = -w- | 1 = --x | 0 = ---

Common ls -l examples:
- -rw-r--r-- 1 alice staff 1234 Feb 21 file.txt  → regular file, user=rw-, group=r--, others=r--

Common commands (one-liners)
- ls -l          — long listing (permissions, links, owner, size, time, name) #ls
- stat file      — inode, size, timestamps, link count, device, blocks #stat
- df -h          — filesystem disk free/used #df
- du -sh dir     — size of dir (summarized) #du
- ncdu           — interactive disk usage navigator #ncdu
- chmod 644 f    — set permissions using octal #chmod
- chmod u+x f    — add execute for user #chmod
- umask 022      — set default mask (typical) #umask
- ln src tgt     — create hard link #hardlink
- ln -s tgt link — create symbolic link #softlink
- unlink link    — remove a link #commands
- rm file        — remove file (deletes directory entry; data freed when linkcount=0 & not open) #commands
- mv / cp / mkdir / pwd — standard file ops #commands

umask calculation examples
- File default 666, umask 022 → 666 & ~022 = 644 (rw-r--r--)
- Dir default 777, umask 002 → 777 & ~002 = 775 (rwxrwxr-x)

File type letters (ls -l first char)
- - regular file
- d directory
- l symlink
- b block device
- c character device
- p named pipe (FIFO)
- s socket

Link-count & delete quick facts
- Hard link creation: link count increments.
- Deleting one name: only removes that directory entry; other hard links still access file.
- Data is freed when link count reaches 0 (and no process holds the file open).

---

Keep this sheet near your notes: use hashtags to quickly search topics (#inode, #permissions, #umask, #hardlink, #softlink, #du, #df, #ncdu). Good luck on the open-book exam!