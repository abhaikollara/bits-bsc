# Linux File System Layout & Implementation — Cheatsheet
#keywords: #filesystem #linux #hierarchy #directories #mount #virtualfilesystem #devicefile #ext4 #xfs #btrfs #zfs #fat32 #ntfs #journaling #snapshot #COW

---

## Key Definitions
- Root: `/` — top-level directory; all paths under this. #root
- Absolute path: path starting with `/`. #path
- Relative path: path relative to current directory (no leading `/`). #path
- Home directory: `~` or `/home/<user>` — default user directory. #home
- Mount point: directory where another filesystem is attached. #mount
- Device file: special files in `/dev` that represent hardware or virtual devices. #devicefile #dev
- Virtual filesystem: in-memory pseudo-filesystems exposing kernel/process info (e.g., `/proc`, `/sys`). #virtualfilesystem #proc #sys
- Filesystem implementation: on-disk (or on-device) organization and access logic (Ext4, XFS, Btrfs, ZFS, etc.). #ext4 #xfs #btrfs #zfs

---

## Filesystem Layout — Standard & System Directories (quick table)
| Directory | Purpose | Hashtag |
|---|---:|---|
| `/bin` | Essential user executables (commands used by all users). | #bin |
| `/sbin` | System/admin executables (root/admin tools). | #sbin |
| `/usr` | User programs, libraries, docs (read-only at runtime). | #usr |
| `/var` | Variable data: logs, mail, spool, caches, temp runtime data. | #var |
| `/etc` | System configuration files. | #etc |
| `/dev` | Device files (hardware/virtual devices). | #dev |
| `/proc` | Process & kernel info (virtual FS). | #proc |
| `/sys` | Kernel data structures & config (virtual FS). | #sys |
| `/home` | Users' home directories. | #home |
| `/mnt`, `/media` | Common mount points for temporary/media mounts. | #mount |

---

## Formulas / Notation
- Path separator: `/`
- Home shorthand: `~` = `/home/<user>`
- Mount command (syntax): mount <device> <mount-point>  (use `-t <fstype>` to specify) #mount
- Common inspection: `df -h`, `lsblk`, `mount` (list mounted FS)

---

## Key Algorithms / Concepts
- Hierarchical file system: tree structure with single root; directories contain files/subdirs. #hierarchy
- Standard vs System directories: standard for users (`/usr`, `/home`); system controlled (`/sbin`, `/etc`). #systemdirs
- Mounting: attach filesystems at mount points; multiple filesystems can be mounted anywhere under `/`. #mount
- Virtual filesystems:
  - `/proc`: runtime process & kernel metadata (not persisted). #proc
  - `/sys`: kernel object model & configuration (sysfs). #sys
- Device files: special inode types representing device interfaces (character/block). #devicefile
- Filesystem features by type:
  - Ext4: default, journaling, supports large files/partitions, backward-compatible with ext3/ext2. #ext4 #journaling
  - XFS: high-performance, scalable, suitable for large storage. #xfs
  - Btrfs: modern, snapshots, subvolumes, compression, checksums, COW. #btrfs #snapshot #COW
  - ZFS: pooled storage, integrated volume management, checksums, robust data protection (not native but widely used). #zfs
  - FAT32 / NTFS: Windows-compatible filesystems used for interchange. #fat32 #ntfs

---

## Important Properties / Invariants
- Single root hierarchy: every file/directory reachable under `/`. #root
- Mounts can hide underlying directory contents while mounted. #mount
- Virtual filesystems (`/proc`, `/sys`) are ephemeral (not stored on disk). #virtualfilesystem
- Journaling (Ext4, XFS): helps recover metadata (and optionally data) after crashes. #journaling
- COW (Btrfs, ZFS): writes create new blocks — enables snapshots and stronger integrity features. #COW
- Snapshots/subvolumes: allow point-in-time views and cheap clones (Btrfs/ZFS). #snapshot
- Device interface layer: `/dev` provides filesystem-accessible handles to hardware. #devicefile

---

## Quick Reference (scannable)
- Common dirs: `/bin` `/sbin` `/usr` `/var` `/etc` `/dev` `/proc` `/sys` `/home` `/mnt` `/media` #directories
- Mount common commands:
  - mount <device> <dir>  (mount device to dir) #mount
  - umount <dir|device>  (unmount) #mount
  - mount -t <type> ...  (specify FS type) #mount
- Inspect:
  - df -h  (space usage) #df
  - lsblk  (block devices) #lsblk
  - blkid  (labels/UUIDs) #blkid
  - cat /proc/mounts or mount  (list mounts) #proc
- When to choose FS:
  - Ext4: general-purpose, compatibility, stable. #ext4
  - XFS: large filesystems, high throughput. #xfs
  - Btrfs: snapshots, subvolumes, compression, modern features. #btrfs
  - ZFS: enterprise features, data integrity, pooling (often via native kernel module or FUSE). #zfs
  - FAT32/NTFS: cross-OS compatibility (Windows). #fat32 #ntfs
- Virtual FS notes:
  - /proc: process IDs as directories, kernel tunables (/proc/sys). #proc
  - /sys: device and driver attributes, writable knobs for hardware params. #sys
- Permissions & control: system directories typically require root to modify (`/sbin`, `/etc`, `/usr`). #permissions

---

If you want, I can:
- Add a one-page printable PDF layout,
- Include common command examples (mkfs.*, fsck, tune2fs, btrfs subvolume/snapshot commands),
- Or expand the table with typical default mount points and sample usages.