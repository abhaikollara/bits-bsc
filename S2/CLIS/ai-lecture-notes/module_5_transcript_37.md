# Block vs Character Devices — Linux I/O Cheatsheet

#keywords
#block-device #character-device #Linux #I/O #filesystem #mount #umount #fdisk #cat #echo #stty #serial-port #stdin #tty #read #write #file-descriptor #partitioning

## Key Definitions
- Block device: I/O device that transfers data in fixed-size blocks (e.g., 512 B–4 KB); supports random block access. #block-device
- Character device: I/O device that transfers data byte-by-byte (stream); typically sequential access. #character-device
- Mount point: directory where a filesystem on a block device is attached (e.g., /mnt/mydrive). #mount
- Partition: logical section of a block device (created/managed with fdisk). #partitioning
- File descriptor (fd): integer handle for open files/devices used by read/write syscalls. #file-descriptor
- stdin: standard input stream (often points to the terminal/keyboard device). #stdin
- Device node: special file in /dev that represents a device (e.g., /dev/sda, /dev/tty). #dev

## Formulas / Notation / Syscall Signatures
- Typical block sizes: 512 B — 4 KB
- read syscall: ssize_t read(int fd, void *buf, size_t count);
- write syscall: ssize_t write(int fd, const void *buf, size_t count);

## Key Algorithms / Concepts
- Block-device usage: mounting filesystems, partitioning, direct block-level I/O. #mount #fdisk
- Character-device usage: interactive I/O, serial communication, terminal I/O. #tty #serial-port
- Partitioning with fdisk: modify partition table on a block device. #fdisk
- Device access flow (keyboard/terminal):
  - keyboard -> character device (/dev/tty) -> stdin (fd) -> program buffer -> display. #tty #stdin
- Writing to a character device: open fd (O_WRONLY), write(fd, buf, n). #write #file-descriptor

## Important Properties / Invariants
- Block devices:
  - Data accessed in fixed-size blocks.
  - Random access: any block can be read/written independently.
  - Suited for filesystems and storage devices (HDD, SSD, USB, RAID). #hdd #ssd #usb #raid
  - Device nodes typically: /dev/sdX, /dev/nvmeXnY. (e.g., /dev/sda, /dev/nvme0n1) #dev
- Character devices:
  - Data accessed byte-by-byte (stream).
  - Typically sequential access (read/write in order).
  - Suited for terminals, keyboards, mice, serial ports, audio. #keyboard #mouse #audio
  - Device nodes typically: /dev/tty, /dev/ttyS0, /dev/pts/X. #tty

## Quick Reference (Commands & Examples)
- Mounting / unmounting (block devices)
  - mount syntax: sudo mount /dev/sda1 /mnt/mydrive
  - unmount syntax: sudo umount /mnt/mydrive
  - Notes: mount attaches block-device filesystem to a mount point. #mount #umount
- Partitioning (block devices)
  - fdisk usage: sudo fdisk /dev/sda
  - Notes: create/delete/modify partitions; requires administrative privileges (sudo). #fdisk
- Reading / writing character devices (simple commands)
  - Read/display: cat /dev/tty or cat /dev/ttyS0  (reads from char device). #cat
  - Write (redirect): echo "text" > /dev/ttyS0  (writes to char device). #echo
  - Configure terminal/serial: stty -F /dev/ttyS0 <options>  (change/print line settings). #stty
- Programmatic I/O on devices
  - Open (write-only): fd = open("/dev/ttyS0", O_WRONLY);
  - Write: write(fd, buffer, len); close(fd);
- Common device-node examples:
  - /dev/sda, /dev/sda1 → block device / partition (HDD/SSD). #sda
  - /dev/nvme0n1 → NVMe block device. #nvme
  - /dev/tty, /dev/pts/* → terminal character devices. #tty #pts
  - /dev/ttyS0 → serial port character device. #serial-port

## Scannable Facts / Patterns
- Block = blocks (512B–4KB), random access, used by filesystems.
- Character = stream (bytes/chars), sequential, used by terminals/serial.
- Use sudo for mount and fdisk (requires root).
- Device nodes live under /dev — choose node based on device type.
- To interact from programs: use standard POSIX open/read/write on device file descriptors.
- Kernel exposes same interface: treat devices as files (Unix “everything is a file” model).
- To send data to a serial device: open write-only and use write(fd,...). #write

Keep this sheet handy while troubleshooting or performing device I/O tasks in Linux.