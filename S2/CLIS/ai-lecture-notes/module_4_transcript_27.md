# In-memory File System (TMPFS) — Cheatsheet
#keywords: #tmpfs #in-memory #filesystem #Linux #RAM #mount #umount #rm #/tmp #caching #volatile #swap #performance #temporary_storage #SSD #hard_disk

## Key Definitions
- TMPFS: In-memory file system that stores files/directories in RAM (no disk persistence). #tmpfs #in-memory
- In-memory (RAM): Volatile primary memory used for fast read/write; not secondary storage. #RAM
- Disk (secondary storage): Persistent storage devices (HDD, SSD). #hard_disk #SSD
- Volatile: Data lost on power-off or unmount. #volatile
- Mount point: Directory where a filesystem is attached into the VFS tree. #mount
- Swap: Disk-backed area used when RAM is scarce; TMPFS may be swapped out. #swap
- Unmount: Detach filesystem (data lost for TMPFS). Use umount. #umount

## Formulas / Command Syntax
- Mount TMPFS (example):
  - mount -t tmpfs -o size=1G tmpfs /path/to/mount
- Unmount:
  - umount /path/to/mount
- Clear TMPFS content:
  - rm -rf /path/to/mount/*   (or target files/directories)
- Notes on size option:
  - -o size=<value> (e.g., 1G, 512M) sets the maximum TMPFS allocation.

## Key Concepts / Uses
- #speed: Fast read/write because data is in #RAM (suitable for temporary high-speed needs).
- #volatile: Not persistent — data lost on shutdown or unmount.
- #mounting: Can be mounted at any directory like other filesystems.
- #/tmp: Common default use (temporary files for distributions).
- #caching: Store frequently accessed data to reduce latency.
- #temporary_storage: Scratchpad for programs or maintenance tasks.
- #swap_interaction: If RAM low, TMPFS pages may go to swap (performance hit).

## Important Properties / Invariants
- Resides entirely in RAM (consumes system memory).
- Size limited by available memory (and any explicit size= limit).
- Volatile: unmount or shutdown → data lost.
- May use swap if RAM is insufficient (can degrade performance).
- Mounting/unmounting and managing contents are administrative operations (permissions apply).
- Suitable for ephemeral data; not for persistent storage.

## Quick Reference (scannable)
- Mount example:
  - mount -t tmpfs -o size=1G tmpfs /mnt/tmp
- Unmount:
  - umount /mnt/tmp  → frees RAM and loses contents
- Clean content:
  - rm -rf /mnt/tmp/*  → frees memory without unmounting
- Common use cases:
  - /tmp, caches, build/scratch directories, temporary storage for processes
- Limits & cautions:
  - Do not store large persistent files in TMPFS (risk OOM / swap).
  - Monitor memory usage (free, top, /proc/meminfo).
  - Consider size= option to cap TMPFS usage.
- Performance:
  - Faster than disk-backed filesystems; performance drops if swapped.
- Recovery:
  - No recovery after unmount or power loss (back up to disk before unmount if needed).
- Best practices:
  - Use for ephemeral, performance-sensitive data.
  - Set explicit size= if needed.
  - Periodically clean large/unneeded files (rm -rf).
  - Avoid relying on TMPFS for persistence.

# See also: #mount_command #umount #rm #/tmp #caching #swap #performance

(Keep this sheet open during the exam as a quick reference for TMPFS behavior, commands, and limitations.)