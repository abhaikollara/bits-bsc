# hwinfo & parted — Linux hardware & partition cheatsheet

Keywords: #hwinfo #parted #linux #disk #partition #gpt #ext4 #primary #bootable #sudo #superuser #systemadministration #hardware #mklabel #mkpart #resizepart #set #quit #redirection

---

## Key Definitions
- hwinfo: CLI tool to gather detailed hardware information. #hwinfo
- parted: CLI utility to create, resize, and manage disk partitions. #parted
- Partition table (label): scheme describing partitions on a disk (e.g., GPT). #gpt
- Filesystem: data structure used to store files on a partition (e.g., ext4). #ext4
- Bootable partition: partition flag allowing boot loader to use it. #bootable
- Superuser / sudo: privileged account or command prefix required for hwinfo/parted. #sudo #superuser
- Redirection (>): shell operator to write command output to a file. #redirection

---

## Syntax / Formulas (quick patterns)
- hwinfo: 
  - hwinfo [options] [category]
  - Example: hwinfo                 (show complete hardware info)
  - Example: hwinfo cpu             (show CPU category)
  - Save output: hwinfo > filename  (#redirection)
- parted:
  - parted [options] <device>
  - Example: sudo parted /dev/sdX
  - After entering, interact at (parted) prompt
  - End session: quit

---

## Key Commands & Concepts (#quick)
- hwinfo:
  - hwinfo — gathers comprehensive hardware details (#hwinfo)
  - Use category names to limit output (e.g., cpu, memory, network)
  - Redirect output to file: hwinfo > all-hw.txt (#redirection)
- parted:
  - Start: sudo parted /dev/sdX → enters (parted) prompt (#sudo)
  - mklabel gpt — create new GPT partition table (#mklabel #gpt)
  - mkpart primary ext4 <start> <end> — create primary partition formatted ext4 (#mkpart #primary #ext4)
  - resizepart <part-num> <end> — resize a partition (end can be percent like 80%) (#resizepart)
  - set <part-num> boot on/off — toggle bootable flag (#set #bootable)
  - quit — save & exit (commits changes) (#quit)
- Privilege note:
  - Both hwinfo and parted require superuser privileges; use sudo or root. (#sudo #superuser)

---

## Important Properties / Invariants
- Changes in parted modify partition table—can cause data loss; always backup first. #parted
- mklabel overwrites existing partition table (destructive). #mklabel
- resizepart affects partition boundaries only (filesystem resize may be required separately). #resizepart #ext4
- Boot flag is a partition attribute, not a filesystem type. #bootable
- hwinfo is informational only (non-destructive) but requires privileges to access low-level hardware details. #hwinfo

---

## Quick Reference (scannable)
- Start hwinfo (full): hwinfo
- hwinfo for CPU: hwinfo cpu
- Save hwinfo: hwinfo > hwinfo.txt
- Start parted on disk: sudo parted /dev/sdX
- Create GPT table: (parted) mklabel gpt
- Create partition: (parted) mkpart primary ext4 0% 100%  (adjust ranges)
- Resize partition 1 to 80%: (parted) resizepart 1 80%
- Make partition 1 bootable: (parted) set 1 boot on
- Exit & write changes: (parted) quit
- Always: backup data before using parted; use sudo for both tools.

---

Tags for search: #hwinfo #parted #mklabel #mkpart #resizepart #set #quit #gpt #ext4 #bootable #sudo #redirection #linux #hardware #disk

(Concise, exam-ready: copy-paste commands above; follow backup & superuser cautions.)