# Linux Kernel I/O & Device Management — Cheatsheet

Keywords: #LinuxKernel #I/O #IODevice #DeviceDriver #BlockDevice #CharDevice #Interrupt #DMA #VFS #udev #sysfs #proc #lsblk #fdisk #df #hwinfo #parted #major_minor #request_queue #bio #file_operations

---

## Key Definitions (one-line)
- Kernel I/O structure: the kernel layers & interfaces that route I/O from user space to hardware. #LinuxKernel #I/O  
- Block device: device that transfers data in fixed-size blocks, supports random access and buffering (e.g., disks). #BlockDevice  
- Character device: device that transfers byte streams, typically unbuffered and sequential (e.g., serial ports). #CharDevice  
- Device driver: kernel code that implements an interface between kernel subsystems and hardware. #DeviceDriver  
- Interrupt: hardware signal that informs the CPU of an event, triggering an ISR (top-half) and deferred work (bottom-half). #Interrupt  
- DMA (Direct Memory Access): hardware mechanism allowing devices to read/write memory without CPU intervention. #DMA  
- dev_t (major/minor): kernel identifier for devices; identifies driver (major) and device instance/partition (minor). #major_minor  
- VFS (Virtual File System): kernel abstraction providing uniform file/device access via file_operations. #VFS #file_operations  
- request_queue / gendisk / bio: core block-layer structures: queue of I/O requests, disk descriptor, block I/O unit. #request_queue #gendisk #bio  
- udev: userspace device manager creating /dev nodes dynamically. #udev  
- sysfs / procfs: kernel-exported virtual filesystems for device/driver information and stats. #sysfs #proc

---

## Formulas / Equations / Notation
- dev_t packing (conceptual): device = (major << 8) | minor  (platform-dependent sizing). #major_minor  
- Common notation: O(...) for algorithmic complexity (not primary here). #Complexity  
- IRQ view: Inspect -> /proc/interrupts  ; devices -> /sys/block, /sys/class. #proc #sysfs

---

## Key Algorithms / Concepts (scannable)
- Kernel I/O stack (typical flow): user syscall -> VFS -> file_operations -> block/char layer -> driver -> hardware. #VFS #file_operations #DeviceDriver
- Block-layer flow: submit_io -> bio -> request_queue -> IO scheduler -> driver -> device -> completion. #bio #request_queue
- Character-device flow: open/read/write/ioctl -> char driver callbacks (unbuffered/stream). #CharDevice
- Buffered I/O vs Direct I/O:
  - Buffered: cached in page cache, higher latency but coalescing/ordering benefits. #BufferedIO
  - Direct (O_DIRECT): bypass page cache for direct device transfers. #DirectIO
- Interrupt handling:
  - Top-half: ISR (fast, minimal work) — acknowledges device/collects minimal state. #Interrupt
  - Bottom-half: softirq/tasklet/workqueue for deferred processing. #softirq #workqueue
- Poll/select/epoll: async I/O readiness APIs that drivers implement (poll callback). #epoll
- Driver registration patterns:
  - Character: register_chrdev / cdev_add + file_operations. #CharDevice
  - Block: register_blkdev / alloc_disk / set_queue / add_disk. #BlockDevice
  - Bus drivers (PCI/platform): probe/remove callbacks, managed by bus core. #DeviceDriver #PCI
- Major/minor allocation:
  - Static (reserved majors) or dynamic (alloc_chrdev_region/alloc_blkdev). #major_minor
- IO schedulers: noop, deadline, cfq (affect reordering/throughput/latency). #IOScheduler

---

## Important Properties / Invariants
- Block devices:
  - Support random access, block-aligned I/O, usually buffered via page cache. #BlockDevice
  - Expose partitions as minor numbers. #major_minor
- Character devices:
  - Byte-stream semantics, no inherent block boundaries. #CharDevice
- Interrupts:
  - Must keep top-half minimal; avoid sleeping. Use bottom-half for heavy work. #Interrupt
  - Edge vs level triggered: driver must match controller type. #Interrupt
- Concurrency:
  - Driver callbacks may be concurrent — must protect shared state (spinlocks in IRQ context, mutexes in process context). #Concurrency
- Device nodes:
  - /dev entries map to dev_t; /sys exposes driver/device attributes for uevent/udev. #udev #sysfs
- DMA:
  - Buffers must meet alignment and zone requirements; use dma_map_* APIs. #DMA

---

## Quick Reference (commands, files, and common checks)
- Common commands:
  - lsblk — list block devices & partitions (#lsblk)  
    - Usage: lsblk -f  (shows FS, UUID, mountpoints)
  - fdisk — partition table editor (#fdisk)  
    - Usage: fdisk -l /dev/sdX
  - parted — partitioning tool (#parted)  
    - Usage: parted /dev/sdX print
  - df — filesystem disk usage (#df)  
    - Usage: df -h
  - hwinfo — hardware info (may require install) (#hwinfo)  
  - blkid — get block device UUIDs and types (#blkid)
  - cat /proc/interrupts — view IRQ counts and handlers (#proc)  
  - ls -l /dev/sd* — show major:minor in device nodes (#major_minor)
  - dmesg | tail — kernel messages (driver/IRQ logs)
  - udevadm info -a -p /sys/class/... — udev/sysfs device attributes (#udev #sysfs)
- Useful sysfs/proc paths:
  - /sys/block — block devices and attributes (#sysfs)  
  - /sys/class/net — network devices (#sysfs)  
  - /proc/interrupts — IRQ usage (#proc)  
  - /sys/devices — device tree and bus topology (#sysfs)
- Quick device-node check:
  - ls -l /dev/sda -> crw/brw ? major,minor
    - 'b' = block device, 'c' = character device (#BlockDevice #CharDevice)
- Viewing driver binding:
  - cat /sys/class/<class>/<device>/device/driver -> shows bound driver
- Common driver lifecycle hooks:
  - probe(), remove(), suspend(), resume() for bus-managed drivers. #DeviceDriver

---

## Short Patterns / Rules-of-thumb
- To differentiate: if device is accessed as fixed-size blocks and can be mounted -> likely #BlockDevice.  
- If driver needs low-latency byte stream -> likely #CharDevice.  
- Keep ISRs < few microseconds; defer work to bottom-half. #Interrupt  
- Use lsblk + blkid for disk identification; use fdisk/parted for repartitioning. #lsblk #fdisk #parted  
- For driver debugging: check dmesg, /proc/interrupts, /sys/class, then enable dynamic debug or printk. #dmesg #proc

---

Tags (repeat for easy search): #LinuxKernel #I/O #IODevice #DeviceDriver #BlockDevice #CharDevice #Interrupt #DMA #VFS #udev #sysfs #proc #lsblk #fdisk #df #hwinfo #parted #major_minor #request_queue #bio #file_operations

(Use this sheet as a quick lookup — for commands, run with sudo where appropriate; consult man pages for full option lists.)