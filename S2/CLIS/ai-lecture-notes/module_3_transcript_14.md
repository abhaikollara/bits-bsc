# Linux Files & Directories — Cheatsheet
#hashtags: #Linux #filesystem #inode #partition #disk #root #paths #directories #permissions #commands #dev #home #bin #usr #var #lib #tmp #sbin #absolute-path #relative-path

---

## Title
Linux file system basics — hierarchy, paths, partitions, inodes, key directories & commands

---

## Key Definitions (one-liners)
- File: Persistent collection of data (text, binary, image, program). #File  
- Directory (folder): Special file that contains entries (files/dirs). #Directory  
- File path: Textual location of a file/dir in the hierarchy. #Path  
- Absolute path: Path starting at root "/" (full path). #AbsolutePath  
- Relative path: Path starting from current working directory. #RelativePath  
- Root directory: Top-level directory, represented by "/". #Root  
- Partition: Group of contiguous cylinders treated as an independent disk region. #Partition  
- Block device: Storage device exposing fixed-size blocks (disks). #BlockDevice  
- Sector: Smallest addressable unit on a disk (often 512B/4KB). #Sector  
- Track: Circular track on a disk platter. #Track  
- Cylinder: Set of tracks at same radius across all platters. #Cylinder  
- Partition table: Index mapping disk sections to partitions. #PartitionTable  
- Inode: File metadata record (permissions, owner, times, size, block addresses, inode number). #Inode

---

## Formulas / Notation / Mappings
- Disk composition: sector(s) → track → cylinder → partition (contiguous cylinders). #Disk  
- Block = 1 or more contiguous sectors. #Block  
- Partition = contiguous cylinders. #Partition  
- Path notation:
  - Absolute: /a/b/c (starts with /)  
  - Relative: ../x/y or ./file (no leading /)  
- Permission bits (per class: user/group/other):
  - read = 4, write = 2, execute = 1  
  - numeric mode = sum per class (e.g., rwxr-xr-x = 7 5 5 → 755). #Permissions
- Inode attributes (common): permissions, hard link count, UID, GID, size, atime, mtime, ctime, inode number, device/partition id. #Inode

---

## Key Algorithms / Concepts (bulleted)
- Hierarchical namespace: single tree rooted at "/" where all file systems are mounted. #Hierarchy  
- Mounting: attach a filesystem (partition/device) at a directory (mount point). #Mount  
- Device-as-file: hardware devices represented as special files in /dev. #DeviceFile #dev  
- Partitioning: split physical disk into logical partitions to host file systems. #Partitioning  
- Inode-based storage: directory entries map names → inode numbers; inode stores file metadata + block pointers. #InodeStructure  
- Absolute vs Relative resolution: resolve from / vs from current working directory (CWD). #PathResolution

---

## Important Properties / Invariants
- Single root ("/") — everything is reachable under this tree. #Root  
- Directories are files containing name → inode mappings. #Directory  
- Inodes are unique within a filesystem; the inode number + device identifies a file location. #Inode  
- Hard links: multiple directory entries can point to same inode; link count stored in inode. #HardLink  
- Device files in /dev control hardware access via permissions. #dev  
- /tmp is ephemeral (often cleared on reboot). Do not store permanent data there. #tmp  
- /bin and /usr/bin: user commands; /sbin and /usr/sbin: system/admin commands. #bin #sbin #usr  
- /etc stores system configuration; /var stores variable runtime data (logs, spool, db). #etc #var  
- Partitioning helps separate concerns (OS / user data / swap / logs). #Partitioning

---

## Common Directories (quick map)
- / — root #Root  
- /bin — essential user binaries (programs) #bin  
- /sbin — system binaries (admin) #sbin  
- /usr — user programs/libraries/data (larger read-only hierarchy) #usr  
- /lib, /lib64 — shared libraries for binaries #lib  
- /etc — system-wide configuration files #etc  
- /home — user home directories (/home/username) #home  
- /dev — device files (disks, terminals, etc.) #dev  
- /tmp — temporary files (cleared on reboot) #tmp  
- /var — variable files (logs, mail, spool, db) #var

---

## Quick Reference — Commands (compact)
| Command | Purpose | Example |
|---|---:|---|
| pwd | print working directory | pwd → /home/alice |
| ls | list directory | ls -l (long), ls -a (all) |
| cd | change directory | cd /etc ; cd .. ; cd ~ |
| mkdir | create directory | mkdir notes |
| rmdir | remove empty directory | rmdir olddir |
| rm | remove file/dir | rm file ; rm -r dir |
| cp | copy file/dir | cp src dst ; cp -r dir1 dir2 |
| mv | move/rename | mv old new ; mv file /path/ |
| ln | hard link | ln target linkname |
| ln -s | symbolic (soft) link | ln -s /path/target linkname |
| chmod | change permissions (symbolic or numeric) | chmod 755 script.sh ; chmod u+x file |
| chown | change owner/group | chown user:group file |
| stat | show inode & timestamps | stat file |
| df | filesystem disk usage (per FS) | df -h |
| du | disk usage (per file/dir) | du -sh dir |
| mount / umount | attach/detach filesystem | mount /dev/sda1 /mnt ; umount /mnt |

(Use root/sudo for privileged operations like mount, chown to root-owned files, writing to /sbin, etc.)

---

## Quick Patterns / Cheats
- Paths:
  - /absolute/path — stable regardless of CWD  
  - relative: ./file (current), ../ (parent)  
- Permissions mapping:
  - rwxrwxrwx → octal 777; rwxr-xr-x → 755; rw-r--r-- → 644  
- Check file metadata:
  - ls -l → permissions, link count, owner, group, size, mtime, name  
  - stat → detailed inode info (inode #, blocks, atime/mtime/ctime)  
- Find mount & partition info:
  - lsblk, fdisk -l, blkid, cat /proc/partitions, df -h  
- Temporary files: avoid storing persistent data in /tmp (cleared on reboot). #tmp
- When copying ownership and perms: use cp -a (archive) to preserve metadata.  
- Use symbolic links for shared access across directories; hard links only within same FS. #links

---

Keep this sheet near your reference materials for quick lookup of filesystem structure, path rules, inode attributes, common directories, permission octal mapping, and essential commands.