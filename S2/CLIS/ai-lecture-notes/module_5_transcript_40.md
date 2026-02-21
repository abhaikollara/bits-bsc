# Partitioning & Inspecting Hard Disks in Linux — Cheatsheet

Keywords
#disk #partition #partitiontable #MBR #GPT #lsblk #fdisk #parted #gdisk #df #smart #smartctl #dd #dev #sectors #blockdevice #filesystem #lowlevel #sudo #backup

--- 

## Key Definitions
- Block device: Kernel object representing raw storage (e.g., /dev/sdX). #blockdevice
- Partition: Contiguous region of a disk defined in the partition table. #partition
- Partition table: On-disk structure describing partitions — MBR or GPT. #partitiontable #MBR #GPT
- Sector: Smallest addressable unit on disk (typically 512 bytes). #sectors
- Block size (bs): I/O unit for dd; common bs=512, bs=1M. #blockdevice
- SMART: Self-Monitoring, Analysis and Reporting Technology — drive health system. #smart
- smartctl: Tool to query SMART attributes and run tests. #smartctl
- dd: Low-level utility to read/write raw disk blocks. Dangerous — can overwrite. #dd
- /dev/sdX: Device node pattern for SATA/SCSI disks (X = a, b, ...). Always double-check. #dev

---

## Formulas / Command Syntax (quick reference)
- dd general: dd if=<input> of=<output> bs=<blocksize> count=<n> skip=<n>
  - Read Nth sector: dd if=/dev/sdX of=sector.bin bs=512 count=1 skip=N
  - Read first sector: dd if=/dev/sdX of=mbr.bin bs=512 count=1 skip=0
  - Create disk image: dd if=/dev/sdX of=disk.img bs=4M status=progress
  - Overwrite first 1 MB with zeros: dd if=/dev/zero of=/dev/sdX bs=1M count=1
- smartctl:
  - Show attributes: sudo smartctl -a /dev/sdX
  - Start long test: sudo smartctl -t long /dev/sdX
- fdisk/gdisk/parted/lsblk/df:
  - List block devices: lsblk (often lsblk -f or -o NAME,SIZE,MOUNTPOINT,FSTYPE)
  - fdisk list partitions: sudo fdisk -l /dev/sdX
  - parted list: sudo parted -l
  - df human-readable: df -h

---

## Key Commands / Concepts
- lsblk: list block devices, sizes, mount points. #lsblk
- fdisk: interactive MBR/partition tool. Options: d (delete), n (new), p (primary), w (write). #fdisk
- gdisk: GPT partition table manipulator (interactive). Options: d, n, w. #gdisk
- parted: GNU parted for partition info and manipulation; used with -l for listing. #parted
- df -h: show mounted filesystem usage in human-readable units. #df
- smartctl: query SMART attributes and initiate self-tests. #smartctl #smart
- dd: raw block read/write (imaging, sector inspection, wiping). Use bs/count/skip. #dd
- /dev/sdX naming: X = a, b, c... identify correct device before any write. #dev

---

## Important Properties / Invariants
- Many commands require root: prepend sudo for low-level device access. #sudo
- dd is destructive: if and of must be correct — swapping them can overwrite source. #dd #lowlevel
- First 512 bytes often contain MBR and partition table — overwriting = loss of partition info. #MBR
- GPT uses more than just first sector (primary/backup headers); zeroing can corrupt disk. #GPT
- Always backup (image) before modifying partitions or writing zeros. #backup
- bs affects performance and alignment; use bs=4096 or bs=1M for faster imaging. #blockdevice
- count controls how many blocks are read/written; skip moves read pointer by blocks. #dd

---

## Quick Reference Table (commands & single-line use)
| Command | Purpose | Typical flags / example |
|---|---:|---|
| lsblk | List block devices & mountpoints | lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT |
| fdisk | Interactive MBR partition editor | sudo fdisk /dev/sdX (use d,n,p,w) |
| gdisk | Interactive GPT partition editor | sudo gdisk /dev/sdX (use d,n,w) |
| parted | Partition info & manipulator | sudo parted -l |
| df | Mounted filesystem usage | df -h |
| smartctl | SMART info / tests | sudo smartctl -a /dev/sdX ; sudo smartctl -t long /dev/sdX |
| dd | Raw read/write / imaging / sector access | dd if=/dev/sdX of=disk.img bs=4M status=progress |
| dd (read sector) | Read specific sector | dd if=/dev/sdX of=sec.bin bs=512 count=1 skip=N |
| dd (wipe) | Overwrite start of disk with zeros | dd if=/dev/zero of=/dev/sdX bs=1M count=1 |

---

## Practical Tips (exam quick-hits)
- Verify device: lsblk; double-check /dev/sdX letter before write operations. #lsblk #dev
- For inspection only, prefer read-only commands: lsblk, fdisk -l, parted -l, smartctl -a. #smartctl
- Use dd with status=progress to monitor long copies. Example: dd if=/dev/sdX of=d.img bs=4M status=progress
- To image entire disk (faster): dd if=/dev/sdX of=/path/disk.img bs=1M
- To examine filesystem usage: df -h /mountpoint
- To run a SMART long self-test: sudo smartctl -t long /dev/sdX (check results with -a after completion) #smart
- When modifying partitions interactively: create (n), delete (d), write changes (w). Unsaved changes lost on quit. #fdisk #gdisk

---

Caution: All low-level operations can cause irreversible data loss. Always backup and confirm device identifiers before running write commands. #backup #sudo #dd