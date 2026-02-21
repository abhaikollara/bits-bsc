# Superblocks — Linux file system metadata cheatsheet
# #superblock #filesystem #metadata #inode #block #bitmap #backup-superblock #mount #fsck #dumpe2fs #corruption #recovery #ext4 #xfs #btrfs #kernel

## Key Definitions (one-line)
- Superblock: the primary metadata block describing a file system’s layout, size and state (first data block / fixed offset).  
- Inode: data structure representing a file or directory (stores metadata, pointers to data blocks).  
- Block: fixed-size unit of data storage in a file system (size = block_size bytes).  
- Block bitmap: bitset marking which data blocks are in use/free.  
- Inode bitmap: bitset marking which inodes are in use/free.  
- Backup superblock: redundant copies of the superblock distributed in the FS for recovery.  
- Mount: the operation where the kernel reads the superblock to enable access.  
- Mount count: number of mounts since last check.  
- fsck: file system check/repair utility.  
- dumpe2fs: utility to display ext2/3/4 superblock and FS info (pass mount point/device).

## Superblock — Key fields (quick table)
| Field | One-line meaning | #hashtag |
|---|---:|---|
| filesystem type | FS type (e.g., Ext4, XFS, Btrfs) | #ext4 #xfs #btrfs |
| total inodes | Number of inodes available | #inode |
| total blocks | Number of data blocks available | #block |
| block size | Bytes per block | #block |
| mount count | Times mounted since last check | #mount-count |
| mount time | Timestamp when last mounted | #mount-time |
| last write time | Timestamp of last write | #last-write-time |
| inode bitmap | Bitmap of allocated/free inodes | #inode #bitmap |
| block bitmap | Bitmap of allocated/free blocks | #block #bitmap |
| backup superblocks | Locations of redundant superblocks | #backup-superblock |

## Formulas / Quick equations
- Disk capacity (bytes) = total_blocks * block_size  
- Bitmap size (bytes) ≈ ceil(count / 8)  (count = total_blocks or total_inodes)  
- Common integer relations: indexes and offsets measured in blocks: byte_offset = block_index * block_size

## Key Concepts / Actions
- Mounting: kernel reads superblock to interpret layout/health and allow access — if superblock invalid, mount may fail. #mount #kernel  
- Backup/Recovery: use backup superblocks to recover when primary is corrupted. #backup-superblock #recovery  
- fsck: run file system check to detect and repair inconsistencies (including superblock issues). #fsck  
- dumpe2fs: inspect superblock details for ext* filesystems (pass mount point/device). #dumpe2fs  
- Direct modification: editing superblock data manually (raw disk edits) is risky — prefer standard tools. #corruption

## Important Properties / Invariants
- Superblock is authoritative for FS layout and must be consistent with inodes/bitmaps. #metadata  
- Backup superblocks exist to provide redundancy — used when primary corrupted. #backup-superblock  
- Linux kernel requires correct superblock to mount and interpret file system. #kernel  
- Bitmaps must correspond to in-use counts reported in superblock (inconsistency => fsck fix). #bitmap

## Quick Reference (scannable)
- Common commands:
  - Inspect (ext2/3/4): dumpe2fs <mount-point|device>  #dumpe2fs
  - Repair/check: fsck <device|mount-point>  #fsck
- Quick checks:
  - If mount fails → check superblock via dumpe2fs and try fsck. #mount #fsck
  - If primary superblock corrupted → locate and restore from backup superblock. #backup-superblock
  - Don’t edit raw superblock fields manually — use FS utilities only. #corruption
- Helpful facts:
  - Superblock contains type, counts, block size, timestamps, bitmaps, backups. #superblock
  - Calculate raw FS size: total_blocks * block_size.  
  - Bitmap byte size: ceil(total_entries / 8). #bitmap

Keep this sheet for quick lookup of fields, tools and recovery steps; prefer standard utilities (dumpe2fs, fsck) over raw edits.