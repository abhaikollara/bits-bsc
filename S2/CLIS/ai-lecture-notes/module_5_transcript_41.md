# Linux Block Devices & Disk-Utilities — Cheatsheet
#hashtags: #lsblk #fdisk #df #blockdevices #partitions #filesystem #mount #storage #linux

---

## Key Definitions
- Block device: I/O device that transfers data in fixed-size blocks (e.g., HDD, SSD). #blockdevices  
- Character device: I/O device that transfers data as a stream of bytes. #chardev  
- Partition: A defined region of a block device used as an independent filesystem/volume. #partitions  
- Mount point: Directory where a filesystem is attached into the directory tree. #mount #filesystem

---

## Syntax / Command Templates
- lsblk [options] [device] — list block devices and attributes. #lsblk  
- fdisk [options] [device] — start fdisk utility to create/modify/delete partitions on device. #fdisk  
- df [options] [file|filesystem|mountpoint] — report disk space usage of mounted filesystems. #df

---

## Common Options (quick)
- lsblk
  - -f : show filesystem type and mountpoint (#lsblk -f)  
  - -t : show tree view (#lsblk -t)  
  - -o <cols> : show only specified columns (e.g., NAME,SIZE,MOUNTPOINT)  
- fdisk (interactive)
  - p : print existing partitions  
  - n : create new partition  
  - d : delete partition  
  - w : write changes and exit  
  - (usage example) fdisk /dev/sda  
- df
  - -h : human-readable sizes (KB/MB/GB)  
  - -k : display sizes in 1 KB blocks  
  - (usage example) df -h /path/or/device

---

## Columns / Output Notes
- lsblk typical columns: NAME, MAJ:MIN, RM, SIZE, RO, TYPE, MOUNTPOINT (use -o to customize). #lsblk  
- df output shows total blocks, used, available, use% and mount point for each mounted filesystem. #df

---

## Important Properties & Invariants
- fdisk is destructive: writing changes (w) modifies partition table -> possible data loss. Always double-check. #fdisk  
- lsblk shows block devices even if not mounted; -f adds filesystem & mountpoint info. #lsblk  
- df reports only mounted filesystems by default (use path to show a specific mount). #df  
- Block/sector sizes may vary by device; utilities show bytes/sectors information (check fdisk output). #blockdevices

---

## Quick Reference Table

| Command | Main purpose | Key options | Example |
|---|---:|---|---|
| lsblk | list block devices & attributes | -f, -t, -o | lsblk -f |
| fdisk | create/modify/delete partitions (interactive) | p, n, d, w | fdisk /dev/sda → p → n → w |
| df | show disk usage for mounted filesystems | -h, -k | df -h /dev/zero |

---

## Safety / Best Practices
- Always back up important data before using fdisk. #fdisk  
- Prefer viewing with lsblk and df before making partition changes. #lsblk #df  
- Use -h for readable sizes when checking space; use -k if you need exact 1KB-block counts. #df

---

## Quick Command Cheats (copyable)
- List all block devices: lsblk  
- List with filesystem & mountpoint: lsblk -f  
- Tree view of devices: lsblk -t  
- Show only specific columns: lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT  
- Start partition editor: fdisk /dev/sda  
  - inside fdisk: p (print), n (new), d (delete), w (write & exit)  
- Show disk usage human-readable: df -h  
- Show disk usage in 1KB blocks: df -k /path

---

End — concise reference for lsblk, fdisk, df. Use caution with fdisk; verify before writing changes. #linux #storage