# Kernel I/O Structure & Linux I/O Cheatsheet

#hashtags
#KernelIO #I/O #InputOutput #Linux #BlockIO #CharacterIO #NetworkLayer #DeviceDrivers #BlockDevices #CharacterDevices #NetworkDevices #BufferCache #IOScheduler #CFQ #NOOP #deadline #SATA #SCSI #NVMe #TTY #sysfs #procfs #IOAPIs #read #write #open #ioctl #mmap #fopen #fgets #fclose #I/Oredirection #stdin #stdout #stderr #/dev #lsblk #lspci #lsusb #lsmod #modprobe #rmmod #dmesg #Socket #TCP #UDP #IPv4 #IPv6

## Key Definitions (one-liners)
- Kernel I/O: data transfer between kernel/user memory and hardware devices.  
- Block device: storage device that reads/writes fixed-size blocks (e.g., disks).  
- Character device: device that streams data character-by-character (e.g., terminals).  
- Network layer: packet-oriented I/O stack (network drivers + protocol stack).  
- Device driver: kernel module that interfaces with specific hardware.  
- I/O scheduler: kernel component that orders block I/O requests for performance.  
- Buffer cache: RAM region caching block device data to reduce disk access.  
- sysfs/procfs: virtual filesystems exposing kernel state/config to user space.  
- Device file: special file under /dev representing a hardware device.  
- Standard streams: stdin (0), stdout (1), stderr (2).  
- I/O redirection: shell mechanism to map standard streams to files/devices.

## Formulas / Notation / Sizes
- Block sizes: typically 512 B — 4 KiB (common values: 512, 1024, 2048, 4096).  
- File descriptors: stdin = 0, stdout = 1, stderr = 2.  
- Common system calls / APIS: open(), read(), write(), ioctl(), mmap(), close()  
- stdio wrappers: fopen(), fgets(), fprintf(), fclose()  
- Redirection symbols: > (stdout), < (stdin), 2> (stderr), >> (append), 2>&1 (merge stderr→stdout)

## Key Algorithms / Concepts (bulleted)
- #BlockIO
  - Block device drivers (SATA, SCSI, #NVMe) handle low-level disk I/O.  
  - I/O scheduler types: #CFQ (fairness), #NOOP (minimal), #deadline (latency bounds).  
  - Buffer cache: holds frequently-used blocks to reduce disk seeks.
- #CharacterIO
  - Character device drivers (e.g., #TTY at /dev/tty1) handle serial/terminal I/O.
- #NetworkLayer
  - Network device drivers for NICs/Wi-Fi; network stack implements IPv4/IPv6, transport (TCP/UDP) and #Socket API.
- #DeviceFiles
  - Devices exposed as files under /dev (e.g., /dev/sda, /dev/tty). Interact via normal file ops.
- #KernelAPIs
  - syscalls: open/read/write/ioctl/mmap/close for kernel-user I/O interaction. stdio: fopen/fgets/fclose for user-level file I/O.
- #I/Oredirection (shell)
  - Redirect standard streams using >, <, >>, 2>, 2>&1, &>.

## Important Properties / Invariants
- Block devices: random-access in block units; kernel queues requests and scheduler reorders them to optimize head movement/latency.  
- Character devices: no block buffering semantics — sequential character stream.  
- Buffer cache correctness: cached data must be synced to device (write-back vs write-through semantics).  
- Device files are just kernel interfaces — permission and major/minor numbers determine driver association.  
- sysfs/procfs are read/write interfaces to kernel state — not persistent storage.  
- Standard streams default: stdin ← keyboard, stdout/stderr → terminal unless redirected.  
- I/O scheduler choice impacts throughput vs latency vs fairness.

## Quick Reference (scannable)

Redirection symbols
| Symbol | Meaning / Example |
|---|---|
| cmd > file | Redirect stdout to file (overwrite) |
| cmd >> file | Append stdout to file |
| cmd < file | Use file as stdin |
| cmd 2> file | Redirect stderr to file |
| cmd > out 2>&1 | Redirect stdout and stderr to out |
| cmd &> file | Bash shorthand to redirect stdout+stderr to file |

Common device examples
- /dev/sda — first block disk (#BlockDevices)  
- /dev/tty1 — first virtual terminal (#CharacterDevices)

Important kernel filesystems
- /proc — process & kernel info (#procfs)  
- /sys — device and driver attributes (#sysfs)

Useful commands
| Command | Purpose |
|---|---|
| lsblk | List block devices & partitions (#lsblk) |
| lspci | List PCI devices (#lspci) |
| lsusb | List USB devices (#lsusb) |
| lsmod | List loaded kernel modules (#lsmod) |
| modprobe <mod> | Load kernel module (#modprobe) |
| rmmod <mod> | Unload kernel module (#rmmod) |
| dmesg | Show kernel ring buffer / boot messages (#dmesg) |

Common I/O syscalls / stdio wrappers
- open(path, flags) — open file/device  
- read(fd, buf, n) — read up to n bytes  
- write(fd, buf, n) — write up to n bytes  
- ioctl(fd, request, arg) — device-specific control  
- mmap(...) — map file/device to memory  
- close(fd) — close descriptor  
- fopen/fgets/fclose — stdio convenience wrappers

I/O scheduler quick notes
- CFQ: fairness per process (good for multi-user desktop).  
- NOOP: minimal (useful for devices with their own scheduling like SSDs/NVMe).  
- deadline: prioritizes latency and prevents starvation.

Examples (shell)
- echo "hello I/O" > output.txt  # writes to output.txt  
- cat < input.txt  # read input.txt as stdin to cat  
- ls nonexist 2> error.txt  # capture error message

Tips for exams (quick)
- Remember file descriptor numbers 0/1/2.  
- Use /proc and /sys to inspect kernel/device state.  
- Choose NOOP/deadline for SSDs/NVMe when device has internal scheduling.  
- Use mmap for large, efficient file access when random access and zero-copy beneficial.  
- Device nodes in /dev map to drivers by major/minor numbers — check with ls -l /dev.

End of cheatsheet.