# Linux & Unix — Lecture Cheatsheet
#Keywords
#Linux #Unix #kernel #shell #terminal #filesystem #root #process #memorymanagement #virtualmemory #deviceDrivers #scheduling #timesharing #multitasking #processisolation #preemption #IPC #pipes #sockets #sharedmemory #messagepassing #RPC #distributions #packageManager #APT #YUM #Ubuntu #Fedora #Debian #CentOS #Arch #OpenSUSE #LinuxMint #Manjaro #Kali #openSource #stability #multiuser #backgroundJobs #Android #Darwin #WSL #VirtualBox #CourseraLabs #BourneShell #Csh #Ksh #Bash

---

## Title
Linux & Unix: Kernel, Shell, Distributions, Time‑Sharing & Core OS Services

---

## Key Definitions (one-line)
- Linux: the open-source kernel created by Linus Torvalds (1991); often used to mean the complete OS. #Linux #kernel
- Kernel: core OS component that interfaces with hardware; manages processes, memory, devices, I/O. #kernel
- Distribution (distro): a complete Linux OS bundle (kernel + tools, packages, package manager). #distributions
- Shell / Terminal: text-based command interpreter (Shell) and the terminal app/interface. #shell #terminal
- Package manager: tool to install/update/remove packages (e.g., APT, YUM). #packageManager #APT #YUM
- Time‑sharing OS: kernel design enabling multiple users/processes to share CPU via time slices. #timesharing #multitasking
- Process scheduling: mechanism to allocate CPU time among processes (scheduler). #scheduling
- Time slice / Quantum (q): allotted CPU execution interval per process. #timesharing
- Preemption: interrupting a running process to run another (usually higher priority). #preemption
- Process isolation: separation ensuring one process cannot corrupt others. #processisolation
- Virtual memory: using disk as extension of RAM so processes can exceed physical memory. #virtualmemory
- Device driver: kernel module that controls hardware devices and abstracts them for the OS. #deviceDrivers
- IPC (Inter‑process communication): mechanisms to exchange/synchronize data (pipes, sockets, shared memory, message passing, RPC). #IPC #pipes #sockets

---

## Formulas / Notations / Quick Symbols
- Time slice / quantum: q (smaller q → better responsiveness; larger q → fewer context switches) #timesharing
- Context switch overhead: cost_CS (switching too often increases CPU overhead) #scheduling
- Virtual memory mapping: virtual_address → physical_frame via page table (paging) #virtualmemory

(No heavy math in lecture; focus on symbolic reminders above.)

---

## Key Algorithms / Concepts (bulleted)
- Kernel responsibilities:
  - Process management: scheduling, context switch, preemption. #kernel #scheduling #preemption
  - Memory management: virtual memory, paging/swapping, protection. #memorymanagement #virtualmemory
  - Device management: load/init drivers, handle interrupts, I/O. #deviceDrivers
  - IPC & networking: pipes, sockets, shared memory, message passing, RPC. #IPC #sockets #pipes
- Time‑sharing / Multitasking:
  - Scheduler gives each process time slice (q); supports fairness, responsiveness. #timesharing #multitasking
  - Preemption ensures higher priority/interactive tasks run promptly. #preemption
- Multi‑user model:
  - Multiple user accounts, home directories, permissions, quotas, process isolation. #multiuser #permissions
- Shell & terminal:
  - Shells: Bourne/Bash, C Shell (csh), Korn Shell (ksh), other variants. #BourneShell #Bash #Csh #Ksh
  - Shell tasks: command execution, scripting, automation, aliases/functions. #shell
  - Background jobs: long tasks can run in background and continue after logout (via job control, nohup/screen/tmux). #backgroundJobs
- Distributions & package management:
  - Debian/Ubuntu/Mint → APT (.deb). #Debian #Ubuntu #LinuxMint #APT
  - Red Hat/CentOS/Fedora → YUM / dnf / RPM. #Fedora #CentOS #YUM
  - Arch, Manjaro, OpenSUSE, Kali, etc. — choice depends on use case. #Arch #Manjaro #OpenSUSE #Kali
- Open source ecosystem:
  - Source code availability, free redistribution, community development, OSI-licensed (GPL, MIT, Apache). #openSource

---

## Important Properties / Invariants
- Hierarchical file system with single root: / is top-level. #filesystem #root
- Multi‑user, multi‑process isolation: processes/users cannot interfere without permission. #multiuser #processisolation
- Kernel vs OS usage:
  - "Linux" = kernel (strict); "Linux OS" = kernel + userland/utilities. #kernel #Linux
- Stability & uptime: Linux designed for long uptimes; widely used for servers and embedded systems. #stability
- Portability & adaptability: kernel runs on many architectures and powers Android devices. #Android
- Security model: privilege separation (user mode vs kernel mode) and file permissions enforced. #security #permissions
- Community maintenance: rapid updates, wide driver support, large developer community. #openSource #community

---

## Quick Reference (scannable)
- Top directory: /  #root #filesystem
- Common package managers:
  - Debian-based: apt, dpkg (.deb)  #APT #Debian
  - RedHat-based: yum/dnf, rpm (.rpm)  #YUM #Fedora #CentOS
- Popular distros: Ubuntu, Fedora, Debian, CentOS, Arch, OpenSUSE, Mint, Manjaro, Kali  #distributions
- Shells: bash (default on many), sh, csh, ksh  #Bash #BourneShell #Csh #Ksh
- IPC methods: pipes | sockets | shared memory | message queues | RPC  #IPC #pipes #sockets
- Background job hints: run long tasks in background; use job control or persistent sessions (nohup/screen/tmux). #backgroundJobs
- Where to practice Linux:
  - Local VM: VirtualBox/VMware  #VirtualBox
  - Windows: WSL (Windows Subsystem for Linux)  #WSL
  - Online: Coursera Labs, cloud VMs  #CourseraLabs
  - macOS/iOS: Darwin (Unix-based) — shell access via terminal  #Darwin #MacOS #iOS
- Android: uses Linux kernel (modified for mobile)  #Android
- Kernel modes:
  - User mode: limited privileges
  - Kernel mode: full hardware access  #kernel

---

## One‑line reminders for exam
- Linux = kernel; Linux distro = kernel + userland + package manager. #Linux #distributions
- Kernel core duties: processes, memory, devices, I/O, IPC, scheduling. #kernel
- Time‑sharing uses quantums q and preemption to provide multitasking and fairness. #timesharing
- Virtual memory lets processes address more memory than physical RAM via paging/swap. #virtualmemory
- Use APT for Debian-based, YUM/dnf for RedHat-based distributions. #APT #YUM

---

End of cheatsheet — keep this page handy for quick lookup of core Linux/Unix terms, mappings, and kernel/service responsibilities.