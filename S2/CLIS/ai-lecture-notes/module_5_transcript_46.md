# Kernel I/O & Linux I/O Utilities — Cheatsheet
#keywords: #kernel #io #input-output #block-layer #character-layer #network-layer #device-drivers #filesystem #partitioning #scheduling #interrupts #disk-health #linux-commands

---

## Key Definitions (one-liners)
- #InputOutput: Transfer of data between memory and external devices.
- #Block-Layer: Manages storage devices that read/write fixed-size blocks (e.g., HDD/SSD). Typical block sizes: 512 B, 4 KiB.
- #Character-Layer: Manages byte-by-byte devices (terminals, keyboard, mouse, serial ports).
- #Network-Layer: Manages packet I/O, includes network device drivers + network stack (routing, flow control).
- #Block-Device-Driver / #Character-Device-Driver / #Network-Device-Driver: Kernel drivers providing interface between kernel and hardware.
- #Kernel-Module: Piece of code loaded into kernel at runtime to extend functionality (lsmod / rmmod).
- #Scheduler (I/O scheduler): Kernel component ordering disk I/O requests for performance/fairness.
- #Interrupt: Signal from hardware/software to CPU indicating an event needs immediate attention (hardware vs software interrupts).
- #Partition-Table: Table format that describes disk partitions; common formats: MBR (legacy) and GPT (GUID, modern).

---

## Formulas / Notation / Quick facts
- Block sizes: typical = 512 B, 4 KiB (4096 B)
- File descriptors: 0 = stdin, 1 = stdout, 2 = stderr
- Redirection operators:
  - >  : redirect stdout to file (create/overwrite)
  - >> : append stdout to file
  - <  : take stdin from file
  - 2> : redirect stderr to file
  - Example: cmd >out.txt 2>err.txt
- dd syntax: dd if=<input-file/device> of=<output-file/device> [bs=<block-size>] [count=<n>]

---

## Key Algorithms / Concepts (bulleted)
- #ThreeLayersOfIO
  - #Block-Layer: buffered I/O, random access via blocks
  - #Character-Layer: unbuffered or line/byte oriented, sequential
  - #Network-Layer: packetized I/O, managed by network stack
- #I/O-Schedulers
  - #CFQ (Completely Fair Queuing): separate queues per process → fair share of disk time
  - #NOOP: single FIFO queue → minimal reordering (good for SSDs)
  - #deadline: assigns deadlines to requests → prevents starvation (reduces latency)
- #Partitioning-Tools
  - #fdisk: MBR-focused interactive CLI (legacy)
  - #gdisk: GPT-focused interactive CLI (modern)
  - #parted: supports MBR & GPT, handles large disks (>2 TiB)
  - #cfdisk: text-based interactive UI
  - #sfdisk: scriptable batch partitioning (automation)
- #Device-Nodes: /dev contains device files (e.g., /dev/tty*, /dev/sdX*)
- #EverythingIsAFile (Linux/Unix philosophy): devices exposed via filesystem nodes

---

## Important Properties / Invariants
- Block devices are accessed in block units and usually buffered by kernel caches.
- Character devices provide byte or character streams and are often unbuffered.
- Network I/O is packet-based; routing/flow control performed by kernel network stack.
- Partitioning is destructive: always unmount & backup before modifying partitions.
- Kernel modules can be added/removed at runtime but may be required for hardware support.
- Use NOOP or deadline for SSDs/NVMe vs rotational disks depending on workload.
- Always check /sys and /proc virtual files for kernel/device info (non-destructive reads).

---

## Quick Reference — Commands (purpose | example)
- Device listing & modules
  - lsblk [-f|-o|-t] : list block devices and filesystems — e.g., lsblk -f
  - lsusb : list USB devices
  - lspci : list PCI devices
  - lsmod : list loaded kernel modules
  - rmmod <module> : remove kernel module
  - dmesg : kernel diagnostic/boot messages
  - cat /proc/interrupts : show interrupts handled by CPU
  - cat /sys/block/sda/queue/scheduler : show available I/O schedulers (current in [brackets])
- Mount / unmount
  - mount <device> <mountpoint>
  - umount <mountpoint|device>
- Partitioning & disk layout
  - fdisk -l /dev/sdX : list partitions (MBR-focused)
  - gdisk /dev/sdX : interactive GPT tool
  - parted -l : list partitions (supports large disks)
  - cfdisk /dev/sdX : text UI partitioning
  - sfdisk <script> : scriptable partitioning
- Disk usage & info
  - df -h : filesystem disk usage (human)
  - lsblk : block device/partition tree
  - hwinfo --cpu : hardware info (CPU)
- Disk health (SMART)
  - smartctl -a /dev/sdX : show SMART info
  - smartctl -t short /dev/sdX : run short test
  - smartctl -t long /dev/sdX : run long test
- Low-level copying
  - dd if=/dev/sdX of=image.img bs=4M status=progress
- Text & redirection (character I/O examples)
  - cat file : display file contents
  - echo "text" > out.txt : redirect stdout to file (creates out.txt)
  - cmd < in.txt : take stdin from in.txt
  - ls somefile 2>error.txt : redirect stderr to file
  - Use > (overwrite) vs >> (append)

---

## Quick Reference Table (command → purpose)
| Command | Purpose |
|---|---|
| lsblk | list block devices & mount points |
| fdisk -l | list/inspect partitions (MBR) |
| gdisk / parted | GPT / large-disk partitioning |
| cfdisk | interactive partition UI |
| sfdisk | scriptable partition operations |
| mount / umount | attach/detach filesystems |
| dd if=... of=... | block-level copy / cloning |
| smartctl -a /dev/sdX | SMART disk health report |
| lspci / lsusb | list PCI / USB devices |
| lsmod / rmmod | list / remove kernel modules |
| dmesg | kernel diagnostic messages |
| cat /proc/interrupts | show interrupt counts |
| cat /sys/block/sda/queue/scheduler | show I/O scheduler in use |

---

## Safety & Exam Tips (very short)
- Always back up before partitioning or using dd.
- Unmount filesystems before editing partitions.
- Use lsblk, fdisk -l, parted -l to identify devices before actions.
- Use smartctl to check drive health before heavy I/O or migration.
- To find current I/O scheduler: cat /sys/block/<device>/queue/scheduler
- To catch errors only: use 2>err.txt; to discard output: >/dev/null 2>&1

---

Hashtags (core): #block-layer #character-layer #network-layer #device-drivers #kernel-modules #mount #fdisk #gdisk #parted #cfdisk #sfdisk #lsblk #lsusb #lspci #lsmod #rmmod #dmesg #cat #echo #redirection #dd #smartctl #hwinfo #CFQ #NOOP #deadline #interrupts

If you want, I can produce a one-page printable PDF layout or a single-page condensed version with only commands and one-line reminders. Which format do you prefer?