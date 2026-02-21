# Merged AI Lecture Notes (Cheatsheets)

All lecture cheatsheets in one document. Use Ctrl+F / Cmd+F to search.

## Table of contents

### Module 2

- [Lecture 1: Linux & Unix — Lecture Cheatsheet](#module-2--lecture-1-linux--unix--lecture-cheatsheet)
- [Lecture 2: Linux CLI Basics — Day-to-day Commands (Cheatsheet)](#module-2--lecture-2-linux-cli-basics--day-to-day-commands-cheatsheet)
- [Lecture 3: Linux file editing & basic file commands — Cheatsheet](#module-2--lecture-3-linux-file-editing--basic-file-commands--cheatsheet)
- [Lecture 4: Linux text tools: wc & grep — Cheatsheet](#module-2--lecture-4-linux-text-tools-wc--grep--cheatsheet)
- [Lecture 5: File commands cheatsheet — Sort, Tail, cmp, diff](#module-2--lecture-5-file-commands-cheatsheet--sort-tail-cmp-diff)
- [Lecture 6: Linux Shell Cheatsheet](#module-2--lecture-6-linux-shell-cheatsheet)
- [Lecture 7: Linux User Session Lifecycle — Cheatsheet](#module-2--lecture-7-linux-user-session-lifecycle--cheatsheet)
- [Lecture 8: Linux Manual & Basic Commands — Cheatsheet](#module-2--lecture-8-linux-manual--basic-commands--cheatsheet)
- [Lecture 9: Linux Links & Basic File Commands — Cheatsheet](#module-2--lecture-9-linux-links--basic-file-commands--cheatsheet)
- [Lecture 10: Linux commands: touch, tr, pr — Cheatsheet](#module-2--lecture-10-linux-commands-touch-tr-pr--cheatsheet)
- [Lecture 11: Linux Networking Commands — Cheatsheet](#module-2--lecture-11-linux-networking-commands--cheatsheet)
- [Lecture 12: SSH & SCP Cheatsheet — Secure Remote Access and File Transfer](#module-2--lecture-12-ssh--scp-cheatsheet--secure-remote-access-and-file-transfer)
- [Lecture 13: Linux Fundamentals Cheatsheet](#module-2--lecture-13-linux-fundamentals-cheatsheet)

### Module 3

- [Lecture 14: Linux Files & Directories — Cheatsheet](#module-3--lecture-14-linux-files--directories--cheatsheet)
- [Lecture 15: File Permissions (Linux) — Cheatsheet](#module-3--lecture-15-file-permissions-linux--cheatsheet)
- [Lecture 16: Inodes & Linux File System Layout — Cheatsheet](#module-3--lecture-16-inodes--linux-file-system-layout--cheatsheet)
- [Lecture 17: Linux Inode & Links — Cheatsheet](#module-3--lecture-17-linux-inode--links--cheatsheet)
- [Lecture 18: Inodes & Directory Permissions (Linux) — Cheatsheet](#module-3--lecture-18-inodes--directory-permissions-linux--cheatsheet)
- [Lecture 19: Navigating & Listing Files (UNIX/Linux) — Cheatsheet](#module-3--lecture-19-navigating--listing-files-unixlinux--cheatsheet)
- [Lecture 20: File & Directory Creation and Deletion (Linux)](#module-3--lecture-20-file--directory-creation-and-deletion-linux)
- [Lecture 21: Copying & Moving Files and Directories — Cheatsheet](#module-3--lecture-21-copying--moving-files-and-directories--cheatsheet)
- [Lecture 22: File & Directory Permissions (Unix/Linux) — Cheatsheet](#module-3--lecture-22-file--directory-permissions-unixlinux--cheatsheet)
- [Lecture 23: Linux disk-usage & links — Cheatsheet](#module-3--lecture-23-linux-disk-usage--links--cheatsheet)
- [Lecture 24: Linux Files & Directories — Cheatsheet](#module-3--lecture-24-linux-files--directories--cheatsheet)
- [Lecture 25: Linux File System Cheatsheet](#module-3--lecture-25-linux-file-system-cheatsheet)

### Module 4

- [Lecture 26: Open files & File Descriptor Management — Cheatsheet](#module-4--lecture-26-open-files--file-descriptor-management--cheatsheet)
- [Lecture 27: In-memory File System (TMPFS) — Cheatsheet](#module-4--lecture-27-in-memory-file-system-tmpfs--cheatsheet)
- [Lecture 28: Linux File System Layout & Implementation — Cheatsheet](#module-4--lecture-28-linux-file-system-layout--implementation--cheatsheet)
- [Lecture 29: Superblocks — Linux file system metadata cheatsheet](#module-4--lecture-29-superblocks--linux-file-system-metadata-cheatsheet)
- [Lecture 30: Path-name to Inode (Linux) — Cheat Sheet](#module-4--lecture-30-path-name-to-inode-linux--cheat-sheet)
- [Lecture 31: Linux Links Cheatsheet — Symbolic (Soft) vs Hard Links](#module-4--lecture-31-linux-links-cheatsheet--symbolic-soft-vs-hard-links)
- [Lecture 32: Linux filesystems — Data blocks & inodes (cheatsheet)](#module-4--lecture-32-linux-filesystems--data-blocks--inodes-cheatsheet)
- [Lecture 33: Inode — Linux file metadata structure (cheatsheet)](#module-4--lecture-33-inode--linux-file-metadata-structure-cheatsheet)
- [Lecture 34: File Systems: Superblock, Inodes, and Links — Cheatsheet](#module-4--lecture-34-file-systems-superblock-inodes-and-links--cheatsheet)
- [Lecture 35: Linux filesystems & I/O cheatsheet](#module-4--lecture-35-linux-filesystems--io-cheatsheet)

### Module 5

- [Lecture 36: Kernel I/O Structure & Linux I/O Cheatsheet](#module-5--lecture-36-kernel-io-structure--linux-io-cheatsheet)
- [Lecture 37: Block vs Character Devices — Linux I/O Cheatsheet](#module-5--lecture-37-block-vs-character-devices--linux-io-cheatsheet)
- [Lecture 38: Linux Device Drivers — Cheatsheet](#module-5--lecture-38-linux-device-drivers--cheatsheet)
- [Lecture 39: I/O Queuing, I/O Scheduling & Interrupt Handling — Linux (Cheatsheet)](#module-5--lecture-39-io-queuing-io-scheduling--interrupt-handling--linux-cheatsheet)
- [Lecture 40: Partitioning & Inspecting Hard Disks in Linux — Cheatsheet](#module-5--lecture-40-partitioning--inspecting-hard-disks-in-linux--cheatsheet)
- [Lecture 41: Linux Block Devices & Disk-Utilities — Cheatsheet](#module-5--lecture-41-linux-block-devices--disk-utilities--cheatsheet)
- [Lecture 42: hwinfo & parted — Linux hardware & partition cheatsheet](#module-5--lecture-42-hwinfo--parted--linux-hardware--partition-cheatsheet)
- [Lecture 43: Disk Tools Cheatsheet — cfdisk, sfdisk, smartctl](#module-5--lecture-43-disk-tools-cheatsheet--cfdisk-sfdisk-smartctl)
- [Lecture 44: smartmontools & smartctl — Disk Health Monitoring (Linux) Cheat Sheet](#module-5--lecture-44-smartmontools--smartctl--disk-health-monitoring-linux-cheat-sheet)
- [Lecture 45: Linux Kernel I/O & Device Management — Cheatsheet](#module-5--lecture-45-linux-kernel-io--device-management--cheatsheet)
- [Lecture 46: Kernel I/O & Linux I/O Utilities — Cheatsheet](#module-5--lecture-46-kernel-io--linux-io-utilities--cheatsheet)

### Module 6

- [Lecture 47: vi Editor Cheatsheet](#module-6--lecture-47-vi-editor-cheatsheet)
- [Lecture 48: Vi Editor — Modes & Essential Commands (cheatsheet)](#module-6--lecture-48-vi-editor--modes--essential-commands-cheatsheet)
- [Lecture 49: vi/vim Quick Cheatsheet — Deleting & Common Shortcuts](#module-6--lecture-49-vivim-quick-cheatsheet--deleting--common-shortcuts)
- [Lecture 50: vi/vim Misc Commands — Cheatsheet](#module-6--lecture-50-vivim-misc-commands--cheatsheet)
- [Lecture 51: vi — Copy, Cut, Paste Cheatsheet](#module-6--lecture-51-vi--copy-cut-paste-cheatsheet)
- [Lecture 52: Searching & Substitution in vi Editor — Cheatsheet](#module-6--lecture-52-searching--substitution-in-vi-editor--cheatsheet)
- [Lecture 53: vi editor — Quick Cheatsheet](#module-6--lecture-53-vi-editor--quick-cheatsheet)
- [Lecture 54: vi/vim Editor Cheatsheet](#module-6--lecture-54-vivim-editor-cheatsheet)

### Module 7

- [Lecture 55: Vi/Vim — Auto-recovery, Backup & Version-control Cheatsheet](#module-7--lecture-55-vivim--auto-recovery-backup--version-control-cheatsheet)
- [Lecture 56: Vi/Vim Crash Recovery Cheatsheet](#module-7--lecture-56-vivim-crash-recovery-cheatsheet)
- [Lecture 57: Vi/vim: Undelete & Buffer Recovery — Cheatsheet](#module-7--lecture-57-vivim-undelete--buffer-recovery--cheatsheet)
- [Lecture 58: VA Editor / vi: Mark (Bookmark) Command — Cheatsheet](#module-7--lecture-58-va-editor--vi-mark-bookmark-command--cheatsheet)
- [Lecture 59: Standard Input Redirection (Linux) — Cheatsheet](#module-7--lecture-59-standard-input-redirection-linux--cheatsheet)
- [Lecture 60: Standard Output Redirection & Appending — Cheatsheet](#module-7--lecture-60-standard-output-redirection--appending--cheatsheet)
- [Lecture 61: Standard Error Redirection (Shell/Bash)](#module-7--lecture-61-standard-error-redirection-shellbash)
- [Lecture 62: /dev/null (Linux) — Quick Cheatsheet](#module-7--lecture-62-devnull-linux--quick-cheatsheet)
- [Lecture 63: Sort (Linux sort filter) — Cheatsheet](#module-7--lecture-63-sort-linux-sort-filter--cheatsheet)
- [Lecture 64: Linux head — Quick Cheatsheet](#module-7--lecture-64-linux-head--quick-cheatsheet)
- [Lecture 65: Linux tail command — Cheatsheet](#module-7--lecture-65-linux-tail-command--cheatsheet)
- [Lecture 66: grep Cheatsheet — Search & Filter Text in Linux](#module-7--lecture-66-grep-cheatsheet--search--filter-text-in-linux)
- [Lecture 67: Linux Pipe Command — Cheatsheet](#module-7--lecture-67-linux-pipe-command--cheatsheet)
- [Lecture 68: Linux tee — Cheatsheet](#module-7--lecture-68-linux-tee--cheatsheet)
- [Lecture 69: VI/Vim Recovery & Linux IO Redirection — Cheatsheet](#module-7--lecture-69-vivim-recovery--linux-io-redirection--cheatsheet)
- [Lecture 70: Week 7 Cheatsheet — vi editor recovery, Linux I/O redirection & common text utilities](#module-7--lecture-70-week-7-cheatsheet--vi-editor-recovery-linux-io-redirection--common-text-utilities)

### Module 8

- [Lecture 71: Shell Scripting — Cheatsheet](#module-8--lecture-71-shell-scripting--cheatsheet)
- [Lecture 72: Shell Script Basics — Quick Cheatsheet](#module-8--lecture-72-shell-script-basics--quick-cheatsheet)
- [Lecture 73: Bash Wildcards (Globbing) Cheatsheet](#module-8--lecture-73-bash-wildcards-globbing-cheatsheet)
- [Lecture 74: Shell Metacharacters & Redirection — Cheatsheet](#module-8--lecture-74-shell-metacharacters--redirection--cheatsheet)
- [Lecture 75: Shell Special Variables — Quick Reference](#module-8--lecture-75-shell-special-variables--quick-reference)
- [Lecture 76: Bash Variables — Types, Usage & Common System Variables](#module-8--lecture-76-bash-variables--types-usage--common-system-variables)
- [Lecture 77: User-defined Variables in Bash — Cheatsheet](#module-8--lecture-77-user-defined-variables-in-bash--cheatsheet)
- [Lecture 78: Interactive Shell Scripts — Read Input Cheatsheet](#module-8--lecture-78-interactive-shell-scripts--read-input-cheatsheet)
- [Lecture 79: expr (Shell) — Quick Cheatsheet](#module-8--lecture-79-expr-shell--quick-cheatsheet)
- [Lecture 80: Shell Scripting — Week 7 Cheatsheet](#module-8--lecture-80-shell-scripting--week-7-cheatsheet)

### Module 9

- [Lecture 81: Bash test / [ ] Cheatsheet](#module-9--lecture-81-bash-test----cheatsheet)
- [Lecture 82: Bash comparison-based branching — Cheatsheet](#module-9--lecture-82-bash-comparison-based-branching--cheatsheet)
- [Lecture 83: Bash conditionals cheatsheet](#module-9--lecture-83-bash-conditionals-cheatsheet)
- [Lecture 84: Case Statement (Linux shell) — Cheatsheet](#module-9--lecture-84-case-statement-linux-shell--cheatsheet)
- [Lecture 85: Bash String Operations in if Statements — Cheatsheet](#module-9--lecture-85-bash-string-operations-in-if-statements--cheatsheet)
- [Lecture 86: Bash Logical Operators & File Tests — Cheatsheet](#module-9--lecture-86-bash-logical-operators--file-tests--cheatsheet)
- [Lecture 87: Bash For-Loop Cheatsheet](#module-9--lecture-87-bash-for-loop-cheatsheet)
- [Lecture 88: Bash Loops & Flow Control — #while #until #break #continue #bash](#module-9--lecture-88-bash-loops--flow-control--while-until-break-continue-bash)
- [Lecture 89: Arrays in Bash — Declaration, Initialization, Access, and Operations](#module-9--lecture-89-arrays-in-bash--declaration-initialization-access-and-operations)
- [Lecture 90: Bash Arrays — Advanced Operations (cheatsheet)](#module-9--lecture-90-bash-arrays--advanced-operations-cheatsheet)
- [Lecture 91: Bash File Handling — Reading & Writing Cheatsheet](#module-9--lecture-91-bash-file-handling--reading--writing-cheatsheet)
- [Lecture 92: Shell Scripting Cheatsheet (Decision making, loops, arrays, I/O)](#module-9--lecture-92-shell-scripting-cheatsheet-decision-making-loops-arrays-io)

### Module 10

- [Lecture 93: Processes & Process States (Linux) — Cheatsheet](#module-10--lecture-93-processes--process-states-linux--cheatsheet)
- [Lecture 94: Kernel vs User Mode — Cheatsheet](#module-10--lecture-94-kernel-vs-user-mode--cheatsheet)
- [Lecture 95: Process Creation & OS Services — Cheatsheet](#module-10--lecture-95-process-creation--os-services--cheatsheet)
- [Lecture 96: Fork (process creation) — Cheatsheet](#module-10--lecture-96-fork-process-creation--cheatsheet)
- [Lecture 97: Process coordination: parent/child, fork/wait/exec cheatsheet](#module-10--lecture-97-process-coordination-parentchild-forkwaitexec-cheatsheet)
- [Lecture 98: Signals & Signal Handlers (Linux) — Cheatsheet](#module-10--lecture-98-signals--signal-handlers-linux--cheatsheet)
- [Lecture 99: Signals (raise / kill) — Cheatsheet](#module-10--lecture-99-signals-raise--kill--cheatsheet)
- [Lecture 100: System Call vs Function Call — Cheatsheet](#module-10--lecture-100-system-call-vs-function-call--cheatsheet)
- [Lecture 101: Processes, Lifecycle, fork/exec, wait, and Signals — Cheatsheet](#module-10--lecture-101-processes-lifecycle-forkexec-wait-and-signals--cheatsheet)

### Module 11

- [Lecture 102: Low-level File I/O (Linux) — Cheatsheet](#module-11--lecture-102-low-level-file-io-linux--cheatsheet)
- [Lecture 103: File I/O: read, write, and random access (#fileio #read #write #lseek #filedescriptor #sequentialaccess #randomaccess #EOF #error #systemcall)](#module-11--lecture-103-file-io-read-write-and-random-access-fileio-read-write-lseek-filedescriptor-sequentialaccess-randomaccess-eof-error-systemcall)
- [Lecture 104: Linux System Administration — Advanced Commands (cheatsheet)](#module-11--lecture-104-linux-system-administration--advanced-commands-cheatsheet)
- [Lecture 105: Linux Group Management — Cheatsheet](#module-11--lecture-105-linux-group-management--cheatsheet)
- [Lecture 106: Low-level I/O & Admin Commands — Cheatsheet](#module-11--lecture-106-low-level-io--admin-commands--cheatsheet)

---

## Module 2 — Lecture 1: Linux & Unix — Lecture Cheatsheet

#Keywords
#Linux #Unix #kernel #shell #terminal #filesystem #root #process #memorymanagement #virtualmemory #deviceDrivers #scheduling #timesharing #multitasking #processisolation #preemption #IPC #pipes #sockets #sharedmemory #messagepassing #RPC #distributions #packageManager #APT #YUM #Ubuntu #Fedora #Debian #CentOS #Arch #OpenSUSE #LinuxMint #Manjaro #Kali #openSource #stability #multiuser #backgroundJobs #Android #Darwin #WSL #VirtualBox #CourseraLabs #BourneShell #Csh #Ksh #Bash

---

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

---

## Module 2 — Lecture 2: Linux CLI Basics — Day-to-day Commands (Cheatsheet)

#keywords
#Linux #CLI #commandline #terminal #stty #who #whoami #date #pwd #man #mail #write #tabs #tabcompletion #history #logout #CtrlC #CtrlU #CtrlD

---

## Key Definitions
- Command: a text instruction given to the OS to perform a task.  
- Terminal / CLI: text-based interface to enter commands.  
- Prompt: the shell marker (e.g., $) — do not type it.  
- Echo: terminal setting that shows typed characters; turned off for passwords.  
- Tab completion: pressing Tab to auto-complete file/command names.  
- Manual (man): built-in documentation for commands and options.  

---

## Formulas / Notation
- RETURN = Enter key (execute command)
- Control notation: Ctrl-X shown as Ctrl+X (e.g., Ctrl+D)  
- stty syntax examples:
  - stty -echo        (turn echo off)
  - stty echo         (turn echo on)
  - stty sane         (restore defaults)
  - stty intr ^C      (set interrupt char to Ctrl+C)  
  (Options and arguments are case-sensitive.)

---

## Key Commands & Concepts
- who
  - Purpose: list currently logged-in users and their login times/sessions.  
  - Syntax: who
- whoami (or who am I)
  - Purpose: show current user identity.  
  - Syntax: whoami  or  who am i
- date
  - Purpose: display current date & time.  
  - Syntax: date
- pwd
  - Purpose: print current working directory.  
  - Syntax: pwd
- man
  - Purpose: display manual pages and options for a command.  
  - Syntax: man <command>  (e.g., man who)
- mail
  - Purpose: read/send system mail (simple client).  
  - Syntax: mail                 (read)  
           mail <user@host>     (send; Ctrl+D to finish body)
- write
  - Purpose: send a message to another logged-in user.  
  - Syntax: write <username> <tty?>  (user must be logged in)
- stty
  - Purpose: view/modify terminal settings (echo, control chars, tabs).  
  - Syntax: stty             (view)  
           stty -echo        (disable echo)  
           stty echo         (enable echo)  
           stty sane         (reset to sane defaults)  
           stty intr ^C      (set interrupt char)
- tabs
  - Purpose: set/reset terminal tab stops.  
  - Syntax: tabs -0   (reset)  tabs -8  (set standard 8-col tabs)
- Tab completion
  - Behavior: press Tab to complete filenames/commands or list matches.
- history
  - Purpose: list previously-entered commands.  
  - Syntax: history
- Logout
  - Ctrl+D (EOF) to log out, or type exit / logout

---

## Important Properties / Invariants
- Commands and stty options are case-sensitive.  
- Do not type the shell prompt symbol ($) when entering commands.  
- Password input: echo is off (characters not displayed).  
- Ctrl+D sends EOF — commonly logs out of shell or ends input (e.g., mail).  
- Ctrl+U kills the entire current input line (before Enter).  
- Backspace removes last character; arrow keys move cursor for editing.  
- Tab completion and history speed up command entry.  
- Use man pages to discover options; commands often have many flags.

---

## Quick Reference (scannable)

Commands:
- who        — list logged-in users
- whoami     — current username
- date       — show date/time
- pwd        — show present working directory
- man <cmd>  — manual for <cmd> (e.g., man who)
- mail       — read system mail
- mail addr  — send mail to addr (end body with Ctrl+D)
- write user — send message to logged-in user
- history    — show past commands
- exit/logout / Ctrl+D — log out

stty (common):
- stty              — show terminal settings
- stty -echo        — turn off echo (useful for passwords)
- stty echo         — turn on echo
- stty sane         — restore defaults
- stty intr ^C      — set interrupt to Ctrl+C (case-sensitive)

Tabs & completion:
- tabs -0           — reset tab stops
- tabs -8           — set 8-column tabs
- Tab               — auto-complete filenames/commands

Line editing / control keys:
- Ctrl+U            — kill whole input line
- Ctrl+D            — send EOF / logout
- Ctrl+C            — interrupt current process (if configured)
- Backspace         — delete previous character
- ← / →             — move cursor within line

Manual options (example: who):
- who -a            — all
- who -b            — boot time
- who -d            — dead processes
- who -H            — show headings

Notes:
- If terminal behaves oddly, inspect stty and use stty sane to recover.  
- Use Coursera Labs / terminal emulator to practice commands interactively.

---

#hashtags (summary)  
#Linux #CLI #terminal #stty #tabcompletion #history #man #mail #write #pwd #who #whoami #date #logout #lineediting #controlchars


---

## Module 2 — Lecture 3: Linux file editing & basic file commands — Cheatsheet

#keywords: #vi #vim #ls #pr #mkdir #mv #cp #rm #cd #pwd #hidden-files #tab-completion #file-colors #human-readable #sorting #insert-mode #command-line

---

## Key Definitions
- vi filename — open file in VI (modal) editor. #vi #vim  
- Insert mode — VI mode for typing text (entered with i). #insert-mode  
- Normal mode — VI mode for commands (press ESC to enter). #vi  
- ls — list directory contents. #ls  
- pr — paginate/print file contents with options for page length, header, line numbers. #pr  
- mkdir name — create a directory. #mkdir  
- mv src dst — move/rename file or directory. #mv  
- cp src dst — copy file or directory. #cp  
- rm file — remove (delete) a file (permanent). #rm  
- cd dir — change current directory; cd .. goes to parent. #cd  
- pwd — print working directory (current path). #pwd  
- Hidden files — filenames starting with . (dot); shown by ls -a. #hidden-files  
- Tab-completion — press Tab to auto-complete filenames/paths. #tab-completion

---

## Formulas / Notation
- Command syntax: command [options] [arguments]  
- Combine options: ls -l + -h + -a => ls -lha

---

## Key Commands & Options (scannable)
- vi filename
  - i — enter Insert mode. #vi #insert-mode
  - ESC :w — save file. #vi
  - ESC :wq — save and quit. #vi
- ls
  - ls -l — long listing (permissions, owner, group, size, mod time). #ls
  - ls -a — show hidden files (dotfiles). #ls #hidden-files
  - ls -h — human-readable sizes (with -l: 6K, 2M, etc.). #human-readable
  - ls -t — sort by modification time (newest first). #sorting
  - Combine: ls -lha — long + human-readable + all. #ls
  - Color meaning (common defaults): blue = directory, green = executable, white = regular file. #file-colors
- pr
  - pr -l N filename — set lines per page to N (default 66). #pr
  - pr -h "Header" filename — set/modify header. #pr
  - pr -n filename — number lines. #pr
  - Options can be combined (e.g., pr -n -l 3 file). #pr
- mkdir name — create directory. #mkdir
- mv src dst — move or rename file/directory (use full/relative paths). #mv
- cp src dst — copy file to destination. #cp
- rm filename — permanently delete file (no recycle). Use with caution. #rm
- cd path — change directory; cd .. = parent, cd . = current. #cd
- pwd — show current directory path. #pwd

---

## Important Properties / Invariants
- VI is modal: must switch modes (Insert vs Normal) to edit vs issue commands. #vi #insert-mode
- ls -l shows permission string (e.g., -rwxr-xr-x), owner, group, size, timestamp. #ls
- Hidden files begin with '.' and are not shown unless using -a. #hidden-files
- Tab-completion speeds navigation and reduces typing errors. #tab-completion
- mv moves (removes source from origin) while cp leaves original intact. #mv #cp
- rm permanently deletes files — no undo by default. Back up critical files. #rm
- Options can be combined; order usually irrelevant for POSIX utilities. #ls #pr

---

## Quick Reference (one-line facts)
- Open VI: vi file.txt
- Insert text: In Normal mode press i → type → ESC to stop inserting
- Save: ESC :w
- Save & quit: ESC :wq  (or :x)
- Quit without saving: ESC :q! 
- List files: ls
- List long: ls -l
- Show hidden: ls -a
- Human sizes: ls -lh
- Sort by time: ls -lt (or ls -t)
- All options: ls -lha (long + human + all)
- Show current dir: pwd
- Change dir: cd target_dir
- Create dir: mkdir name
- Move file: mv file target_dir/
- Copy file: cp file target_dir/
- Remove file: rm file
- Print file with page length: pr -l N file
- Number lines: pr -n file
- Set header: pr -h "Header" file

---

## Safety Tips
- Double-check target paths before mv, cp, rm. #mv #cp #rm  
- Use backups or version control for important files.  
- Use ls to verify before/after file operations. #ls

---

Tags for quick find: #vi #vim #ls #pr #mkdir #mv #cp #rm #cd #pwd #hidden-files #tab-completion #file-colors #human-readable #sorting

---

## Module 2 — Lecture 4: Linux text tools: wc & grep — Cheatsheet

#hashtags: #wc #grep #linux #commandline #textprocessing #regex #BRE #ERE #pipes #shell

---

## Key Definitions
- wc: count lines, words, and bytes/characters in files or stdin. (#wc)
- grep: search for lines matching a pattern or regular expression in files or streams. (#grep #regex)
- Pattern: string or regular expression passed to grep. (#pattern)
- BRE / ERE: Basic / Extended Regular Expressions used by grep (-E for ERE). (#BRE #ERE)
- Fixed-string: literal string matching (grep -F). (#fixedstring)

---

## Formulas / Syntax (quick)
- wc basic: wc [options] [file...]
  - Default output: <lines> <words> <bytes> <file>
  - Example: `6 18 93 employee.txt` ⇒ 6 lines, 18 words, 93 bytes/characters
  - Flags: -l (lines), -w (words), -c (bytes), -m (characters)
- grep basic: grep [options] PATTERN [file...]
  - With stdin: command | grep PATTERN
  - Recursive: grep -r PATTERN dir/
  - Extended regex: grep -E PATTERN
  - Fixed strings: grep -F PATTERN
- Complexity: O(n) in input size for both tools (scan input once).

---

## Key Algorithms / Concepts
- #wc:
  - wc -l file : count lines
  - wc -w file : count words
  - wc -c file : count bytes
  - wc -m file : count characters (multibyte-aware)
  - Multiple files: prints counts per file + total
  - Use with pipe: somecommand | wc -l  (count lines of output)
- #grep:
  - grep PATTERN file : show lines containing PATTERN
  - grep -i : case-insensitive search
  - grep -r : recursive search through directories
  - grep -v : invert match (show non-matching lines)
  - grep -n : prefix each matching line with its line number
  - grep -l : list file names that contain matches
  - grep -w : match whole words only
  - grep -c : count matching lines per file
  - grep -o : print only matching part(s) of line
  - grep -E / -F : use extended regex / fixed-strings
  - Common use: piped filtering (e.g., ps aux | grep process)

---

## Important Properties / Invariants
- grep is line-oriented: returns whole matching lines (unless -o).
- By default grep matches substrings (use -w to restrict to whole words).
- grep uses basic regex (BRE) by default; -E enables ERE.
- Case sensitive by default (use -i to ignore case).
- Exit codes: 0 = match found, 1 = no match, 2 = error.
- wc default order: lines, words, bytes. Use flags to select specific counts.
- Use -m (characters) vs -c (bytes) when multi-byte characters (UTF-8) matter.

---

## Quick Reference (options)
- wc:
  - -l : lines
  - -w : words
  - -c : bytes
  - -m : characters
- grep:
  - -i : case-insensitive
  - -r / -R : recursive
  - -v : invert match
  - -n : show line numbers
  - -l : list matching file names only
  - -w : match whole words
  - -c : count matching lines
  - -o : output only matched text
  - -E : extended regex (egrep)
  - -F : fixed-string (fgrep)
  - --color=auto : highlight matches

---

## Quick Examples
- wc:
  - `wc file.txt` → prints "<lines> <words> <bytes> file.txt"
  - `wc -l file.txt` → number of lines
  - `ls | wc -l` → number of items in current directory
- grep:
  - `grep "00" employee.txt` → lines containing "00"
  - `grep -n "00" employee.txt` → same + line numbers
  - `grep -i "error" *.log` → case-insensitive across files
  - `grep -r "TODO" src/` → recursive search in src/
  - `grep -v "header" file.txt` → show lines that do NOT contain "header"
  - `grep -o "pattern" file | wc -l` → count total matches (not just lines)

---

## Tips / Pitfalls
- Use -w to avoid substring matches (e.g., "art" matching "start").
- For Unicode characters, -m (chars) differs from -c (bytes).
- grep -r follows directory traversal; use --exclude / --include to filter files.
- Combine tools: grep → cut/awk/sed → wc for more complex pipelines.
- Reference: `man grep` and `man wc` for full option lists and behavior.

---

End of cheatsheet — keep this nearby during exams for quick lookup.

---

## Module 2 — Lecture 5: File commands cheatsheet — Sort, Tail, cmp, diff

#hashtags: #linux #shell #file-commands #sort #tail #cmp #diff #text-processing #files

## Key Definitions
- sort: Sort lines of text (default: ascending, lexicographic).  
- tail: Show last part of a file (commonly last lines).  
- cmp: Compare two files byte-by-byte; reports first difference (byte & line).  
- diff: Show line-by-line differences between text files (various output formats).

## Syntax / quick examples
- sort: `sort filename`  
- tail: `tail -n <lines> filename` , `tail -f filename`  
- cmp: `cmp file1 file2`  
- diff: `diff file1 file2`

## Flags / Options (concise)
- sort
  - `-r` : reverse order (#reverse)  
  - `-n` : numeric sort (#numeric)  
  - `-u` : unique — output each line once (#unique)  
  - `-k <n>` : sort by field/column number (#field-sort)  
  - `-t <sep>` : set field separator for column-based sort (#separator)
- tail
  - `-n <N>` : show last N lines (#lines)  
  - `-f` : follow file as it grows (realtime) (#follow)
- cmp
  - `-l` : list byte differences with decimal values (#bytes)  
  - `-b` : show differing bytes in octal (#octal)  
  - `-i <N>` : skip first N bytes in both files before comparing (#skip)
  - Behavior: no output → files identical (per transcript)
- diff
  - `-c` : context format (#context)  
  - `-u` : unified format (#unified)  
  - `-r` : recursively compare directories (#recursive)

## Important properties / invariants
- sort does not modify the original file by default; it prints sorted output to stdout (transcript demo).  
- tail shows the last lines; `-f` streams updates without re-reading full file.  
- cmp reports the first differing byte and line number; useful for exact (byte) equality checks.  
- diff reports textual (line-level) differences and supports multiple output formats for patches/reads.  
- Skipping bytes in cmp (`-i`) shifts the comparison offset; first difference reported is after skip.

## Quick reference table
| Command | Purpose | Common flags | Typical use |
|---|---:|---|---|
| sort | Sort lines of a file | `-r`, `-n`, `-u`, `-k <n>`, `-t <sep>` | Sort by column, remove dupes |
| tail | Show last lines / follow file | `-n <N>`, `-f` | View recent log entries |
| cmp | Byte-by-byte file compare | `-l`, `-b`, `-i <N>` | Detect first byte difference |
| diff | Line-by-line differences | `-c`, `-u`, `-r` | Produce patches / compare directories |

## Quick patterns / rules to remember
- To view sorted output but keep file unchanged: `sort file` (redirect to overwrite if wanted). #sort  
- To view last 10 lines (default 10): `tail file` or specific: `tail -n 2 file`. #tail  
- Follow logs in realtime: `tail -f /var/log/syslog`. #tail #follow  
- Exact binary check: `cmp a b` — no output = identical (per lecture). #cmp  
- Skip first N bytes in cmp: `cmp -i N a b` (comparison starts at byte N+1). #cmp #skip  
- Human-friendly diff: `diff -u a b` (unified) — common for patches. #diff #unified

## Searchable hashtags (for exam lookup)
#linux #shell #file-commands #sort #tail #cmp #diff #text-processing #sorting #reverse #numeric #unique #field-sort #separator #lines #follow #bytes #octal #skip #context #unified #recursive

(Concise reference derived from lecture demo: sort, tail, cmp, diff — flags and behaviors above.)

---

## Module 2 — Lecture 6: Linux Shell Cheatsheet

#hashtags
#LinuxShell #terminal #terminal_emulator #GNOMEterminal #KDEconsole #xterm #Bash #Zsh #Fish #prompt #root #user #absolute_path #relative_path #paths #slash #tab_completion #command_history

## Key Definitions
- Linux Shell: Command-line interface to execute commands and manage system resources. #LinuxShell  
- Terminal emulator: GUI program that provides an interface to a shell (e.g., GNOME Terminal). #terminal_emulator  
- Shell types: Implementations of the shell command interpreter (Bourne Again Shell/Bash, Z shell/Zsh, Fish). #Bash #Zsh #Fish  
- Prompt: Visible shell cue; indicates user type and readiness for input. #prompt  
- Root (superuser): System administrator account (prompt ends with #). #root  
- Regular user: Normal account (prompt typically ends with $). #user  
- Absolute path: Full path from root (starts at /). #absolute_path  
- Relative path: Path relative to current directory (does not start with /). #relative_path  
- Tab completion: Press Tab to auto-complete commands, options, filenames, or list possible matches. #tab_completion  
- Command history: Previously run commands accessible via up/down arrow keys. #command_history

## Formulas / Notation
- Path separator: /  (UNIX-style) #slash  
- Absolute path example: /home/user/documents/fite.dxt  (#absolute_path)  
- Relative path example (from /home/user): documents/fite.dxt  (#relative_path)  
- Prompt symbols: Regular user -> ends with $ ; Root -> ends with #  (#prompt #root #user)

## Key Algorithms / Concepts
- Terminal ↔ Shell: Terminal emulator (GNOME Terminal, KDE Console, xterm) hosts the shell. #terminal_emulator #GNOMEterminal #KDEconsole #xterm  
- Shell types:
  - Bash (Bourne Again Shell): common default shell. #Bash  
  - Zsh: extended features over Bash. #Zsh  
  - Fish: interactive-friendly, syntax highlighting & autocompletion. #Fish  
- Prompt detection: Use trailing symbol to infer user type ($ = regular, # = root). #prompt #root #user  
- Path addressing:
  - Absolute path: start with / (root) and list full directories to file. #absolute_path  
  - Relative path: from current working directory; shorter and context-sensitive. #relative_path  
- Tab completion behavior:
  - Single match -> completes text.  
  - Multiple matches -> lists possible options for selection. #tab_completion  
- Command history navigation: Up/Down arrow to scroll previous commands; re-run or edit. #command_history

## Important Properties / Invariants
- / is the directory separator in Linux paths. #slash  
- Absolute paths start with /; relative paths do not. #absolute_path #relative_path  
- Prompt trailing character indicates privilege: $ (regular), # (root). #prompt  
- Tab completion speeds typing and reduces errors; ambiguous prefixes show choices. #tab_completion  
- Terminal emulator only provides UI; the shell actually interprets commands. #terminal_emulator

## Quick Reference (scannable)
- Terminals: GNOME Terminal | KDE Console | xterm  (#GNOMEterminal #KDEconsole #xterm)  
- Shells: Bash | Zsh | Fish  (#Bash #Zsh #Fish)  
- Prompt symbols:
  - user: ...$  (#user)  
  - root: ...#  (#root)  
- Path rules:
  - Absolute: starts with / → /path/to/file  (#absolute_path)  
  - Relative: from current dir → path/to/file  (#relative_path)  
  - Separator: /  (#slash)  
- Tab completion:
  - Hit Tab while typing command/filename/options  
  - Single completion → auto-fill  
  - Multiple → list choices  (#tab_completion)  
- Command history: Up-arrow = previous command, Down-arrow = next command  (#command_history)

Keep this sheet for quick lookup of shell types, prompt conventions, and path/addressing basics during open-book exams.

---

## Module 2 — Lecture 7: Linux User Session Lifecycle — Cheatsheet

#keywords: #Linux #login #session #authentication #SSH #TTY #GDM #LightDM #PAM #MFA #shell #Bash #startup-scripts #/etc/passwd #/etc/shadow #logout #processes

---

## Key Definitions
- User initiation: user starts a login via GUI, TTY, or remote client (SSH). #UserInitiation
- Authentication: verifying credentials by comparing entered password to stored (hashed) password. #Authentication
- Multi-factor Authentication (MFA): additional factor(s) beyond password (e.g., mobile OTP, biometrics). #MFA
- Session initialization: system sets up user environment and runs startup scripts. #SessionInitialization
- Shell assignment: shell specified for the user (e.g., /bin/bash) used as the command interpreter. #ShellAssignment
- Login shell vs interactive/non-login shell: different startup script order and behavior. #LoginShell
- Logout / cleanup: termination of session, signaling/killing user processes and freeing resources. #Logout

---

## Lifecycle (compact flow)
user initiation -> authentication -> session initialization -> shell assignment -> user session (use) -> logout -> cleanup
- Notation: Initiation (GUI/TTY/SSH) → Auth (PAM + /etc/shadow) → Init (env + startup scripts) → Shell (/etc/passwd shell) → Active → Logout (SIGHUP, kill user processes)

---

## Formulas / Notation / Fields
- /etc/passwd entry format:
  username:password:UID:GID:GECOS:home:shell
  - Note: password field usually "x" and hashed password stored in /etc/shadow. #/etc_passwd #/etc_shadow
- Common env vars: USER, UID, HOME, SHELL, PATH, LOGNAME. #Environment
- SSH command: ssh user@host  (secure remote login). #SSH

---

## Key Algorithms / Concepts (bulleted)
- User initiation methods:
  - Graphical: GDM, LightDM (display managers). #GDM #LightDM #DisplayManager
  - Local text: TTY virtual consoles (Ctrl+Alt+F1..F7). #TTY
  - Remote: SSH (secure shell). #SSH
- Authentication pipeline:
  - Password verification against hashed entry in /etc/shadow via PAM. #PAM #/etc_shadow
  - Optional MFA step integrated via PAM modules. #MFA
- Session initialization:
  - System loads global and user configs, sets env vars, mounts home (if networked), creates session leader. #SessionInitialization
- Shell assignment and startup scripts:
  - Login shell sequence (common for Bash): /etc/profile → ~/.bash_profile → ~/.bash_login → ~/.profile
  - Interactive non-login shells: ~/.bashrc
  - ~/.bash_profile often sources ~/.bashrc for consistency. #Bash #StartupScripts
- Logout & cleanup:
  - Session termination sends SIGHUP to session processes; system may forcibly kill remaining processes (pkill -u USER). #SIGHUP #Cleanup
  - Session management tools: systemd-logind (loginctl), display manager teardown. #systemd #loginctl

---

## Important Properties / Invariants
- Passwords are stored hashed (never plaintext) — compare hashes during auth. #Hashing
- User processes run with user UID/GID and limited privileges. #UID #GID
- Shell assigned in /etc/passwd determines interpreter for user sessions. #ShellAssignment
- PAM + modules control authentication, account, session, password management. #PAM
- GUI logins start display/session managers (X/Wayland); TTY sessions have a controlling terminal. #X #Wayland #TTY
- On logout, session leader termination usually causes child processes to receive SIGHUP. #SIGHUP

---

## Quick Reference (commands, files, checks)
Files:
- /etc/passwd — account records (shell field). #/etc_passwd
- /etc/shadow — hashed passwords. #/etc_shadow
- /etc/pam.d/ — PAM configuration. #PAM
- /etc/profile, ~/.profile, ~/.bash_profile, ~/.bashrc — startup scripts. #StartupScripts

Commands:
- ssh user@host — remote login. #SSH
- whoami / id — show current user / UID/GID. #whoami #id
- who / w / last — who is logged in / recent logins. #who #w #last
- loginctl list-sessions — systemd session list. #loginctl
- ps -u username / pkill -u username — list/kill user processes. #ps #pkill
- logout / exit / Ctrl-D — end a shell session. #logout
- getent passwd username — view passwd entry via NSS. #getent

Checks / quick facts:
- Where is the hashed password? /etc/shadow (requires root). #/etc_shadow
- How is shell set? 7th field in /etc/passwd. #/etc_passwd
- Which scripts run for login shell? /etc/profile then user's login scripts. #LoginShell
- How are GUI sessions started? Display manager (GDM/LightDM) spawns user session (X/Wayland). #GDM #LightDM
- How to force-logoff user processes? pkill -u username or killall -u username. #pkill

---

## Short Troubleshooting Tips
- Can't login remotely: test network + sshd status (systemctl status sshd). #sshd
- Wrong shell: check /etc/passwd entry; change with chsh. #chsh
- Env vars missing on GUI login: ensure display manager sources correct profile scripts. #Environment
- Persisting background processes after logout: check nohup, screen/tmux sessions, or systemd user services. #nohup #screen #tmux #systemd

---

Tags included for quick search: #Linux #login #session #authentication #SSH #TTY #GDM #LightDM #PAM #MFA #shell #Bash #startup-scripts #/etc_passwd #/etc_shadow #logout #processes #systemd #loginctl


---

## Module 2 — Lecture 8: Linux Manual & Basic Commands — Cheatsheet

#hashtags: #linux #man #manual #passwd #date #who #whoami #write #adduser #sudo #su #users #timezones #format

---

## Key Definitions
- man: The manual-page viewer for commands/programs (#man #manual)  
- passwd: Change a user's password (#passwd #password)  
- date: Display or set system date/time; supports format specifiers (#date #time #format)  
- who: Show currently logged-in users and related info (#who)  
- whoami: Print current effective username (alias: who am i) (#whoami)  
- write: Send a message to another logged-in user/TTY (#write)  
- adduser: Create a new user account (usually via sudo) (#adduser)  
- sudo: Run a command with administrative privileges (#sudo)  
- su: Switch user / start a login shell for another user (#su)

---

## Formulas / Notation
- man syntax: man [options] <command>
- passwd syntax: passwd [options] [user]
- date syntax (display custom): date +"%<specifier> %<specifier> ..."  (enclose format in quotes)
- who syntax: who [options]
- write syntax: write <username> [tty]
- adduser: sudo adduser <username>
- su-login: su - <username>

---

## Man pages (manual) — Key Options & Behavior (#man)
- man <command> : open manual page for command  
- man -k <keyword> : search keyword in man descriptions (apropos)  
- man -f <command> : short description (whatis)  
- man -a <command> : show all manual pages for command (from all sections/packages)  
- man -w <command> : print path(s) to manual page file(s)  
- man -h / man --help : show help for man itself (also common for most commands)  
- man <section> <name> : show man page in specific section (see sections table)

Man sections (commonly used)
- Section 1 — User commands (#man-section-1)  
- Section 2 — System calls (#man-section-2)  
- Section 3 — Library functions (#man-section-3)

Example: man 1 wc -> command wc; man 3 cw -> library function (may be not present)

---

## passwd (change password) — Quick facts (#passwd)
- passwd : change current user's password (prompts: current, new, confirm)  
- sudo passwd <user> : change another user's password (requires sudo)  
- Options:  
  - -l : lock account password  
  - -u : unlock account password  
  - -d : delete password (disable password)  
  - -e : set password to expire

Notes: password input is not echoed; policy/length enforced by PAM.

---

## date (display / set date & time) — Format tokens (#date #time #format)
- Default: date -> prints current date/time in default format  
- Custom: date +"%A %d %B %Y"  -> e.g., Monday 07 August 2023  
- Common specifiers:
  - %a : abbreviated weekday name (Sun)  
  - %A : full weekday name (Sunday)  
  - %b / %h : abbreviated month name (Aug)  
  - %B : full month name (August)  
  - %d : day of month (01..31)  
  - %H : hour (00..23) — 24-hour  
  - %I : hour (01..12) — 12-hour (transcript used lowercase l for 12h; common is %I)  
  - %M : minute (00..59)  
  - %S : second (00..60)  
  - %Y : year with century (2023)  
  - %y : year without century (23)  
  - %Z : time zone name (UTC, etc.)  
- Setting system date: date requires appropriate privileges (sudo/root)

---

## who / whoami — Usage & Options (#who #whoami)
- who : list logged-in users (username, tty, login time, host)  
- who -a : show all available information (inclusive output)  
- who -b : show last system boot time  
- who -d : show dead processes / abandoned sessions  
- who -l : (transcript) omit hostname/terminal (note: behavior may vary)  
- who -q : quick list + count of logged-in users  
- who -T : display time of last system activity (transcript)  
- who -u : show users and process status (including processes still running)  
- who -H : show header line  
- who -w : display without terminal information (transcript)  
- whoami / who am i : print the current user name (effective user)

---

## write — Send message to logged-in user (#write)
- Syntax: write <username> [tty]  
- Requirements: recipient must be logged in and message writing allowed on their TTY  
- Example: write student pts/1  (then type message; Ctrl-D to end)  
- Use-case: quick terminal-to-terminal messaging on multi-user systems

---

## adduser / sudo / su — Creating & switching users (#adduser #sudo #su)
- sudo adduser <username> : create a new user (prompts for password & details)  
  - creates home directory, group, prompts for user info  
- sudo : run command as root (prompts for caller password)  
- su - <username> : switch to user account with login shell (use to test login / open user session)

---

## Important Properties & Invariants
- man shows per-section documentation; same name can have multiple manual pages (use man -a)  
- man -k is keyword search (useful if you don't know exact command)  
- passwd requires current password for non-root users; sudo allows root to change others' passwords  
- date format specifiers must be prefixed by % and enclosed in quotes to avoid shell expansion  
- who only reports currently logged-in terminal sessions; remote users and background processes appear per options  
- write only works if recipient's terminal allows messages (mesg toggle) and the user is logged in on specified tty

---

## Quick Reference (one-liners & examples)
- Open manual: man ls  
- Search manual pages for keyword "disk": man -k disk  
- Short description: man -f ls  
- Show all man pages for a name: man -a man  
- Print man page path: man -w passwd

- Change own password: passwd  
- Change another's password: sudo passwd alice  
- Lock account: sudo passwd -l username

- Show date: date  
- Custom date: date +"%A %d %B %Y"  -> Monday 07 August 2023  
- Set date (requires sudo/root): sudo date -s "2023-08-07 14:00:00"

- List logged-in users: who  
- Quick user count: who -q  
- Show boot time: who -b  
- Current user: whoami   (or who am i)

- Send message: write <username> [pts/X]  (Ctrl-D to end message)  
- Create user: sudo adduser student  
- Switch to user: su - student

---

Keep this sheet by your terminal for fast lookup: search tags like #man, #passwd, #date, #who, #write, #adduser.

---

## Module 2 — Lecture 9: Linux Links & Basic File Commands — Cheatsheet

#hashtags: #linux #bash #commands #ln #hardlink #symlink #inode #pwd #ls #filesystem #directory #file #file-management

---

## Key Definitions (one-line)
- ln: create a link (hard or symbolic) between files/directories. #ln  
- hard link: an additional directory entry pointing to the same inode/data blocks as the original file. #hardlink  
- symbolic link (symlink): a special file that stores a pathname referencing another file/directory. #symlink  
- inode: filesystem metadata structure representing a file’s data blocks and attributes (shared by hard links). #inode  
- pwd: print working directory — shows current absolute path. #pwd  
- ls: list directory contents. #ls

---

## Syntax / Quick Examples
- Create hard link: ln <source> <target>  
  Example: ln ./TWO/employee.txt emp
- Create symbolic link: ln -s <source> <target>  
  Example: ln -s ./TWO/employee.txt semp
- Print working directory: pwd
- List files: ls [options] [directory]  
  Example: ls -lha TWO

---

## Important Properties / Invariants
- Hard link:
  - Shares same inode as original → same data blocks and inode metadata (link count increases). #hardlink #inode
  - Modifying data via any hard link changes the same underlying file data.
  - Deleting one hard link removes one directory entry; file data remains until link count = 0.
  - Cannot (normally) cross filesystem boundaries (source and target must be same filesystem). #filesystem
  - Generally cannot create hard links to directories (restricted to avoid cycles).
- Symbolic link:
  - Is a separate file containing path to target; does not share inode/data blocks of target. #symlink
  - Can point across filesystems and to non-existent targets (dangling symlink).
  - If target is deleted, symlink becomes broken (dangling) and does not provide file data.
  - Modifying target via symlink affects original file (because symlink resolves to target at access time).
- ls and pwd:
  - pwd prints absolute path of current working directory.
  - ls shows directory entries; options change formatting and visibility.

---

## ls Options (quick reference)
- -l : long listing (permissions, owner, size, date, name). #ls  
- -a : show all files including hidden (dotfiles). #ls  
- -h : human-readable sizes (e.g., 1K, 2M). #ls  
- -t : sort by modification time (newest first). #ls  
- Combine: ls -lha -t

---

## Filesystem / Link Behavior Table

| Action | Hard Link | Symlink |
|---|---:|:---|
| Shares inode/data | Yes | No |
| Cross-filesystem | No | Yes |
| If target removed | Underlying data remains until all links removed | Symlink becomes dangling |
| Can link directories | Usually no | Yes (but can produce loops) |
| Creation command | ln src target | ln -s src target |

(#hardlink #symlink #filesystem)

---

## Quick Reference — One-page Rules
- Create hard link: ln source target → target is a new name for same inode. #ln  
- Create symlink: ln -s source target → target is a pointer file containing source path. #ln #symlink  
- Check current dir: pwd → prints absolute path. #pwd  
- List files: ls [dir]  
  - Use -l for details, -a for hidden, -h for human sizes, -t to sort by mod time. #ls  
- Deleting a link:
  - rm <hard-link-name> removes one directory entry; file data removed only when no links remain.
  - rm <symlink-name> removes the symlink only; target unaffected.
- To tell link types: ls -l → symlinks show “-> target”, hard links appear as regular files with same inode number (use ls -i to display inode). #inode

---

## Minimal Commands Checklist (copy into exam)
- ln src tgt        → create hard link
- ln -s src tgt     → create symbolic link
- rm linkname       → remove link (hard or symlink)
- pwd               → show absolute current directory
- ls -l -a -h -t dir → detailed listing (combine options)

---

Keep this sheet for quick lookup of #ln, #hardlink, #symlink, #pwd, and #ls behaviors and options.

---

## Module 2 — Lecture 10: Linux commands: touch, tr, pr — Cheatsheet

#hashtags: #linux #shell #command #touch #tr #pr #file #timestamp #textstream #formatting #man

## Key Definitions
- touch: create an empty file or update file access/modify timestamps without changing content. #touch
- tr: translate, delete, or squeeze characters from a text stream (stdin → stdout). #tr #textstream
- pr: paginate/format text files for printing or screen display (adds headers, page breaks). #pr #formatting
- man: view manual page for a command (e.g., man touch). #man

## Syntax / Quick Reference Forms
- touch: touch [OPTION]... FILE...
  - example: touch newfile.txt
  - set timestamp: touch -d "YYYY-MM-DD HH:MM:SS" file
- tr: tr [OPTION] SET1 [SET2]
  - example: tr 'A-Z' 'a-z' < infile > outfile
- pr: pr [OPTION]... [FILE]...
  - example: pr -l 60 file.txt       (set 60 lines/page)
  - merge files: pr -m file1 file2

## Important Options (concise)
- touch
  - -c : do not create file if it does not exist (no error). #touch
  - -d STRING : use STRING as the new access and modification time. #touch
  - -t [[CC]YY]MMDDhhmm[.ss] : use specified timestamp (alternate format). #touch
- tr
  - -d : delete characters in SET1 (no translation). #tr
  - -s : squeeze repeated characters in SET1 to a single occurrence. #tr
  - -c : complement SET1 (operate on characters not in SET1). #tr
- pr
  - -l N : set page length to N lines (lines per page). #pr
  - -m : merge multiple files side-by-side into one page. #pr
  - -h STRING : use STRING as the page header. #pr
  - -t : omit headers and trailers (print only file contents). #pr

## Key Algorithms / Concepts (bullet)
- #touch
  - Create placeholder files quickly.
  - Update file timestamps for build systems / dependency tracking.
- #tr
  - Simple byte/character-wise transformations; works with stdin/stdout—use with redirection or pipes.
  - Typical uses: case conversion, removing characters, normalizing whitespace.
- #pr
  - Paginate for printing or readable screen output; useful to view files in page-sized chunks and to prepare multi-file printouts.

## Important Properties / Invariants
- touch does not change file contents; only timestamps (unless file is created empty). #touch
- tr operates on byte/character streams — it does not accept filenames directly (use redirection or pipes). #tr
- tr is single-character-set oriented; to transform ranges use ranges like 'A-Z' 'a-z' or POSIX classes like '[:digit:]'. #tr
- pr formats output into pages (headers, footers, page breaks) — it is not an editor. #pr

## Quick Reference (scannable)
- Create file: touch file.txt    #touch
- Update timestamp to now: touch file.txt    #touch
- Do not create if missing: touch -c file.txt    #touch
- Set specific time: touch -d "2023-08-01 12:34:56" file.txt    #touch
- Lowercase stream: tr 'A-Z' 'a-z' < in > out    #tr
- Delete digits: tr -d '[:digit:]' < in > out    #tr
- Squeeze spaces: tr -s ' ' < in > out    #tr
- Complement and delete: tr -cd '[:alnum:]\n' < in > out    (keep only alnum + newline)    #tr
- Paginate with 50 lines/page: pr -l 50 file.txt    #pr
- Merge files side-by-side: pr -m file1.txt file2.txt    #pr
- No headers/trailers: pr -t file.txt    #pr
- View help: man touch | man tr | man pr    #man

## Examples (one-liners)
- touch placeholder: touch .placeholder    #touch
- touch specific date: touch -d "2024-02-21 09:00:00" report.txt    #touch
- convert file to lowercase: cat file | tr 'A-Z' 'a-z' > file.lc    #tr
- remove all non-printing: tr -cd '\11\12\15\40-\176' < in > out    #tr
- print two files merged per page: pr -m chapter1.txt chapter2.txt | lp    #pr

Remember: use man <command> for full option lists and platform-specific details. #man #linux

---

## Module 2 — Lecture 11: Linux Networking Commands — Cheatsheet

#hashtags: #networking #linux #hostname #ping #traceroute #nmap #ICMP #TCP #UDP #ports #diagnostics #TTL #RTT

---

---

## Key Definitions
- #hostname: command to display or set a system's network name (FQDN/short name).
- #ping: sends ICMP Echo Request to test reachability and measure round-trip time (RTT).
- #traceroute: traces network path (hops) from source to destination by manipulating TTL.
- #Nmap: network mapper — port/service scanner and discovery tool.
- #ICMP: Internet Control Message Protocol (used by ping).
- #TTL: Time To Live — hop-count limit for IP packets; used by traceroute.
- #RTT: Round-Trip Time — time for packet to go to host and return.

---

## Formulas / Notations
- RTT: measured per-packet by ping (typically shown in ms).
- TTL decrement → hop count (used by traceroute).
- ICMP Echo Request/Reply pair = connectivity check.
- localhost IP: 127.0.0.1
- Default ping packet payload on many Linux distros: 56 bytes data + 8 bytes ICMP header → 64 bytes total.

---

## Command Syntax Templates
- hostname: hostname [options] [new-hostname]
- ping: ping [options] destination
- traceroute: traceroute [options] destination
- nmap: nmap [scan-type options] [scan-options] target(s)

---

## Key Options / Quick Flag Reference

- hostname
  - -s : short hostname
  - -f : full/long hostname (FQDN)
  - -d : DNS domain name
  - -i : IP address of hostname
  - -I : all network addresses for host
  - (use man hostname for full list)  
  (#hostname)

- ping
  - -c <count> : send <count> packets then stop
  - -i <sec>   : interval between packets
  - -w <sec>   : deadline (max total seconds)
  - -s <size>  : data payload size (bytes)
  - Ctrl+C     : stop continuous ping (default on Linux runs until stopped)  
  (#ping #ICMP #RTT)

- traceroute
  - -n         : show numeric IPs (no DNS lookup)
  - -T         : use TCP packets (instead of default UDP/ICMP depending on platform)
  - -m <max>   : set maximum hops (max TTL)
  - (behavior) : increments TTL from 1 → max to elicit ICMP Time Exceeded replies to map hops  
  (#traceroute #TTL)

- Nmap
  - -sS : TCP SYN scan (fast, stealthy; half-open)
  - -sT : TCP connect scan (full TCP handshake)
  - -sU : UDP scan
  - -sV : service/version detection
  - -p <ports> : specify ports or ranges (e.g., -p 22,80,1000-2000)
  - -T<0..5> : timing template (0 slow → 5 aggressive)
  - <target> : hostname, IP, network (e.g., 192.168.1.0/24)  
  (LEGAL: only scan networks you own or have permission to scan)  
  (#nmap #ports #sS #sU #sV)

---

## Key Algorithms / Concepts (concise)
- Ping operation: send ICMP Echo Request → wait for Echo Reply → report RTT and packet loss (#ping #ICMP).
- Traceroute mechanism: send probes with increasing TTL; each router that decrements TTL to 0 returns ICMP Time Exceeded → reveals path & hop latency (#traceroute #TTL).
- Nmap scanning types:
  - SYN scan (-sS): send SYN, wait for SYN/ACK → determines open/closed without completing handshake.
  - Connect scan (-sT): full TCP connect() syscall; slower and more noisy.
  - UDP scan (-sU): send UDP packets; open/filtered detection is less reliable.
  - Version detection (-sV): probes services to identify software/version (#nmap).
- DNS resolution: hostnames map to IP via DNS; traceroute/ping may show hostname or numeric IP depending on flags (#DNS).

---

## Important Properties / Invariants
- Ping uses ICMP; some hosts/firewalls block ICMP → "host unreachable" or no replies.
- Traceroute depends on ICMP Time Exceeded responses; intermediate devices may drop/ignore probes or rate-limit responses.
- Nmap results can be affected by firewall rules, IDS/IPS, and host responsiveness — absence of responses ≠ guaranteed closed port.
- Changing hostname may require privileges and may not persist across reboots depending on distro/config.
- localhost = 127.0.0.1 (IPv4 loopback) — always local machine.
- Default ping on Linux sends packets continuously until stopped; use -c for fixed count.

---

## Quick Reference (one-liners & examples)
- Show hostname: hostname
- Show FQDN: hostname -f
- Show short name: hostname -s
- Show IP(s): hostname -i  (single)  | hostname -I (all)
- Ping once (4 packets): ping -c 4 example.com
- Ping every 5s: ping -i 5 8.8.8.8
- Ping with packet size 100 bytes: ping -s 100 host
- Trace route (numeric IPs): traceroute -n example.com
- Traceroute with TCP probes max 30 hops: traceroute -T -m 30 example.com
- Nmap quick SYN scan top ports: nmap -sS -T4 target
- Nmap UDP & version detection: nmap -sU -sV -p U:53,161 target
- Common ports: 21 FTP, 22 SSH, 23 Telnet, 25 SMTP, 53 DNS, 80 HTTP, 443 HTTPS, 3306 MySQL
- Legal reminder: Only scan authorized networks (Nmap usage can be illegal without permission).

---

## Where to get more info
- man hostname
- man ping
- man traceroute
- man nmap / nmap --help
- Nmap reference: https://nmap.org/book/quickstart.html

---

Keep this sheet for quick flags, command templates, and reminders about behavior (ICMP vs TCP/UDP, TTL behavior, permissions/legal).

---

## Module 2 — Lecture 12: SSH & SCP Cheatsheet — Secure Remote Access and File Transfer

#keywords: #SSH #SCP #SecureShell #encryption #publickey #privatekey #hostkey #known_hosts #DiffieHellman #/etc/ssh #ssh_config #sshd_config #port #identityfile #recursive

## Key Definitions
- SSH: Secure Shell protocol for encrypted remote login, command execution, and tunneling. #SSH
- SCP: Secure copy utility using SSH to transfer files/directories. #SCP
- Private key: Secret key file used for public-key authentication. #privatekey #publickey
- Public key: Key distributed to servers for verifying a client. #publickey
- Host key: Server’s key pair used by clients to verify server identity. #hostkey
- known_hosts: Client-side file storing host public keys to prevent MITM. #known_hosts
- /etc/ssh: System directory with SSH client/server configuration and keys. #/etc/ssh
- Moduli: File(s) containing primes for Diffie–Hellman key exchange. #DiffieHellman

## Formulas / Syntax Templates
- SSH connect: ssh [options] [user@]hostname [command]
- SCP copy: scp [options] source destination
- Remote path format: [user@]host:/absolute/or/relative/path
- Default SSH port: 22

## Common Options (quick)
- -p (ssh): specify port (e.g., -p 2000)  #port
- -i (ssh|scp): specify private key file (identity file)  #identityfile
- -r (scp): recursive copy for directories  #recursive
- -P (scp): specify port for scp (note: scp uses capital -P) — see note below

Note: SSH uses -p (lowercase) for port; scp historically uses -P (uppercase). Also scp’s -p (lowercase) preserves file times/modes.

## Key Algorithms / Concepts
- Authentication modes: password-based, public-key (key pair + optional passphrase). #publickey
- Host verification: client checks host key vs ~/.ssh/known_hosts to detect changes. #known_hosts
- Diffie–Hellman: key exchange method using primes from /etc/ssh/moduli to derive session keys. #DiffieHellman
- SSH daemon vs client: sshd (server) reads /etc/ssh/sshd_config; client reads /etc/ssh/ssh_config. #sshd_config #ssh_config

## /etc/ssh — Important Files (one-liners)
- ssh_config — global SSH client defaults. #ssh_config
- sshd_config — SSH server configuration (port, auth methods, allow/deny). #sshd_config
- moduli — primes for Diffie–Hellman key exchange. #moduli
- ssh_host_* (e.g., ssh_host_rsa_key, ssh_host_rsa_key.pub) — server private/public host keys. #hostkey
- known_hosts (client-side usually ~/.ssh/known_hosts) — stored remote host public keys. #known_hosts
- sshrc — optional script executed at login (server/client specific). #sshrc
- ssh_config.d / sshd_config.d — directories for included config fragments. #ssh_config.d #sshd_config.d

## Important Properties / Invariants
- Private key must be kept secret; set permissions (chmod 600) to avoid rejection. #privatekey
- Host key changes indicate possible MITM; verify out-of-band. #hostkey
- Key-based auth preferred over passwords; protect keys with passphrases. #publickey
- SSH defaults to port 22; changing port is obscurity, not security. #port
- scp follows source→destination order: swapping changes transfer direction. #SCP

## Quick Reference — Commands & Examples
- Connect (password auth): ssh user@example.com
- Connect (key + custom port): ssh -p 2000 -i ./key/key.txt user@BITSPilani
- Run remote command: ssh user@host 'ls -la /var/www'
- Copy local → remote: scp ./file.txt user@host:/remote/path
- Copy remote → local: scp user@host:/remote/file.txt ./localdir
- Copy directory recursively: scp -r ./dir user@host:/remote/dir
- SCP with port (correct): scp -P 2000 -r ./dir user@host:/remote/dir
  - Note: transcript used -p for scp port; correct OpenSSH scp flag is -P (uppercase). Lowercase -p preserves times/modes.
- Use identity file with scp: scp -i ./key/key.txt user@host:/file ./local
- View manuals: man ssh_config ; man sshd_config

## Security Best-Practices (short)
- Use key-based auth + passphrase-protected private keys. #publickey
- Keep SSH software/config up-to-date. #SSH
- Restrict RootLogin in sshd_config (e.g., PermitRootLogin no). #sshd_config
- Use strong ciphers; review /etc/ssh/ssh_config and /etc/ssh/sshd_config. #encryption
- Backup server host keys on reinstall to avoid host key mismatches. #hostkey

## Troubleshooting Tips (one-liners)
- Permission denied → check key permissions and correct user. #privatekey
- Host key mismatch → verify server identity; remove outdated entry in ~/.ssh/known_hosts to reconnect (but verify first). #known_hosts
- scp fails on port → try -P (uppercase) or verify server sshd port. #port

Keep this sheet handy for quick command syntax, config file names, and security checks during an open-book exam.

---

## Module 2 — Lecture 13: Linux Fundamentals Cheatsheet

#hashtags: #linux #kernel #shell #filesystem #processes #systemlibraries #bootloader #init #systemd #systemctl #ps #ls #commands #grub #runlevels #targets #permissions

---

## Key Definitions (one-line)
- Kernel: Core OS component managing hardware, drivers, memory, and processes. #kernel  
- Shell: User interface (command interpreter) for running commands and scripts. #shell  
- Filesystem: Hierarchical namespace of files/directories rooted at `/`. #filesystem  
- Process: An executing program instance (has PID, state, parent). #processes  
- System libraries: Shared libraries (.so) used by programs at runtime. #systemlibraries  
- Bootloader: Program that loads the kernel (e.g., GRUB) during boot. #bootloader #grub  
- Init (PID 1): First user-space process that starts and manages services (systemd or SysV). #init #systemd  
- Unit/Service (systemd): Config file describing how to start/manage a service. #systemctl

---

## Boot & Login Sequence (scannable steps)
1. Firmware (BIOS/UEFI) POST → reads boot device.  
2. Bootloader (GRUB) loads kernel + initramfs. #grub #bootloader  
3. Kernel initialization (drivers, mounts initramfs). #kernel  
4. Root filesystem mounted → kernel execs init (PID 1). #init  
5. Init/systemd reads units → starts services/targets. #systemd #targets  
6. getty/login prompt → user login → user shell session. #login #shell

Important files: `/boot/vmlinuz`, `/boot/initrd.img`, `/etc/fstab`, `/etc/default/grub`.

---

## Formulas / Notation / Quick mappings
- Permission bits: r=4, w=2, x=1 → numeric mode (e.g., 755 = rwx r-x r-x). #permissions  
- Exit code: 0 = success, nonzero = error.  
- Common PID facts: PID 1 = init/systemd; orphaned processes adopted by PID 1. #processes  
- Process listing formats: `ps aux` (BSD) vs `ps -ef` (UNIX). #ps

---

## Key Commands & Flags (quick reference)
- File listing: `ls -l` (long), `ls -a` (hidden), `ls -la`. #ls  
- Process view: `ps aux`, `ps -ef`, `top`, `htop`. #ps  
- Start/stop services (systemd): `systemctl status|start|stop|restart|enable|disable <unit>`. #systemctl #systemd  
- Logs: `journalctl -u <unit>`, `journalctl -b`, `dmesg`. #journalctl #dmesg  
- File ops: `cp`, `mv`, `rm`, `mkdir`, `rmdir`. #commands  
- Disk/FS: `df -h`, `du -sh <path>`, `mount`, `umount`. #filesystem  
- Permissions: `chmod 755 file`, `chown user:group file`, `umask`. #permissions  
- Process control: `kill <PID>`, `kill -9 <PID>`, `pkill -f <pattern>`. #processes  
- Identity: `whoami`, `id`, `su -`, `sudo <cmd>`.  
- Search/text: `grep`, `find`, `cat`, `less`, `tail -f`. #commands

---

## Key Concepts / Components (bulleted)
- Kernel vs User-space: Kernel handles hardware; shells/apps run in user-space. #kernel #shell  
- Single filesystem tree: Everything mounted under `/`. #filesystem  
- Systemd units: service, socket, target, mount, timer, path, etc. #systemd #targets  
- Initramfs purpose: early userspace to mount real root filesystem. #init  
- Service management: `systemctl` controls units, `journalctl` reads logs. #systemctl #journalctl  
- Process lifecycle: create (fork/exec), running, sleeping, stopped, zombie, exit. #processes

---

## Important Properties & Invariants
- PID 1 is special: reaps zombies, adopts orphans. #init  
- Root user UID = 0 has full privileges.  
- Filesystem mount order affects availability (use `/etc/fstab` or systemd mount units). #filesystem  
- Systemd enforces dependencies via unit ordering and targets. #systemd  
- Binary/library locations: `/bin /sbin /usr/bin /usr/sbin /lib /usr/lib`. #systemlibraries

---

## Quick Reference Table (commands → common flags)
| Task | Command (examples) |
|---|---|
| List files | ls -l, ls -la |
| View processes | ps aux, top, htop |
| Manage services | systemctl status/start/stop/restart/enable/disable <unit> |
| Read logs | journalctl -u <unit>, journalctl -b, dmesg |
| Disk usage | df -h, du -sh /path |
| File permissions | chmod 755 file; chown user:group file |
| Kill process | kill PID; kill -9 PID; pkill -f pattern |
| Boot config | update-grub (Debian), edit /etc/default/grub |

---

## Exam Quick Tips (one-liners)
- To check kernel & arch: `uname -a`. #kernel  
- To see PID 1 and tree: `ps -fp 1` and `pstree -p`. #processes  
- To debug boot: check `journalctl -b -1` (previous boot) & `dmesg`. #journalctl #dmesg  
- To persist mounts: add to `/etc/fstab`. #filesystem  
- Use `systemctl is-enabled <unit>` to check boot enablement. #systemctl

---

End — concise reference for Linux components, boot flow, core commands, and quick facts.

---

## Module 3 — Lecture 14: Linux Files & Directories — Cheatsheet

#hashtags: #Linux #filesystem #inode #partition #disk #root #paths #directories #permissions #commands #dev #home #bin #usr #var #lib #tmp #sbin #absolute-path #relative-path

---

---

## Key Definitions (one-liners)
- File: Persistent collection of data (text, binary, image, program). #File  
- Directory (folder): Special file that contains entries (files/dirs). #Directory  
- File path: Textual location of a file/dir in the hierarchy. #Path  
- Absolute path: Path starting at root "/" (full path). #AbsolutePath  
- Relative path: Path starting from current working directory. #RelativePath  
- Root directory: Top-level directory, represented by "/". #Root  
- Partition: Group of contiguous cylinders treated as an independent disk region. #Partition  
- Block device: Storage device exposing fixed-size blocks (disks). #BlockDevice  
- Sector: Smallest addressable unit on a disk (often 512B/4KB). #Sector  
- Track: Circular track on a disk platter. #Track  
- Cylinder: Set of tracks at same radius across all platters. #Cylinder  
- Partition table: Index mapping disk sections to partitions. #PartitionTable  
- Inode: File metadata record (permissions, owner, times, size, block addresses, inode number). #Inode

---

## Formulas / Notation / Mappings
- Disk composition: sector(s) → track → cylinder → partition (contiguous cylinders). #Disk  
- Block = 1 or more contiguous sectors. #Block  
- Partition = contiguous cylinders. #Partition  
- Path notation:
  - Absolute: /a/b/c (starts with /)  
  - Relative: ../x/y or ./file (no leading /)  
- Permission bits (per class: user/group/other):
  - read = 4, write = 2, execute = 1  
  - numeric mode = sum per class (e.g., rwxr-xr-x = 7 5 5 → 755). #Permissions
- Inode attributes (common): permissions, hard link count, UID, GID, size, atime, mtime, ctime, inode number, device/partition id. #Inode

---

## Key Algorithms / Concepts (bulleted)
- Hierarchical namespace: single tree rooted at "/" where all file systems are mounted. #Hierarchy  
- Mounting: attach a filesystem (partition/device) at a directory (mount point). #Mount  
- Device-as-file: hardware devices represented as special files in /dev. #DeviceFile #dev  
- Partitioning: split physical disk into logical partitions to host file systems. #Partitioning  
- Inode-based storage: directory entries map names → inode numbers; inode stores file metadata + block pointers. #InodeStructure  
- Absolute vs Relative resolution: resolve from / vs from current working directory (CWD). #PathResolution

---

## Important Properties / Invariants
- Single root ("/") — everything is reachable under this tree. #Root  
- Directories are files containing name → inode mappings. #Directory  
- Inodes are unique within a filesystem; the inode number + device identifies a file location. #Inode  
- Hard links: multiple directory entries can point to same inode; link count stored in inode. #HardLink  
- Device files in /dev control hardware access via permissions. #dev  
- /tmp is ephemeral (often cleared on reboot). Do not store permanent data there. #tmp  
- /bin and /usr/bin: user commands; /sbin and /usr/sbin: system/admin commands. #bin #sbin #usr  
- /etc stores system configuration; /var stores variable runtime data (logs, spool, db). #etc #var  
- Partitioning helps separate concerns (OS / user data / swap / logs). #Partitioning

---

## Common Directories (quick map)
- / — root #Root  
- /bin — essential user binaries (programs) #bin  
- /sbin — system binaries (admin) #sbin  
- /usr — user programs/libraries/data (larger read-only hierarchy) #usr  
- /lib, /lib64 — shared libraries for binaries #lib  
- /etc — system-wide configuration files #etc  
- /home — user home directories (/home/username) #home  
- /dev — device files (disks, terminals, etc.) #dev  
- /tmp — temporary files (cleared on reboot) #tmp  
- /var — variable files (logs, mail, spool, db) #var

---

## Quick Reference — Commands (compact)
| Command | Purpose | Example |
|---|---:|---|
| pwd | print working directory | pwd → /home/alice |
| ls | list directory | ls -l (long), ls -a (all) |
| cd | change directory | cd /etc ; cd .. ; cd ~ |
| mkdir | create directory | mkdir notes |
| rmdir | remove empty directory | rmdir olddir |
| rm | remove file/dir | rm file ; rm -r dir |
| cp | copy file/dir | cp src dst ; cp -r dir1 dir2 |
| mv | move/rename | mv old new ; mv file /path/ |
| ln | hard link | ln target linkname |
| ln -s | symbolic (soft) link | ln -s /path/target linkname |
| chmod | change permissions (symbolic or numeric) | chmod 755 script.sh ; chmod u+x file |
| chown | change owner/group | chown user:group file |
| stat | show inode & timestamps | stat file |
| df | filesystem disk usage (per FS) | df -h |
| du | disk usage (per file/dir) | du -sh dir |
| mount / umount | attach/detach filesystem | mount /dev/sda1 /mnt ; umount /mnt |

(Use root/sudo for privileged operations like mount, chown to root-owned files, writing to /sbin, etc.)

---

## Quick Patterns / Cheats
- Paths:
  - /absolute/path — stable regardless of CWD  
  - relative: ./file (current), ../ (parent)  
- Permissions mapping:
  - rwxrwxrwx → octal 777; rwxr-xr-x → 755; rw-r--r-- → 644  
- Check file metadata:
  - ls -l → permissions, link count, owner, group, size, mtime, name  
  - stat → detailed inode info (inode #, blocks, atime/mtime/ctime)  
- Find mount & partition info:
  - lsblk, fdisk -l, blkid, cat /proc/partitions, df -h  
- Temporary files: avoid storing persistent data in /tmp (cleared on reboot). #tmp
- When copying ownership and perms: use cp -a (archive) to preserve metadata.  
- Use symbolic links for shared access across directories; hard links only within same FS. #links

---

Keep this sheet near your reference materials for quick lookup of filesystem structure, path rules, inode attributes, common directories, permission octal mapping, and essential commands.

---

## Module 3 — Lecture 15: File Permissions (Linux) — Cheatsheet

#hashtags: #filepermissions #linux #chmod #umask #ls #octal #symbolic #permissions #read #write #execute #filetypes #symlink #blockdevice #chardevice #pipe #socket #security

## Key Definitions (one-line)
- File permission: access rights (read/write/execute) controlling who can do what to a file/dir.  
- Owner (u): user who owns the file.  
- Group (g): group the owner belongs to.  
- Others (o): all other users.  
- Symbolic mode: chmod syntax using letters (u/g/o/a, +/−/=) and r/w/x.  
- Numeric (octal) mode: chmod using 3 octal digits (owner/group/others), each 0–7.  
- umask: mask subtracted from maximum permissions to get default new-file/dir perms.  
- Permission string: 10 chars: [type][owner(3)][group(3)][others(3)] (e.g., -rwxr-xr--).  
- File types chars: - regular, d directory, l symlink, b block device, c character device, p named pipe, s socket.

## Formulas / Notation
- Bit values: read = 4, write = 2, execute = 1.  
- Octal digit = sum(bits): 7=4+2+1 (rwx), 6=4+2 (rw-), 5=4+1 (r-x), 4=r--, 3=-wx, 2=-w-, 1=--x, 0=---.  
- Permission string length: 10 chars (1 type + 3x3 permission triads).  
- Default permissions = (max) − umask  
  - max for directories = 777; max for files = 666 (no execute by default).  
  - Example: umask 022 → dir default = 777−022 = 755; file default = 666−022 = 644.

## Key Commands / Syntax
- View permissions:  
  - ls -l  (long listing, shows permissions & ownership)  
  - ls -a  (include hidden files)  
  - ls -lah (long, human-readable sizes, show hidden)  
- Change permissions: chmod [MODE] FILE(S)  
  - Numeric: chmod 755 script.sh  → owner=rwx (7), group=r-x (5), others=r-x (5)  
  - Symbolic: chmod u+rwx,g-w,o=r file.txt  
    - u/g/o/a (user/group/others/all), + to add, - to remove, = to set exactly  
- umask: umask [MASK]  (set default mask; show with umask without args)

## Key Algorithms / Concepts (bulleted)
- #octal-encoding: encode each triad (u/g/o) to a digit 0–7 using 4/2/1 bits.  
- #symbolic-mode: modify specific classes without touching others (u/g/o/a with +/−/=).  
- #permission-string-interpretation: parse e.g. -rwxr-xr-- → owner=rwx (7), group=r-x (5), others=r-- (4) → 754.  
- #default-permissions: new files/dirs get (max − umask).  
- #execute-meaning: for files, allow running; for dirs, execute = traverse/search (required to enter/access contents).

## Important Properties / Invariants
- The three classes (u,g,o) are independent — changing one does not auto-change others unless using 'a' or explicit commands.  
- Numeric chmod sets all three classes at once (3-digit).  
- Symbolic chmod can be applied incrementally and combined (e.g., u+x,g-w).  
- umask only affects newly created files/directories, not existing ones.  
- For files, default max excludes execute (666); for directories include execute (777).  
- Incorrect permissions can cause security or availability issues — be cautious with 777 on dirs/files.

## Quick Reference (scan)
- Octal → perms:
  - 0 = ---  
  - 1 = --x  
  - 2 = -w-  
  - 3 = -wx  
  - 4 = r--  
  - 5 = r-x  
  - 6 = rw-  
  - 7 = rwx
- Common chmod shortcuts:
  - chmod 644 file.txt → rw- r-- r-- (owner rw, group read, others read)  
  - chmod 600 file.txt → rw- --- --- (private file)  
  - chmod 755 script.sh → rwx r-x r-x (owner can execute; others can read & execute)  
  - chmod 700 dir/ → rwx --- --- (private dir)
- Interpret permissions string:
  - Example: -rw-r--r-- → regular file, owner=rw(6), group=r(4), others=r(4) → chmod 644
  - Example: drwxr-xr-x → directory, owner=7, group=5, others=5 → chmod 755
- umask examples:
  - umask 022 → new file = 666−022 = 644; new dir = 777−022 = 755  
  - umask 077 → new file = 600; new dir = 700 (private)
- File type chars:
  - - regular file, d directory, l symlink, b block dev, c char dev, p named pipe (FIFO), s socket

## Example quick commands
- Show detailed, human sizes: ls -lah  
- Set file private: chmod 600 secret.txt  
- Make script executable: chmod +x run.sh  OR chmod 755 run.sh  
- Add execute for owner only: chmod u+x file  
- Remove read for group: chmod g-r file

Keep this sheet for quick lookup of bit mappings, command forms, and common presets.

---

## Module 3 — Lecture 16: Inodes & Linux File System Layout — Cheatsheet

Keywords: #inode #filesystem #Linux #Unix #superblock #bootblock #inodetable #datablocks #directory #hardlink #permissions #UID #GID #timestamps #blockpointers #partition #MBR

---

## Key Definitions
- inode: index node — metadata record for a file (excludes file name and file data).
- inode number: unique identifier for a file within a filesystem.
- inode table/list: collection of all inode records in a filesystem.
- data block: disk block that contains actual file contents.
- block pointer: pointer(s) in an inode that reference data blocks.
- superblock: metadata describing the filesystem state (size, free blocks, inode info).
- boot block (MBR in disk): first sector that holds bootstrap code and partition info.
- directory file: maps filenames → inode numbers (holds name→inode entries).
- hard link: directory entry that points to an inode; multiple hard links share one inode.
- UID / GID: file owner (user id) and group id stored in inode.
- timestamps: access (atime), modification (mtime), change (ctime) stored in inode.

---

## Formulas / Notation
- File identity: (filesystem_ID, inode_number)
- Typical timestamp set: {atime, mtime, ctime}
- Directory minimum links: links ≥ 2 ('.' points to self, '..' points to parent)
- Allocation rule: Each allocated data block → belongs to exactly one file

---

## Key Algorithms / Concepts
- #inode lookup sequence:
  - filename → directory entry → inode number → inode record → block pointers → data blocks
- #ls commands to view inode:
  - ls -i or ls -li → show inode numbers in directory listing
- #file-metadata stored in inode:
  - type, permissions, owner (UID), group (GID), size, timestamps, link count, block pointers
- #filesystem-layout (high-level order in a partition):
  - Boot block (MBR) → Superblock → Inode list/table → Data blocks
- #block-allocation invariant:
  - Partial-block slack is not shared — a block is owned by a single file

---

## Important Properties / Invariants
- Inode does NOT store filename(s) — name→inode mapping lives in directories. (#directory)
- One inode per filesystem object (file or directory). (#inode)
- Multiple filenames (hard links) can map to the same inode; inode holds link count. (#hardlink)
- Directories always have at least two links: '.' and '..'. (#directory)
- Data blocks referenced by an inode contain actual content; inode stores block pointers. (#datablocks #blockpointers)
- Superblock tracks filesystem capacity, free block list, next free index, inode count/free inodes. (#superblock)
- Each allocated data block is exclusive to one file even if not fully filled. (#datablocks)

---

## Quick Reference (Scannable)
- Show inode numbers: ls -i | ls -li
- File identity: use (filesystem_ID, inode_number)
- Inode contains: {type, perms, UID, GID, size, atime, mtime, ctime, link_count, block_pointers}
- Directory ↔ inode mapping: directory entries = (name → inode_number)
- Partition filesystem layout:
  - Boot block (bootstrap/MBR)
  - Superblock (fs metadata & free lists)
  - Inode list/table (inode records)
  - Data blocks (file contents)
- Directory links: '.' = self, '..' = parent (hence links ≥ 2)
- Deallocation rule (exam-relevant): free blocks/inodes tracked by superblock; blocks not shared among files

---

Tags (major concepts): #inode #filesystem #superblock #bootblock #inodetable #datablocks #directory #hardlink #permissions #UID #GID #timestamps #blockpointers #MBR

--- 
(Use this sheet to quickly locate: what an inode holds, how names map to inodes, and the on-disk layout order.)

---

## Module 3 — Lecture 17: Linux Inode & Links — Cheatsheet

#hashtags: #inode #filesystem #stat #du #df #blocks #direct #indirect #single-indirect #double-indirect #triple-indirect #permissions #ownership #timestamps #hardlink #symlink #symboliclink #filetype #extendedattributes

---

## Key Definitions (one-line)
- inode: On-disk structure holding a file's metadata (not filename or directory entry). #inode  
- stat: Command that displays an inode's metadata for a file. #stat  
- block: Allocation unit on disk; default unit referenced here = 512 bytes. #blocks  
- direct block pointer: Inode pointer that directly references a data block. #direct  
- indirect block pointer: Pointer to a block that contains more pointers to data blocks. #indirect  
- single/double/triple indirect: 1/2/3 levels of pointer indirection to reach data blocks. #single-indirect #double-indirect #triple-indirect  
- hard link: Directory entry that references the same inode (same data) as another name. #hardlink  
- symbolic (soft) link: Separate file whose contents are a path that references another file or dir. #symlink #symboliclink  
- permissions (file mode): Read/write/execute bits for owner, group, others. #permissions  
- ownership: UID and GID stored in inode. #ownership  
- timestamps: atime (access), mtime (modify data), ctime (change metadata), birth (creation). #timestamps  
- extended attributes: Extra metadata attached to file (security/user data). #extendedattributes  
- generation number: FS-specific number tracking inode changes. #generationnumber  
- fragment block: Old FS scheme: block holding fragment pointers (fragmentation). #fragmentblock

---

## Formulas / Equations
- blocks_used = ceil(file_size / block_size)  
  - Example (transcript): block_size = 512 bytes → 4096 bytes uses 8 blocks. #blocks  
- du -k: block unit = 1024 bytes (kilobyte units). #du #blocks  
- df -H: human-readable with powers of 1000; df -h: human-readable with powers of 1024. #df

---

## Key Algorithms / Concepts (bulleted)
- Inode structure (fields) — #inode
  - file mode & type (regular/dir/symlink/special) #filetype #permissions
  - ownership: UID, GID #ownership
  - file size (bytes) #blocks
  - timestamps: atime, mtime, ctime, birth #timestamps
  - link count (# of hard links) #hardlink
  - block pointers: direct + single/double/triple indirect #direct #indirect
  - file flags, extended attributes, generation number, FS id, fragment pointers #extendedattributes #generationnumber
- Pointer levels — #direct #single-indirect #double-indirect #triple-indirect
  - Direct: inode -> data block
  - Single indirect: inode -> block of pointers -> data blocks
  - Double indirect: inode -> block -> block of pointers -> data blocks
  - Triple indirect: three levels of pointer blocks -> data blocks
- Hard links — #hardlink
  - ln source-file link-name
  - multiple directory entries reference same inode/data; deleting one name does not remove data until link count = 0
  - cannot link to directories (typical) and must remain on same filesystem
- Symbolic links — #symlink
  - ln -s source-file link-name
  - separate inode containing path; can point across filesystems; broken/dangling if target removed
- stat command — #stat
  - stat filename → shows size, allocated blocks, type, device (hex), inode number, link count, timestamps, birth time, etc.
- du command (disk usage) — #du
  - du reports per-file/directory allocated blocks (based on file size)
  - du -a : list every file's disk usage (individual files) #du  
  - du -k : show block counts in 1024-byte units (kilobytes) #du  
  - du -i : (lecture) allocates blocks evenly among links #du  
  - du -l : (lecture) represents blocks evenly among links #du  
  - du -s : show total for specified files/directories (summary) #du
- df command (filesystem free space) — #df
  - df shows free/used space on mounted filesystems (per-FS overview)
  - df -h : sizes human-readable (binary 1024) #df  
  - df -H : human-readable powers of 1000 (decimal) #df  
  - df -M : show blocks in megabytes #df  
  - df -i : show inode usage (IUsed, IFree) #df  
  - df -T : show filesystem types #df
  - df /boot : display info for mounted /boot filesystem example

---

## Important Properties / Invariants
- Inodes hold metadata, not filenames; directory entries map names → inode numbers. #inode  
- Hard links share inode and data: changes to content via any hard link affect the same data; inode link count tracks how many names exist. #hardlink  
- Symbolic links are independent files with their own inode; they store a pathname and do not share data blocks with target. #symlink  
- Direct pointers are fastest; indirect pointers allow large files at expense of extra indirection. #direct #indirect  
- Deleting a file removes a directory entry; data freed only when inode link count = 0 and no processes have it open. #inode  
- du reports disk allocation (blocks), not necessarily exact file size (sparse files, fragmentation). #du  
- df reports filesystem-level free/used capacity; df -i reports inode exhaustion (can run out of inodes even if space remains). #df

---

## Quick Reference (scannable)
Commands / Syntax:
- stat filename                     → show inode metadata (#stat)  
- ln source-file link-name          → create hard link (#hardlink)  
- ln -s source-file link-name       → create symbolic link (#symlink)  
- du [options] file/dir             → disk usage (#du)  
  - -a : list all files  
  - -k : use 1024-byte units  
  - -i : (lecture) allocate blocks evenly among links  
  - -l : (lecture) represent blocks evenly among links  
  - -s : summary (total)  
- df [options] [mountpoint]         → filesystem usage (#df)  
  - -h : human-readable (1024)  
  - -H : human-readable (1000)  
  - -M : megabyte units  
  - -i : show inodes  
  - -T : show filesystem type

Units & Examples:
- Default block unit (transcript): 512 bytes → blocks = ceil(size / 512) #blocks  
- Example: 4096 bytes = 8 blocks at 512 B block size.  
- du -k uses 1024-byte blocks (kilobytes). #du

Inode Fields (short list):
- file type & mode, uid/gid, size, link count, device id, inode number, block pointers, atime/mtime/ctime/birth, file flags, xattrs, generation, fs id, fragment pointers. #inode

Hard vs Soft (at-a-glance):
- Hard link: same inode, same data, cannot cross filesystems, cannot usually point to directories. #hardlink  
- Symlink: separate inode, stores target path, can cross FS, can be dangling after target deletion. #symlink

Notes:
- Color coding of files/links depends on terminal/LS_COLORS and distro (lecture noted colors may vary).  
- Stat and du refer to allocated blocks (not logical size for sparse files). #stat #du

---

End of cheatsheet — concise listing for quick lookup during exam.

---

## Module 3 — Lecture 18: Inodes & Directory Permissions (Linux) — Cheatsheet

#hashtags: #inode #directory #directory-entry #filesystem #permissions #access-control #chmod #link #hardlink #dot #dotdot #ls #chmod

---

## Key Definitions
- inode: Filesystem metadata object (permissions, owner, timestamps, pointers to data).
- directory inode: An inode whose data blocks contain directory entries (names + inode numbers).
- directory entry: Fixed-size record mapping a file name to an inode number.
- link (hard link): A directory entry (name) that references an inode; multiple links can reference same inode.
- link count: Number of directory entries (names) pointing to an inode; when 0 the inode is removed.
- dot (.): Directory entry pointing to the directory itself.
- dot-dot (..): Directory entry pointing to the parent directory.

---

## Formulas / Fixed Sizes / Notation
- Directory entry size = 16 bytes
- Directory entry layout (classic): first 2 bytes = inode number; remaining bytes = filename (component)
- Max component (filename) length = 14 characters
- Inode number field = 2 bytes ⇒ max inode id = 2^16 - 1 = 65535
- Permission bits numeric breakdown: rwx = 4 + 2 + 1
  - 7 = rwx, 6 = rw, 5 = rx, 4 = r, 0 = ---
- Example: chmod 755 dir ⇒ owner=7 (rwx), group=5 (r-x), others=5 (r-x)

---

## Key Concepts / Items
- #inode
  - Stores: permissions, ownership (UID/GID), timestamps, link count, pointers to data blocks.
- #directory
  - Represented by an inode whose data blocks store directory entries (name ↔ inode number).
- #directory-entry
  - 16 bytes each; maps filename (≤14 chars) to 2-byte inode number.
- #dot / #dotdot
  - Every directory contains "." (self) and ".." (parent) entries with inode numbers.
- #link / #hardlink
  - File names are links; multiple directory entries can reference the same inode.
  - Deleting a name decrements link count; inode removed only when count = 0.
- #permissions (for directories)
  - Read (r): list names (ls) — view entries only.
  - Write (w): create, delete, rename entries within the directory (subject to file perms).
  - Execute (x): traverse/access directory contents (cd, open files inside).
- #chmod
  - Command to change permissions; e.g., chmod 755 directory

---

## Important Properties / Invariants
- The only connection stored in a directory entry between name and contents is the inode number (first 2 bytes).
- Same inode can appear in multiple directories (hard links).
- Removing a directory entry does not remove the inode unless link count hits zero.
- Read without execute: can list names but cannot access/traverse contents.
- Execute without read: can traverse and access files if you know names, but cannot list directory contents.
- Write on directory allows create/delete/rename; to remove a file also requires write on directory and appropriate permissions on the file (depending on system policy).
- Proper permission setting is essential for confidentiality and integrity.

---

## Quick Reference (scannable)
- Directory entry (16 bytes)
  - Bytes 0–1: inode number (2 bytes)
  - Bytes 2–15: filename (≤14 chars)
- Common commands
  - View contents: ls
  - Change permissions: chmod 755 dir
- Permission effects (directory)
  - r = list (ls)
  - w = create/delete/rename entries
  - x = traverse (cd) and access contents
- Numeric permission mapping
  - 7 = rwx, 6 = rw-, 5 = r-x, 4 = r--, 0 = ---
- Typical safe default: avoid granting write to group/others; give execute only as needed.
- Link semantics
  - link count > 1: multiple names point to same inode
  - link count = 0: inode and data blocks reclaimed

---

Keep this sheet for quick lookup: inode structure facts, directory-entry layout, permission bit meanings, and the minimal commands/behaviors you’ll need during the exam.

---

## Module 3 — Lecture 19: Navigating & Listing Files (UNIX/Linux) — Cheatsheet

#keywords: #filesystem #paths #pwd #mkdir #cd #ls #relative-path #absolute-path #dot #dotdot #tilde #hidden-files

## Key Definitions
- pwd: print working directory — shows current directory (absolute path). #pwd  
- mkdir: make directory — create new directory. #mkdir  
- cd: change directory — move to another directory. #cd  
- ls: list directory contents. #ls  
- Absolute path: full path from root (starts with `/`). #absolute-path  
- Relative path: path relative to current directory (no leading `/`). #relative-path  
- . (dot): entry referring to the current directory. #dot  
- .. (dotdot): entry referring to the parent directory. #dotdot  
- ~ (tilde): shorthand for the current user's home directory. #tilde #home  
- Hidden files: filenames starting with `.`; shown with `ls -a`. #hidden-files

## Formulas / Notation (quick)
- Absolute path example: /home/sai/my_directory  
- Relative path example: my_directory/subdir/file.txt  
- Home shortcut: ~ ≡ /home/username  
- Navigation depth: cd dir1/dir2/dir3  (can jump multiple levels in one command)

## Key Commands / Concepts
- pwd — show current directory (absolute). #pwd
- mkdir <name> — create directory named <name>. #mkdir
- cd <dir> — change to directory <dir> (relative or absolute). #cd
- cd .. — go to parent directory (via `..`). #dotdot
- cd . — stay in the same directory (via `.`). #dot
- cd ~  or cd  — go to home directory. #tilde #home
- ls — list files in current directory. #ls
- ls <path> — list files in given path without cd. #ls
- ls -l -a -h (common combined option: -lah)  
  - -l: long format (permissions, owner, size, date)  
  - -a: include hidden files (names starting with `.`)  
  - -h: human-readable sizes (e.g., K, M). #hidden-files
- Path types:  
  - Absolute: starts with `/` — independent of cwd. #absolute-path  
  - Relative: starts from current working directory — does not start with `/`. #relative-path

## Important Properties / Invariants
- Every directory has `.` (self) and `..` (parent) entries automatically. #dot #dotdot  
- `pwd` always returns an absolute path. #pwd  
- `cd` with an absolute path ignores current directory; with relative path it is resolved from cwd. #cd  
- `ls <dir>` lists contents without changing cwd. #ls  
- `cd` can accept multiple-level paths in one command (no need to cd step-by-step). #cd

## Quick Reference (scannable)
- Show current dir:
  - pwd
- Create directory:
  - mkdir mydir
- Enter directory:
  - cd mydir         (relative)
  - cd /a/b/c        (absolute)
  - cd ~             (home)
  - cd               (also goes to home)
- Move up:
  - cd ..            (parent)
  - cd ../..         (grandparent)
- List files:
  - ls               (names)
  - ls -l            (detailed)
  - ls -a            (include hidden)
  - ls -lah /path    (detailed + human sizes + hidden)
  - ls ./subdir      (list subdir from cwd)
- Examples:
  - mkdir project
  - cd project
  - pwd  → /home/sai/project
  - ls -lah ~/public_html
  - cd /var/log/apache2
  - cd ../../        (go up two levels)

Keep this sheet for quick lookup of commands, path rules, and common ls options.

---

## Module 3 — Lecture 20: File & Directory Creation and Deletion (Linux)

#keywords: #file #directory #filesystem #create #delete #touch #mkdir #rm #rmdir #ls #recursive #force #interactive

## Key Definitions
- touch: create an empty file or update file timestamp.
- mkdir: create a new directory.
- ls: list files and directories in current directory.
- rm: remove (delete) files (and directories with options).
- rmdir: remove an empty directory.
- -R / -r (recursive): apply operation recursively into subdirectories.
- -f (force): do not prompt, ignore nonexistent files, suppress errors.
- -i (interactive): prompt before each removal.

## Command Syntax (quick "formulas")
- Create file: touch filename
- Create directory: mkdir dirname
- List files: ls [options]
- Delete file: rm filename
- Delete multiple files: rm file1 file2 ...
- Delete directory (recursive): rm -r directory
- Force recursive delete: rm -rf directory
- Interactive recursive delete: rm -r -i directory
- Remove empty directory: rmdir dirname

## Key Concepts / Actions
- Create file:
  - touch sample.txt
  - editors (vi, gedit) can also create/edit files
- Create directory:
  - mkdir my_folder
- Delete file:
  - rm sample.txt (permanent deletion)
- Delete multiple files:
  - rm file1 file2 file3
- Delete directory:
  - rmdir dir  — only if dir is empty
  - rm -r dir — removes dir and all nested files/dirs
  - rm -rf dir — force remove without prompts
  - rm -r -i dir — ask confirmation for each item while recursing
- Verification:
  - Use ls to confirm creation/deletion

## Important Properties / Invariants
- rm deletes permanently (no trash/recycle by default) — irreversible from shell.
- rmdir only succeeds on empty directories.
- rm without -r will not delete directories.
- -f suppresses prompts and errors; -i requests confirmation; be cautious combining.
- Recursive deletion traverses into subdirectories and removes everything therein.
- Always verify targets before using rm -r or rm -rf.

## Quick Reference (scannable)
| Command | Effect | Example |
|---|---:|---|
| touch file | create empty file or update timestamp | touch sample.txt |
| mkdir dir | create directory | mkdir newdir |
| ls | list directory contents | ls |
| rm file | delete file (permanent) | rm example.txt |
| rm file1 file2 | delete multiple files | rm a.txt b.txt |
| rmdir dir | delete empty directory only | rmdir olddir |
| rm -r dir | delete dir and contents recursively | rm -r my_folder |
| rm -rf dir | force delete dir and contents (no prompts) | rm -rf my_folder |
| rm -r -i dir | recursive delete with confirmation per item | rm -r -i dir1 |

## Safety Tips / Patterns
- Prefer rm -r -i when unsure (prompts per file/dir).
- Double-check with ls before destructive commands.
- Avoid rm -rf / and be cautious with wildcards (*).
- If you need recoverable deletions, use a trash utility or move to a designated backup directory rather than rm.
- When removing nested dirs, confirmations occur per-level/item when -i is used (you may be asked for each nested directory/file).

# End of cheatsheet — quick look-up tags: #touch #mkdir #ls #rm #rmdir #recursive #force #interactive #filesystem #delete #create

---

## Module 3 — Lecture 21: Copying & Moving Files and Directories — Cheatsheet

#cp #mv #copy #move #recursive #-r #file #directory #rename #filesystem #Unix #Linux #command #shell #resource-intensive

## Key Definitions
- cp: copy command — copies files or directories (creates new file(s)).  
- mv: move command — moves or renames files/directories (does not create a duplicate).  
- source: path/name of file/dir to copy or move.  
- destination: path/name where the item will be copied/moved to.  
- recursive (-r): option to process directories and their contents recursively (required for directory copy).  
- rename: changing a file/dir name using mv (same directory).

## Syntax / Formulas
- cp [options] source... destination
- cp -r source_directory destination_directory
- mv source... destination
- mv old_name new_name  (rename)
- mv file target_directory  (move into target dir)

## Key Algorithms / Concepts
- #cp: copies single or multiple files; leaves original(s) intact.
- #cp -r: required to copy directories and their contents recursively.
- #mv: renames if destination is a name in same directory; moves if destination is a different directory.
- #rename: use mv old_name new_name (no duplicate created).
- Moving a directory into another: mv dir target_dir (result: dir becomes a child of target_dir).
- Conflict behavior (transcript): cannot rename/overwrite a file with a directory of the same name (operation will not be allowed).

## Important Properties / Invariants
- cp creates a separate copy; original remains.
- mv does not create a second copy when renaming within same filesystem/location — the item is moved/renamed.
- To copy directories, always use -r (cp without -r cannot copy directories).
- Moving into an existing directory places the item under that directory (not overwrite a file with a directory).
- Recursive copy/move of large data can be time-consuming and resource-intensive — use with caution.

## Quick Reference (scannable)
- Copy file to new filename (same directory)
  - cp 1.txt 2.txt  → creates 2.txt as a copy of 1.txt
- Copy file into directory (as same name)
  - cp 1.txt dir/1.txt  → copy 1.txt into dir (dir should exist)
- Copy directory recursively
  - cp -r dir1 dir2  → copies dir1 and its contents into dir2 (creates dir2/dir1 or copies into dir2 depending on usage)
- Rename file
  - mv old_name.txt new_name.txt  → old_name removed, new_name appears
- Move file into directory
  - mv 1.txt dir/  → 1.txt moved into dir
- Rename/move directory
  - mv dir2 dir3  → renames dir2 to dir3 (within same parent) or moves dir2 under dir3 if dir3 exists as directory
- Move directory into another directory
  - mv 3 1  → moves directory 3 as a child of directory 1

## Short Tips
- Use cp -r for directories (#recursive).  
- Use mv to rename without duplication (#rename).  
- Check destination path carefully: moves/renames are destructive to source (mv removes source).  
- Avoid recursive operations on very large directories unless necessary (resource/time cost).


---

## Module 3 — Lecture 22: File & Directory Permissions (Unix/Linux) — Cheatsheet

#keywords
#permissions #ownership #file #directory #rwx #octal #chmod #chown #chgrp #setuid #setgid #stickybit #user #group #others #superuser

---

## Key Definitions (one-line)
- Owner: user who owns a file/directory.  
- Group: group associated with a file; group members get group permissions.  
- Others: all users not owner or in group.  
- Permission bits: read (r), write (w), execute (x).  
- Symbolic notation: e.g., rwx r-x r-- (owner / group / others).  
- Octal notation: 3-digit mode like 755 (owner/group/others) or 4-digit with special bits.  
- setuid: special bit causing executable to run with file-owner privileges.  
- setgid: special bit causing executable to run with file-group privileges (or directories inherit group).  
- sticky bit: on a directory, restricts deletion to file owner, directory owner, or superuser.  
- Superuser (root): has overriding privileges.

---

## Formulas / Mappings
- Permission bit values: r = 4, w = 2, x = 1  
- Octal digit = sum of bits present (e.g., rw- = 4+2 = 6)  
- Standard mode: OWNER (hundreds) | GROUP (tens) | OTHERS (ones)  
  - Example: 755 -> owner=7 (rwx), group=5 (r-x), others=5 (r-x)  
- Special (leading) octal bits: setuid = 4, setgid = 2, sticky = 1  
  - Example: 4755 -> setuid + 755

---

## Key Commands & Concepts
- chmod (change mode / permissions)
  - Symbolic: chmod u+r file.txt (add read to owner)  
  - Symbolic multi: chmod g-w,o-w file.txt (remove write from group & others)  
  - Octal: chmod 644 file.txt
  - Special bits: chmod u+s file (setuid symbolically), chmod g+s dir (setgid)
- chown (change owner and/or group)
  - Usage: chown new_owner file; chown new_owner:new_group file
- chgrp (change group only)
  - Usage: chgrp new_group file
- Permission sets: three groups — owner / group / others (#rwx)
- Special bits:
  - #setuid: executable runs with file-owner privileges
  - #setgid: executable runs with file-group privileges; on directories causes group inheritance
  - #stickybit: on directories, controls who can delete/rename files inside

---

## Important Properties & Invariants
- Permission order always: owner, group, others.  
- Symbolic operators: + (add), - (remove), = (set exactly).  
- Octal → symbolic mapping is deterministic via r=4, w=2, x=1.  
- setuid/setgid affect effective privileges during execution, not file contents.  
- Sticky bit only meaningful on directories for deletion control.  
- Owner (or root) can change a file's permissions with chmod; changing ownership (chown) typically requires appropriate privileges (often root).  
- File execute + setuid/setgid: display as 's' (if execute bit set) or 'S' (if execute not set) in ls -l; sticky shown as 't' or 'T'.

---

## Quick Reference (scannable)
- Permission letters: r = read, w = write, x = execute
- Bit values: r=4, w=2, x=1 → octal digit = sum
- Common modes:
  - 755 -> rwx r-x r-x (owner full, others/read+exec)
  - 644 -> rw- r-- r-- (owner read/write, others read)
  - 700 -> rwx --- --- (owner only)
  - 600 -> rw- --- --- (owner read/write only)
- Special bits (leading digit):
  - 4--- : setuid
  - 2--- : setgid
  - 1--- : sticky
  - Example: 2755 -> setgid + 755 (directory inherits group)
- ls -l symbols:
  - owner exec position: 's' (setuid+exec), 'S' (setuid only)  
  - group exec position: 's' (setgid+exec), 'S' (setgid only)  
  - others exec position on dir: 't' (sticky+exec), 'T' (sticky only)
- Examples:
  - chmod u+r file.txt — add read for owner (#chmod #symbolic)  
  - chmod 644 file.txt — set rw- r-- r-- (#chmod #octal)  
  - chown alice file.txt — change owner to alice (#chown)  
  - chown alice:devs file.txt — owner alice, group devs (#chown #chgrp)  
  - chgrp devs file.txt — change group to devs (#chgrp)
- Deletion rules in sticky directory:
  - Only file owner, directory owner, or superuser can remove files (#stickybit)

---

Tags for quick search: #permissions #ownership #rwx #octal #chmod #chown #chgrp #setuid #setgid #stickybit #owner #group #others

--- 

Keep this sheet nearby during open-book exams for quick lookup of commands, octal-symbolic mappings, and special-bit behavior.

---

## Module 3 — Lecture 23: Linux disk-usage & links — Cheatsheet

#hashtags: #df #du #ncdu #readlink #unlink #ls #symlink #hardlink #diskusage #filesystem

---

## Key Definitions
- df: show filesystem disk space usage (per mounted filesystem).  
- du: estimate disk usage of files/directories (per path).  
- ncdu: ncurses-based interactive disk-usage explorer.  
- symbolic link (symlink): a filesystem entry that points to another pathname (can be dangling, crosses filesystems). #symlink  
- hard link: another directory entry pointing to the same inode (same file contents, cannot cross filesystems, not for dirs normally). #hardlink  
- readlink: print the target of a symbolic link. #readlink  
- unlink: remove a name (link) from the filesystem. #unlink  
- ls -A / ls -l: list files (incl. hidden); long listing shows link targets and file types. #ls

---

## Formulas / Notation
- Human-readable sizes: -h shows sizes in KB/MB/GB (powers of 1024 for GNU tools). #units  
- df columns (typical): Filesystem | Size | Used | Avail | Use% | Mounted on  
- du summary flags: -s (summarize per argument), -c (show grand total). #du

---

## Key Commands & Usage (quick reference)
| Command | Syntax | Purpose / Notes |
|---|---:|---|
| df | df -h | Show disk usage per filesystem in human-readable form. #df |
| du | du -h <path> | Show sizes of files/dirs (human-readable). #du |
| du (summary) | du -s <path> | Show only total size for each argument. #du |
| du (grand total) | du -c <paths> | Include grand total at end. #du |
| ncdu | ncdu <path> | Interactive, navigable disk usage explorer. Use arrows/enter to drill down. #ncdu |
| readlink | readlink <symlink> | Print the target of a symlink. #readlink |
| unlink | unlink <path> | Remove a directory entry (link) — works for hard links and symlinks (removes the name). #unlink |
| ls (all) | ls -A | List all files except . and .. (includes hidden). #ls |
| ls (long) | ls -l | Long listing; leading char shows type (l = symlink) and for symlink shows "-> target". #ls |

---

## Important Properties / Invariants
- df reports per mounted filesystem; du reports by directory content (can differ due to mount points, sparse files, or reserved space). #df #du
- du counts space used by data referenced in the directory tree you give; files on other mounts under that path may not be included unless you traverse mounts. #du
- Symlink characteristics:
  - stores a pathname; can point to anything (file/dir); can be dangling; visible as type 'l' in ls -l. #symlink
  - Can cross filesystem boundaries. #symlink
- Hard link characteristics:
  - multiple names --> same inode; file data persists until last link (name) is removed. #hardlink
  - Cannot normally link across filesystems; linking to directories is restricted. #hardlink
- unlink removes a single name; if it was the last name, the inode/data are freed (subject to open file descriptors). #unlink
- readlink only prints the link target; does not resolve recursively by default (use readlink -f to canonicalize). #readlink

---

## Quick Reference / Patterns
- Common flags:
  - df -h : human-readable filesystem usage. #df
  - du -h : human-readable per-file/dir sizes. #du
  - du -sh : concise total for a path (s + h). Example: du -sh /var/log
  - du -hc * : sizes for each entry + grand total. #du
  - ncdu /path : interactive explore and sort by size. #ncdu
  - readlink -f <path> : print canonical absolute path (resolves symlinks). #readlink
  - ls -l : long format (look for leading 'l' for symlinks). #ls
- To list only symlinks in a directory:
  - find . -maxdepth 1 -type l -ls
  - or ls -l | grep '^l'  (quick heuristic). #symlink
- To remove a link safely:
  - unlink <symlink> or rm <symlink>
  - unlink <hardlink-name> removes that name; data remains if other hard links exist. #unlink
- When disk usage looks inconsistent:
  - Check df vs du: df shows filesystem-level free space; du sums directory usage — differences indicate other mounts, deleted-but-open files, reserved blocks, or sparse files. #df #du
- Use sudo when inspecting root-owned dirs: sudo du -sh /root

---

Keep this sheet nearby for fast lookup of command syntax, flags, and link behavior.

---

## Module 3 — Lecture 24: Linux Files & Directories — Cheatsheet

#hashtags: #linux #filesystem #files #directories #paths #hierarchy #bash #commands #create #update #delete #move #copy #ls #cd #pwd #mkdir #rmdir #touch #rm #cp #mv #cat #echo #redirection #globbing

---

## Key Definitions
- File: named collection of bytes stored on disk. #file  
- Directory: container that lists names and links to files and other directories. #directory  
- Filesystem: hierarchical organization of files and directories on storage. #filesystem  
- Root (/): top-level directory of the filesystem hierarchy. #root  
- Working directory: current directory for the shell; shown by `pwd`. #cwd #pwd  
- Absolute path: full path from root (starts with `/`). #absolutepath  
- Relative path: path relative to current directory (no leading `/`). #relativepath  
- `.` : current directory. #dot  
- `..` : parent directory. #dotdot  
- Hidden file: filename beginning with `.`; not shown by default by `ls`. #hiddenfile

---

## Formulas / Syntax Patterns
- Path syntax: /root/subdir/.../file or ./subdir/file or ../sibling/file  
- Command general form: command [options] <operands>  
- Redirection: `>` overwrite, `>>` append  (e.g., `echo hi > file`) #redirection  
- Globbing (wildcards): `*` (any chars), `?` (one char), `[...]` (set) #globbing

---

## Key Commands & Concepts (quick bullets)
- Navigation
  - `pwd` — print working directory. #pwd  
  - `cd <dir>` — change directory; `cd ~` to home, `cd -` previous. #cd
  - `ls` — list directory contents; common flags: `-l`, `-a`, `-h`. #ls
- Create files & directories
  - `touch <file>` — create empty file or update timestamp. #touch  
  - `mkdir <dir>` — create directory; `-p` for parent dirs. #mkdir
- Read/update file contents
  - `cat <file>` — print file contents. #cat  
  - `echo "text" > file` — write (overwrite) text to file. #echo #redirection  
  - `echo "text" >> file` — append text to file. #redirection
- Copy, move, rename
  - `cp src dst` — copy file(s); `-r` recursive for directories. #cp  
  - `mv src dst` — move or rename files/dirs. #mv
- Delete
  - `rm file` — remove file; `rm -r dir` remove directory recursively; `rmdir dir` remove empty dir. #rm #rmdir
- Info & metadata
  - `stat <file>` — status information (size, timestamps, inode). #stat (if available)  
  - `file <file>` — identify file type. #file
- Permissions & ownership (reference)
  - `ls -l` shows permission bits and owner/group. #permissions  
  - `chmod`, `chown` — change permissions/owner (syntax not expanded here). #chmod #chown

---

## Important Properties / Invariants
- Filesystem is hierarchical (tree) with unique absolute paths. #hierarchy  
- Filenames are case-sensitive on typical Linux filesystems.  
- Directories link names to inodes (names can point to same inode via hard links; symbolic links are special files) — (reference). #inode #symlink  
- `mkdir -p` avoids intermediate errors; `rm -r` is destructive — use with care. #safety  
- Hidden files begin with `.` and require `ls -a` to list. #hiddenfile
- Relative operations depend on current working directory scope. #cwd

---

## Quick Reference (commands table)
- Navigation
  - `pwd` — show cwd
  - `cd <dir>` — change dir (`cd ..`, `cd -`, `cd ~`)
  - `ls` — list (`-l` long, `-a` all, `-h` human sizes)
- Create / Read / Write
  - `touch file` — create empty or update timestamp
  - `mkdir dir` — create dir (`-p` parents)
  - `cat file` — display file
  - `echo text > file` — overwrite file
  - `echo text >> file` — append to file
- Copy / Move / Rename / Delete
  - `cp src dst` — copy (`-r` for dirs)
  - `mv src dst` — move/rename
  - `rm file` — remove file
  - `rm -r dir` — remove dir recursively
  - `rmdir dir` — remove empty dir
- Search & meta
  - `ls -l` — permissions, owner, size, date
  - `stat file` — detailed metadata
  - `file file` — detect type

Safety tips (quick):
- Preview before delete: `ls` the target first.  
- Use `rm -i` or `-v` for interactive/verbose removal.  
- Use `cp -r` and `mv` carefully across filesystems (behavior differs).

---

Use this as a compact reference during the exam — commands, flags, and path rules are the most-queried items. Keep practicing commands in a shell to internalize behavior.

---

## Module 3 — Lecture 25: Linux File System Cheatsheet

#hashtags: #Linux #filesystem #partition #blockdevice #bootblock #superblock #inode #inodeTable #datablocks #mount #links #hardlink #softlink #symboliclink #permissions #rwx #chmod #umask #ls #stat #du #df #ncdu #stickybit #setuid #setgid #commands

---

---

## Key Definitions (one-line)
- File system: mechanism that organizes and manages files and directories on a storage device. #filesystem  
- Partition: logical section of a physical disk that can hold a file system. #partition  
- Block device: hardware device that transfers data in fixed-size blocks (HDD/SSD/CD). #blockdevice  
- Boot block: block(s) holding bootstrap code required for system boot. #bootblock  
- Superblock: file-system-level metadata (size, capacity, free space, owner). #superblock  
- Inode: unique metadata record for a file (inode number); does NOT contain filename or file data. #inode #inodeTable  
- Inode table: collection of all inode entries (UID, GID, size, timestamps, permissions, link count, pointers). #inodeTable  
- Data blocks: blocks that store the actual file contents. #datablocks  
- Mount: attach a file system to the directory tree so it’s accessible. #mount  
- Hard link: a directory entry that points to the same inode as the original file (same inode number). #hardlink  
- Soft (symbolic) link: a special file that points (path) to another file; has its own inode and can span file systems. #softlink #symboliclink  
- Link count: number of directory entries (hard links) pointing to an inode; when it reaches 0 (and not open), kernel frees data. #links  
- Permission bits (r/w/x): read, write, execute for user/group/others. #permissions #rwx  
- umask: default mask used at file/directory creation to remove permission bits from default mode. #umask  
- Sticky bit: directory-special permission preventing users from deleting/renaming files unless they own them (set by +t). #stickybit  
- setuid / setgid: special bits to run executable with file owner’s or group’s privileges. #setuid #setgid

---

## Formulas / Notation
- Default creation modes:
  - Files default: 666 (rw-rw-rw-) — execute cleared by default
  - Directories default: 777 (rwxrwxrwx)
- umask effect (correct formula): resulting_mode = default_mode & (~umask)
  - Example: default file 666 & ~022 = 644 (rw-r--r--)
  - Note: lecturer phrased as “remove bits” — do not treat as simple decimal subtraction.
- Octal to bits (binary → rwx):
  - 0 = --- (0) ; 1 = --x (1) ; 2 = -w- (2) ; 3 = -wx (3)
  - 4 = r-- (4) ; 5 = r-x (5) ; 6 = rw- (6) ; 7 = rwx (7)

---

## Key Concepts & Commands (quick bullets)
- Filesystem layout (4 parts): Boot block | Superblock | Inode list (table) | Data blocks. #bootblock #superblock #inode #datablocks
- Block devices listing:
  - lsblk (or blkid / cat /proc/partitions) — shows block devices and sizes. #blockdevice
- Find mounted file systems:
  - df -h — disk free per filesystem (human-readable). #df
  - stat -f -c %T . — prints FS type of current directory (example: ext4). #stat
- File metadata:
  - stat filename — detailed inode & timestamps, size, blocks, link count. #stat #inode
- ls -l layout: filetype+permissions | link count | owner | group | size | timestamp | name
  - Filetype letters: - regular, d directory, l symlink, b block dev, c char dev, p pipe, s socket. #ls
- Permission changes:
  - chmod [symbolic] user/group/other +/- r/w/x filename
  - chmod [octal] 644 filename  (user=6 rw-, group=4 r--, others=4 r--)
  - Examples:
    - chmod u+x file  (add execute for user)
    - chmod 764 file  (user=rwx group=rw- others=r--)
- umask:
  - Set with umask 022 (shell); affects new file/dir modes.
  - Interpret: umask bits are removed from default_mode. Example: umask 022 -> files 644, dirs 755. #umask
- Disk usage tools:
  - du -sh path — disk usage of files/dirs. #du
  - df -h — free space on filesystems. #df
  - ncdu — interactive curses-based disk usage navigator (scan/delete/sort). #ncdu
- Links:
  - Create hard link: ln source target  (same inode; cannot cross filesystems). #hardlink
  - Create symbolic link: ln -s target linkname  (separate inode; can cross filesystems; becomes dangling if target removed). #softlink #symboliclink
  - Remove a link: rm linkname or unlink linkname
  - Hard link behavior: link count increments; data freed only when link count = 0 (and no process holds it). #links
- Special permission bits:
  - setuid: chmod u+s file (executable runs with file owner privileges). #setuid
  - setgid: chmod g+s file (executable runs with file group privileges; on directories, new files inherit group). #setgid
  - sticky bit: chmod +t dir (on directories prevents deletion/rename by non-owners). #stickybit

---

## Important Properties / Invariants
- Inode does NOT contain filename or file data — directory entries map filename -> inode number. #inode #inodeTable
- A directory is a file that stores mappings of names → inode numbers. #filesystem
- Hard links = same inode number; soft links = separate inode pointing to a path. #hardlink #softlink
- Hard links cannot span filesystems; symbolic links can. #hardlink #softlink
- Deleting a directory entry removes a name; file data persists while link count > 0 (and while open by processes). #links
- ls -l permission string: first char = file type; next 9 chars = user/group/other (rwx groups). #ls

---

## Quick Reference (tables & snippets)

Permission octal → rwx
- 7 = rwx | 6 = rw- | 5 = r-x | 4 = r-- | 3 = -wx | 2 = -w- | 1 = --x | 0 = ---

Common ls -l examples:
- -rw-r--r-- 1 alice staff 1234 Feb 21 file.txt  → regular file, user=rw-, group=r--, others=r--

Common commands (one-liners)
- ls -l          — long listing (permissions, links, owner, size, time, name) #ls
- stat file      — inode, size, timestamps, link count, device, blocks #stat
- df -h          — filesystem disk free/used #df
- du -sh dir     — size of dir (summarized) #du
- ncdu           — interactive disk usage navigator #ncdu
- chmod 644 f    — set permissions using octal #chmod
- chmod u+x f    — add execute for user #chmod
- umask 022      — set default mask (typical) #umask
- ln src tgt     — create hard link #hardlink
- ln -s tgt link — create symbolic link #softlink
- unlink link    — remove a link #commands
- rm file        — remove file (deletes directory entry; data freed when linkcount=0 & not open) #commands
- mv / cp / mkdir / pwd — standard file ops #commands

umask calculation examples
- File default 666, umask 022 → 666 & ~022 = 644 (rw-r--r--)
- Dir default 777, umask 002 → 777 & ~002 = 775 (rwxrwxr-x)

File type letters (ls -l first char)
- - regular file
- d directory
- l symlink
- b block device
- c character device
- p named pipe (FIFO)
- s socket

Link-count & delete quick facts
- Hard link creation: link count increments.
- Deleting one name: only removes that directory entry; other hard links still access file.
- Data is freed when link count reaches 0 (and no process holds the file open).

---

Keep this sheet near your notes: use hashtags to quickly search topics (#inode, #permissions, #umask, #hardlink, #softlink, #du, #df, #ncdu). Good luck on the open-book exam!

---

## Module 4 — Lecture 26: Open files & File Descriptor Management — Cheatsheet

#hashtags: #filedescriptor #open #close #read #write #fcntl #dup #dup2 #strace #lsof #ulimit #dd #ps #Linux #I/O #systemcalls #descriptormanagement

---

## Key Definitions
- File descriptor (FD): small integer handle used by a process to access an open file or data stream.  
- Standard FDs: 0 = stdin, 1 = stdout, 2 = stderr. #stdin #stdout #stderr
- Open file (file description): kernel object representing an open file (stores offset, flags) shared by FDs that refer to the same open.  
- File table (per-process FD table): maps FD → pointer to open file description.  
- Resource leak (FD leak): unused/unclosed FD left open causing wasted resources.  
- Blocking / Non-blocking: I/O behavior that waits (blocks) or returns immediately (non-blocking). #nonblocking

---

## System Call Signatures / Return Conventions
- int open(const char *pathname, int flags, mode_t mode);
- int close(int fd);
- ssize_t read(int fd, void *buf, size_t count);
- ssize_t write(int fd, const void *buf, size_t count);
- int fcntl(int fd, int cmd, ...);
- int dup(int oldfd);
- int dup2(int oldfd, int newfd);

Return values:
- open, dup, dup2: non‑negative FD on success; -1 on error (errno set).  
- read/write: number of bytes read/written (0 for EOF on read), -1 on error.

---

## Key Algorithms / Concepts
- #open: create/open file → kernel allocates/open file description → returns FD.  
- #close: release FD → decrement open-file refcount; free when zero.  
- #read / #write: transfer between process buffer and file; update file offset in shared open description.  
- #dup: return smallest unused FD referring to same open description (shares offset, flags).  
- #dup2: duplicate oldfd to specified newfd (closes newfd first if open).  
- #fcntl: manipulate FD properties (e.g., F_GETFD/F_SETFD, F_GETFL/F_SETFL, set O_NONBLOCK, FD_CLOEXEC). #F_GETFL #O_NONBLOCK #FD_CLOEXEC
- FD sharing: multiple FDs can point to same file description → shared file offset & status flags.

---

## Commands (quick usage)
- strace: trace syscalls and signals.
  - Examples:
    - strace [options] command args
    - strace -e open,read,write command
    - strace -o trace_output.txt command
    - strace -p PID (attach)
  - Options: -e (filter syscalls), -o (output file), -p (attach). #strace
- lsof: list open files by processes.
  - Examples:
    - lsof -c process_name   (filter by command)
    - lsof -u username       (filter by user)
  - Output columns: COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME. #lsof
- ulimit: view/set shell resource limits.
  - ulimit -n             (show max open file descriptors per process)
  - ulimit -n <value>     (set new limit in shell)
  - Note: system/global limits may restrict max value. #ulimit
- dd: data copy/benchmark tool (shows records read/written).
  - Syntax: dd if=<infile> of=<outfile> bs=<blocksize>
  - Records calculation: records = ceil(total_bytes / bs) (dd reports records read/written). #dd
- ps: list processes (used with lsof to inspect FD ownership). #ps

---

## Important Properties / Invariants
- Each process has its own FD table (integers → open descriptions). #process
- Standard FDs (0,1,2) exist at process start unless closed/redirected. #standards
- dup / dup2 produce FDs that reference the same open file description → same file offset and certain flags are shared. #dup
- fcntl can change per-FD flags (close-on-exec) and per-description flags (nonblocking). #fcntl
- Closing an FD only affects that FD; underlying file is freed when last reference removed. #close
- Failure to close FDs → FD leaks → resource exhaustion (ulimit enforced). #resourceleak
- read/write return semantics: read returns 0 at EOF; write may write fewer bytes than requested (check return). #readwrite

---

## Quick Reference (scannable)
- Standard FDs: 0 stdin | 1 stdout | 2 stderr
- Common syscalls:
  - open(path, flags[, mode]) → FD or -1
  - close(fd) → 0 or -1
  - read(fd, buf, n) → bytes_read or -1 (0 = EOF)
  - write(fd, buf, n) → bytes_written or -1
  - dup(oldfd) → newfd (smallest unused)
  - dup2(oldfd, newfd) → newfd (closes newfd first if open)
  - fcntl(fd, cmd, arg) → depends on cmd
- strace flags: -e (expr filter), -o file, -p PID
- lsof filters: -c (command), -u (user)
- ulimit: -n shows/sets max open FDs for the shell
- dd: dd if=in of=out bs=512 → records = ceil(bytes/512)
  - Example: bytes=3489, bs=512 → records = ceil(3489/512)=7 → dd reports 7 records in/out.
- fd limit: check with ulimit -n; raising requires privileges/system config.
- Error handling: check return values; on -1 inspect errno for cause (#EINVAL, #EMFILE, #ENFILE, #EBADF).
  - EMFILE = per-process FD limit reached; ENFILE = system-wide limit reached. #EMFILE #ENFILE

---

Use this sheet to quickly find syscall names/signatures, common command flags, FD invariants (sharing/closing), and commands to diagnose FD usage (strace, lsof, ulimit, dd, ps).

---

## Module 4 — Lecture 27: In-memory File System (TMPFS) — Cheatsheet

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

---

## Module 4 — Lecture 28: Linux File System Layout & Implementation — Cheatsheet

#keywords: #filesystem #linux #hierarchy #directories #mount #virtualfilesystem #devicefile #ext4 #xfs #btrfs #zfs #fat32 #ntfs #journaling #snapshot #COW

---

## Key Definitions
- Root: `/` — top-level directory; all paths under this. #root
- Absolute path: path starting with `/`. #path
- Relative path: path relative to current directory (no leading `/`). #path
- Home directory: `~` or `/home/<user>` — default user directory. #home
- Mount point: directory where another filesystem is attached. #mount
- Device file: special files in `/dev` that represent hardware or virtual devices. #devicefile #dev
- Virtual filesystem: in-memory pseudo-filesystems exposing kernel/process info (e.g., `/proc`, `/sys`). #virtualfilesystem #proc #sys
- Filesystem implementation: on-disk (or on-device) organization and access logic (Ext4, XFS, Btrfs, ZFS, etc.). #ext4 #xfs #btrfs #zfs

---

## Filesystem Layout — Standard & System Directories (quick table)
| Directory | Purpose | Hashtag |
|---|---:|---|
| `/bin` | Essential user executables (commands used by all users). | #bin |
| `/sbin` | System/admin executables (root/admin tools). | #sbin |
| `/usr` | User programs, libraries, docs (read-only at runtime). | #usr |
| `/var` | Variable data: logs, mail, spool, caches, temp runtime data. | #var |
| `/etc` | System configuration files. | #etc |
| `/dev` | Device files (hardware/virtual devices). | #dev |
| `/proc` | Process & kernel info (virtual FS). | #proc |
| `/sys` | Kernel data structures & config (virtual FS). | #sys |
| `/home` | Users' home directories. | #home |
| `/mnt`, `/media` | Common mount points for temporary/media mounts. | #mount |

---

## Formulas / Notation
- Path separator: `/`
- Home shorthand: `~` = `/home/<user>`
- Mount command (syntax): mount <device> <mount-point>  (use `-t <fstype>` to specify) #mount
- Common inspection: `df -h`, `lsblk`, `mount` (list mounted FS)

---

## Key Algorithms / Concepts
- Hierarchical file system: tree structure with single root; directories contain files/subdirs. #hierarchy
- Standard vs System directories: standard for users (`/usr`, `/home`); system controlled (`/sbin`, `/etc`). #systemdirs
- Mounting: attach filesystems at mount points; multiple filesystems can be mounted anywhere under `/`. #mount
- Virtual filesystems:
  - `/proc`: runtime process & kernel metadata (not persisted). #proc
  - `/sys`: kernel object model & configuration (sysfs). #sys
- Device files: special inode types representing device interfaces (character/block). #devicefile
- Filesystem features by type:
  - Ext4: default, journaling, supports large files/partitions, backward-compatible with ext3/ext2. #ext4 #journaling
  - XFS: high-performance, scalable, suitable for large storage. #xfs
  - Btrfs: modern, snapshots, subvolumes, compression, checksums, COW. #btrfs #snapshot #COW
  - ZFS: pooled storage, integrated volume management, checksums, robust data protection (not native but widely used). #zfs
  - FAT32 / NTFS: Windows-compatible filesystems used for interchange. #fat32 #ntfs

---

## Important Properties / Invariants
- Single root hierarchy: every file/directory reachable under `/`. #root
- Mounts can hide underlying directory contents while mounted. #mount
- Virtual filesystems (`/proc`, `/sys`) are ephemeral (not stored on disk). #virtualfilesystem
- Journaling (Ext4, XFS): helps recover metadata (and optionally data) after crashes. #journaling
- COW (Btrfs, ZFS): writes create new blocks — enables snapshots and stronger integrity features. #COW
- Snapshots/subvolumes: allow point-in-time views and cheap clones (Btrfs/ZFS). #snapshot
- Device interface layer: `/dev` provides filesystem-accessible handles to hardware. #devicefile

---

## Quick Reference (scannable)
- Common dirs: `/bin` `/sbin` `/usr` `/var` `/etc` `/dev` `/proc` `/sys` `/home` `/mnt` `/media` #directories
- Mount common commands:
  - mount <device> <dir>  (mount device to dir) #mount
  - umount <dir|device>  (unmount) #mount
  - mount -t <type> ...  (specify FS type) #mount
- Inspect:
  - df -h  (space usage) #df
  - lsblk  (block devices) #lsblk
  - blkid  (labels/UUIDs) #blkid
  - cat /proc/mounts or mount  (list mounts) #proc
- When to choose FS:
  - Ext4: general-purpose, compatibility, stable. #ext4
  - XFS: large filesystems, high throughput. #xfs
  - Btrfs: snapshots, subvolumes, compression, modern features. #btrfs
  - ZFS: enterprise features, data integrity, pooling (often via native kernel module or FUSE). #zfs
  - FAT32/NTFS: cross-OS compatibility (Windows). #fat32 #ntfs
- Virtual FS notes:
  - /proc: process IDs as directories, kernel tunables (/proc/sys). #proc
  - /sys: device and driver attributes, writable knobs for hardware params. #sys
- Permissions & control: system directories typically require root to modify (`/sbin`, `/etc`, `/usr`). #permissions

---

If you want, I can:
- Add a one-page printable PDF layout,
- Include common command examples (mkfs.*, fsck, tune2fs, btrfs subvolume/snapshot commands),
- Or expand the table with typical default mount points and sample usages.

---

## Module 4 — Lecture 29: Superblocks — Linux file system metadata cheatsheet

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

---

## Module 4 — Lecture 30: Path-name to Inode (Linux) — Cheat Sheet

#hashtags: #inode #filesystem #path-resolution #directory #directory-entry #tokenization #traversal #metadata #root #inode-number #file-data

## Key Definitions
- inode: Index node; filesystem data structure holding file metadata and pointers to data blocks. #inode
- inode number: Unique identifier for each file/directory in the filesystem. #inode-number
- directory entry: Mapping from a name (string) → inode number stored in a directory. #directory-entry
- path tokenization: Splitting a path into components (tokens) e.g., /home/user/file -> ["home","user","file"]. #tokenization
- path resolution / traversal: Sequentially following directory entries from a start inode to reach the target inode. #path-resolution
- root inode: Starting inode for absolute paths (commonly inode 1). #root

## Formulas / Notation
- Let k = number of path components (tokens).
  - Path resolution time ∝ k (linear in path depth): T = O(k) (ignoring per-directory lookup cost). #complexity
- Directory lookup per component: cost depends on directory implementation (linear/hashed/B-tree) — overall resolution cost = Σ lookup_cost(component_i).

## Key Algorithms / Concepts
- Tokenize path
  - Remove leading “/”, split on “/” → sequence of name tokens. #tokenization
- Start at root inode (absolute path) or CWD inode (relative path). #root
- For each token in order:
  - Read current directory’s entries, find name → get inode number. #directory-entry #traversal
  - Set current inode = found inode; continue to next token.
- Stop when final token resolved → final inode represents file/dir. #inode
- Use final inode to:
  - Read metadata (permissions, ownership, timestamps). #metadata
  - Follow block pointers to access file data blocks. #file-data

## Important Properties / Invariants
- Each file/directory has exactly one inode number (unique). #inode-number
- Directories store name → inode mappings (directory entries). #directory-entry
- Absolute paths: traversal always starts at root inode. #root
- Resolution proceeds component-by-component; failure to find any component = path not found.
- After resolution, inode provides both metadata and pointers to data blocks (content access). #metadata #file-data

## Example (walkthrough)
- Path: /home/user/documents/file1.txt
- Tokenize → ["home", "user", "documents", "file1.txt"]
- Traverse:
  - start inode 1 (/)
  - lookup "home" in inode 1 → inode 10
  - lookup "user" in inode 10 → inode 20
  - lookup "documents" in inode 20 → inode 30
  - lookup "file1.txt" in inode 30 → inode 40 (final)
- Final: inode 40 → metadata + data blocks. #inode

## Quick Reference (scannable)
- Steps:
  1. Tokenize path → tokens[]
  2. Set current = root inode (absolute) or CWD inode (relative)
  3. For each token t:
     - lookup t in current directory → next_inode
     - if not found → error (ENOENT)
     - current = next_inode
  4. Result = current (final inode) → use for metadata/data access
- Common failures: missing component, permission denied while reading a directory, broken symlink (not covered here). #traversal
- Useful reminders:
  - inode contains metadata + block pointers. #inode #metadata
  - directories = special files that map names → inode numbers. #directory
  - resolution cost grows with path depth (k). #complexity

Keep this sheet near your notes for quick lookup during path-resolution problems.

---

## Module 4 — Lecture 31: Linux Links Cheatsheet — Symbolic (Soft) vs Hard Links

#hashtags
#symbolic_link #soft_link #symlink #hard_link #inode #readlink #ln #ls #filesystem #dangling_link #symlink_chain #directory_entry #permissions #rm

---

## Key Definitions
- Symbolic link (symlink / soft link): a file that stores a path pointer to another file or directory.
- Hard link: an additional directory entry that references the same inode (same data) as the original file.
- Inode: filesystem metadata structure identifying file contents and attributes (st_nlink = link count).
- Dangling link: a symlink whose target path does not exist.
- Absolute path: full path from filesystem root (e.g., /home/user/dir/file).

---

## Commands / "Formulas"
- Create hard link: ln <target> <linkname>
- Create symbolic link: ln -s <target> <linkname>
- List long format (shows links): ls -l
- Show symlink target or resolved path: readlink <symlink>
- Resolve to final absolute path (follow chain): readlink -f <symlink>
- Remove file: rm <file> (affects entries/inode as below)

Filesystem/link relations:
- st_nlink = number of hard links to an inode
- File blocks freed when (st_nlink == 0) AND no process has it open

---

## Key Concepts
- #symlink points to a path string; can point to files or directories; can cross filesystems.
- #hard_link points to the same inode (same file contents/metadata); cannot span filesystems; typically cannot link directories.
- #readlink -f resolves symlink chains until it reaches a non-link file and prints absolute path.
- #ls -l displays symlinks with "-> target" and shows file types/colors (symlink often blue).
- Deleting the original file:
  - For #hard_link: other hard links still access the data (inode persists while st_nlink>0).
  - For #symlink: symlink becomes a #dangling_link if target removed.
- Permissions:
  - Symlink has its own directory entry and mode but not meaningful file permissions for target access; access controlled by target permissions.
  - Hard links share the same inode permissions; changing permissions affects all hard links.
- Operations on hard links (write/chmod) affect same underlying data.
- Symlink can form a chain (symlink -> symlink -> ... -> file); readlink -f follows chain.

---

## Important Properties / Invariants
- Hard links: multiple directory entries -> single inode; st_nlink increments per hard link.
- Symlinks: point to path string; no st_nlink increment on target.
- Deleting a filename removes a directory entry; only when inode link count reaches zero and no open descriptors are left are blocks freed.
- Symlinks are lightweight pointers — can become invalid if target moved/removed.
- Hard links cannot reference directories (to avoid cycles) and cannot cross filesystem boundaries.
- readlink -f resolves all symlinks in path and returns an absolute path or nothing if final target missing.

---

## Quick Reference (scannable)
- Create:
  - Hard: ln file.txt hl
  - Soft: ln -s /path/to/file.txt sl
- Inspect:
  - ls -l -> shows "name -> target" for symlink
  - readlink sl -> print symlink target (relative/path)
  - readlink -f sl -> print final absolute path, following any symlink chain
- Effects of rm file.txt:
  - Hard link hl remains usable (data intact)
  - Symlink sl becomes dangling (points to removed path)
- When to use:
  - Use #symlink when you need pointer across filesystems or to directories or want an easily-updated path pointer.
  - Use #hard_link when you want another indistinguishable directory entry to the same file data (same inode).
- Limitations:
  - Hard links: no directories, no cross-filesystem
  - Symlinks: can be dangling, stores path not inode
- Permissions:
  - chmod on inode affects all hard links
  - chmod on symlink typically affects target (or is ignored) — check system semantics

---

## Mini Comparison Table

| Feature | #symbolic_link (symlink) | #hard_link |
|---|---:|---:|
| Points to | path string | inode (same data) |
| Cross-filesystem | Yes | No |
| Can link dirs | Yes | Typically No |
| Affected by target deletion | Becomes dangling | Still usable |
| ls -l shows target | Yes (->) | No |
| readlink -f useful | Yes (resolves chain) | N/A |

---

Keep this as a quick lookup: ln/ln -s to create, ls -l and readlink/readlink -f to inspect, remember symlink stores path (can break), hard link shares inode (same file).

---

## Module 4 — Lecture 32: Linux filesystems — Data blocks & inodes (cheatsheet)

Keywords: #inode #datablock #filesystem #linux #unlink #rm #rmdir #df #debugfs #watch #allocation #extent #blockmap #monitoring #freeing

## Key Definitions
- inode: Metadata structure for a file/dir (permissions, timestamps, size, pointers to data blocks). #inode
- data block: Unit where file contents are stored on disk. #datablock
- block allocation map: Bitmap/structure tracking free/used blocks. #blockmap
- extent-based allocation: Stores ranges (extents) of contiguous blocks for a file. #extent
- unlink: Remove a directory entry (name) that points to an inode; decreases link count. #unlink
- rm/rmdir: User commands to remove files (`rm`) or empty directories (`rmdir`). #rm #rmdir
- df: Show filesystem disk usage; `df -i` shows inode counts. #df
- debugfs: Low-level interactive tool to inspect ext filesystems (inodes/blocks). #debugfs
- watch: Re-run a command periodically (default every 2s). #watch

## Formulas / Equations
- inode usage % = (used_inodes / total_inodes) * 100
- free_inodes = total_inodes − used_inodes
- file deletion condition for freeing blocks:
  - Data blocks freed when (link_count == 0) AND (no process has file open).

## Key Algorithms / Concepts
- #Allocation strategies
  - Block allocation map: track each block (free/used) via bitmap/lists.
  - Extent-based allocation: allocate contiguous block ranges for efficiency. #extent
- #Assignment
  - New file/dir -> allocate an inode; assign data blocks as needed for content.
- #Freeing
  - Deleting/unlinking a name marks its directory entry removed; inode may be freed and blocks reclaimed when link count and open-file conditions permit.
- #Monitoring
  - Regularly check `df -h` and `df -i` (inodes) to avoid running out of space or inodes. #monitoring
- #Debugging
  - Use `debugfs` to inspect inode/block internals and run `stat <inode>` on device. #debugfs

## Important Properties / Invariants
- One inode per file/directory; inodes contain pointers to data blocks. #inode
- A file needs an inode always; data blocks needed only if size > 0 (depends on FS). #datablock
- Deallocation is reclaimable: free inodes/blocks are reusable by filesystem.
- Removing a directory:
  - `rmdir` for empty dir
  - `rm -r` for recursive removal of non-empty dir. #rmdir #rm
- Link count (inode.nlink) controls when inode/blocks can be freed (and open file handles delay freeing).
- `df -i` shows inode exhaustion risk even when disk space remains. #df

## Quick Reference (scannable)

Commands
- unlink file
  - Syntax: `unlink <filename>` — removes one directory entry (decrements links). #unlink
- rm file
  - Syntax: `rm <filename>` — remove file (wrapper that typically calls unlink); `rm -r <dir>` recursive. #rm
- rmdir directory
  - Syntax: `rmdir <directory>` — remove only empty directory. #rmdir
- df (disk usage)
  - Show disk space: `df -h`
  - Show inode usage: `df -i` — outputs total, used, free, %iused. #df
  - Example (from lecture): total inodes = 494,328; used = 2; ~1% used.
- debugfs (inspect ext fs internals)
  - Syntax: `debugfs -R "stat <inode>" /dev/sda1` — run command and exit. #debugfs
  - Use for reading inode metadata, block pointers, extents.
- watch (monitor repeatedly)
  - Syntax: `watch df -i` — runs `df -i` every 2 seconds (default). #watch
  - Useful to observe inode/disk changes live.

Quick checks
- To see inode shortage risk: run `df -i` and check %iused.
- To monitor in real time: `watch -n 2 "df -h; df -i"`
- To inspect a suspected corrupted / inconsistent inode: `debugfs -R "stat <inode>" /dev/<device>`

Notes to remember (short)
- Deleting a file name does not immediately free blocks if link_count > 0 or the file is open. #unlink
- Always monitor both space and inodes; running out of inodes prevents creating new files even if space exists. #monitoring
- Extent allocation reduces fragmentation for large files. #extent

(tags used in this cheatsheet: #inode #datablock #filesystem #linux #unlink #rm #rmdir #df #debugfs #watch #allocation #extent #blockmap #monitoring #freeing)

---

## Module 4 — Lecture 33: Inode — Linux file metadata structure (cheatsheet)

Keywords: #inode #filesystem #metadata #permissions #timestamps #links #direct-blocks #indirect-blocks #ACL #extended-attributes #immutable #generation-number #file-size

---

## Key Definitions
- inode: #inode — data structure representing a file/directory’s metadata (not the filename).
- file mode / permissions: #permissions — bits encoding file type + owner/group/others read/write/execute.
- owner ID / group ID: #uid #gid — numeric user and group identifiers.
- file size: #file-size — size of file contents in bytes.
- atime: #atime — last access time (read).
- mtime: #mtime — last content modification time (write).
- ctime: #ctime — last inode metadata change (permissions, ownership, link count).
- links count: #links — number of hard links referencing the inode.
- direct block pointers: #direct-blocks — pointers from inode directly to data blocks (for small files).
- indirect block pointers: #indirect-blocks — single/double/triple indirection to reach more data blocks.
- extended attributes: #extended-attributes — extra attributes/flags (e.g., compression, immutable).
- ACL: #ACL — access control list entries stored/pointed to by inode where supported.
- generation number: #generation-number — unique id to avoid accidental inode reuse.
- filesystem-specific data: #fs-specific — reserved space for FS-specific extensions.

---

## Formulas / Equations
- Permission string format: rwx rwx rwx → owner / group / others (#permissions).
- Indirection capacity (blocks):
  - Let ND = number of direct pointers, P = pointers per block (block_size / pointer_size).
  - Addressable blocks ≈ ND + P + P^2 + P^3  (#direct-blocks #indirect-blocks)
- Max file size (approx):
  - max_file_size ≈ (ND + P + P^2 + P^3) × block_size  (#file-size)
- Inode free condition:
  - if (links_count == 0 AND no process has file open) → inode and data blocks reclaimed (#links).

---

## Key Algorithms / Concepts
- #Direct-vs-Indirect:
  - Direct pointers: fast access for small files.
  - Single indirect: inode → block of pointers → data blocks.
  - Double indirect: inode → block of pointers → block of pointers → data blocks.
  - Triple indirect: one more level for very large files.
- #Hard-link semantics:
  - Hard links share same inode; directory entries map names → inode numbers; inode holds link count.
- #Filename-vs-inode:
  - Directory entries map filenames to inode numbers; inode itself does NOT store filename.
- #Timestamps management:
  - atime/mtime/ctime maintained in inode; OS policies may modify atime updates for performance (e.g., relatime).
- #Extended-attributes / #ACL:
  - Inode may contain pointers or inline space for ACL entries and security contexts (e.g., POSIX ACL, SELinux).
- #Immutable-flag:
  - Immutable prevents modifications regardless of write permissions; controlled via inode flags.

---

## Important Properties / Invariants
- Inode does not include filename; directories map names → inode numbers. (#inode)
- Link count counts hard links only; soft (symbolic) links are separate filesystem entries. (#links)
- ctime ≠ mtime: ctime changes on metadata changes (permissions, owner, link count); mtime on content write. (#ctime #mtime)
- atime updated on reads (may be disabled/relatime for performance). (#atime)
- When link count reaches 0 and the file is not open, inode + blocks are freed. (#links)
- Mode bits include file type + owner/group/other permission bits (rwx). (#permissions)
- Filesystem may add FS-specific inode fields (compression, extended features). (#fs-specific)
- Generation number protects NFS/clients from inode number reuse issues. (#generation-number)

---

## Quick Reference
- Mode representation examples: 
  - rwxr-xr-- → owner=rwx (7), group=rx (5), others=r (4). (#permissions)
- Timestamp meanings:
  - atime = last read; mtime = last content write; ctime = last metadata change. (#atime #mtime #ctime)
- Link behavior:
  - ln (hard): increments inode.links; unlink/deleting a name decrements links.
  - rm removes directory entry; actual data freed only when links==0 and no open fds. (#links)
- Block addressing order (common):
  - use direct pointers → single indirect → double indirect → triple indirect. (#direct-blocks #indirect-blocks)
- Common inode fields (compact list):
  - mode, uid, gid, size, atime, mtime, ctime, links_count, block pointers, flags, generation, ACL ptrs, fs-specific. (#inode)
- Immutable vs mutable:
  - immutable flag set → no writes/rename/permission changes allowed even if owner writable. (#immutable)
- ACL/SEC:
  - POSIX ACL entries referenced by inode; security context may be stored in inode xattrs. (#ACL #extended-attributes)

---

Keep this sheet for quick lookup of inode fields, permissions, timestamp semantics, and block addressing limits.

---

## Module 4 — Lecture 34: File Systems: Superblock, Inodes, and Links — Cheatsheet

Keywords: #filesystem #superblock #inode #inodes #hardlink #symlink #symboliclink #links #metadata #Linux #data-storage #ln #ls #stat

---

## Key Definitions
- File system (#filesystem): Structures and rules for organizing, storing, and retrieving files on a storage device.
- Superblock (#superblock): File-system metadata block that stores global FS parameters and integrity info (size, block count, inode count, flags).
- Inode (#inode): Per-file metadata structure describing a file/dir (ownership, permissions, timestamps, size, block pointers).
- Hard link (#hardlink): Directory entry that references the same inode as another name (same inode number).
- Symbolic (soft) link (#symlink #symboliclink): Special file that stores a pathname reference to another file.
- Metadata (#metadata): Data about files (permissions, owner, size, timestamps, pointers) stored in superblock & inodes.

---

## Formulas / Equations
- Blocks required for a file: blocks = ceil(file_size / block_size)
- Generic max file size via inode pointers:
  max_size ≈ (D + S * P + Dbl * P^2 + Trp * P^3) * block_size
  - D = number of direct pointers
  - S/Dbl/Trp = 1 if single/double/triple indirect present (or counts of pointers)
  - P = pointers per block = block_size / pointer_size
  (Used to compute limits for inodes with direct/indirect pointers.)
- free_space = total_blocks - used_blocks (tracked in superblock/bitmaps)

---

## Key Concepts / Items (#hashtags included)
- Purpose of a file system (#filesystem): organize data, provide names/paths, manage free space, enforce permissions.
- Superblock (#superblock):
  - Stores FS-wide metadata: total size, block size, inode count, free block/inode counters, mount state, FS type, UUID.
  - Critical for integrity (fsck may use alternate superblocks).
- Inodes (#inode):
  - Contain metadata (mode, uid/gid, timestamps), link count, size, and pointers to data blocks (direct and indirect).
  - Directory entries map filenames → inode numbers.
  - Link count in inode indicates number of directory entries pointing to it.
- Links (#hardlink #symlink):
  - Hard link: another directory entry pointing to same inode (same data); link count increments; cannot span filesystems; usually cannot link directories.
  - Symbolic link: a separate inode containing a path string; can point across filesystems; can be dangling.
- Creating links (#ln #ln -s):
  - Hard link: ln target linkname
  - Symbolic link: ln -s target linkname
- Inspecting inodes and links (#ls #ls -i #stat):
  - ls -i shows inode number
  - stat filename shows inode metadata and link count
- Superblock recovery (#fsck): filesystem check utilities use superblock/alternate copies to repair metadata.

---

## Important Properties / Invariants
- Inode uniqueness: each inode is unique; filenames are directory entries mapping to inode numbers.
- Link count consistency: inode.link_count == number of directory entries pointing to that inode.
- Hard links share the same inode and data blocks; deleting one name decrements link count, data freed only when link count hits 0 and no open file handles exist.
- Symbolic links contain a pathname; resolution occurs at path traversal time.
- Superblock is essential: corrupted superblock can render FS unusable; alternate superblocks (if present) are backups.
- Directories are special files that map name → inode; modifying directory entries updates inode link counts.

---

## Quick Reference (scannable)
- Commands:
  - Create hard link: ln <target> <linkname>  #hardlink #ln
  - Create symlink: ln -s <target> <linkname>  #symlink #ln
  - Show inode number: ls -i <file>  #ls
  - Show inode metadata: stat <file>  #stat
  - Check/repair FS: fsck /dev/xxx  #fsck #superblock
- Hard vs Soft Links (quick table):

  | Property | Hard Link (#hardlink) | Symbolic Link (#symlink) |
  |---|---:|---|
  | References inode directly | Yes | No (stores path) |
  | Cross-filesystem | No | Yes |
  | Can point to directories | Usually no | Yes |
  | Can be dangling | No | Yes |
  | Shares inode number | Yes | No |

- Typical inode fields to expect: inode_number, mode (type+perm), uid/gid, size, atime/mtime/ctime, link_count, block_pointers.
- Calculating required blocks: blocks = ceil(file_size / block_size).
- Common problems to remember:
  - Dangling symlink: target removed → symlink broken.
  - Orphan inode (link_count = 0 but allocated): recovered by fsck if unreferenced.
  - Superblock corrupt: use backup/alternate superblock when available.
- Use ls -li to display inode and long listing in one view.

---

Keep this sheet near your exam materials for quick lookup of #superblock, #inode, and link behavior in #Linux file systems.

---

## Module 4 — Lecture 35: Linux filesystems & I/O cheatsheet

#keywords: #inode #filesystem #filedescriptor #open #read #write #close #fcntl #strace #lsof #tmpfs #dd #dup #dup2 #dumpe2fs #debugfs #ulimit #O_NONBLOCK #inode-table #superblock

---

---

## Key Definitions (one-line)
- inode: unique numeric descriptor for a file (stores metadata & block pointers, NOT the filename) #inode
- directory entry: mapping (filename ↔ inode number) stored in a directory #directory
- inode table: filesystem structure storing inode metadata (link count, block pointers, timestamps, etc.) #inode-table
- data block: disk block(s) storing the actual file content #datablock
- hard link: directory entry that points to an inode; increases inode link count #hardlink
- file descriptor (FD): non-negative integer handle the OS gives a process to reference an open file/device #filedescriptor
- open file / open file table: kernel structures representing an opened file (FD -> open-file-entry -> inode) #openfile
- superblock: filesystem-wide metadata (total inodes, blocks, block size, mount info) #superblock
- tmpfs: in-memory temporary filesystem (volatile, fast, shrinks/grows with RAM) #tmpfs
- non-blocking I/O: file/FD mode allowing I/O calls to return immediately if they would block (O_NONBLOCK) #O_NONBLOCK

---

## Formulas / Notation / Quick facts
- reserved FDs: 0 = stdin, 1 = stdout, 2 = stderr (first user-assigned FDs start at 3) #stdin #stdout #stderr
- dd syntax (common): dd if=<input> of=<output> bs=<blocksize> status=progress  #dd
- dup(2) / dup2(2) syscall patterns:
  - newfd = dup(oldfd)        — duplicate to lowest unused FD #dup
  - dup2(oldfd, newfd)       — duplicate into specific newfd (closes newfd first if open) #dup2
- fcntl usage: flags = fcntl(fd, F_GETFL); fcntl(fd, F_SETFL, flags | O_NONBLOCK)  #fcntl #O_NONBLOCK

---

## Key Algorithms / Concepts (bulleted)
- Path resolution → inode (component-wise):
  - start at root (inode e.g. 2), split path into components, for each component: lookup directory entry → get inode number → read inode → continue. #path-resolution #inode
- File deletion flow:
  - remove directory entry (filename → inode mapping)
  - decrement inode link count
  - if link count > 0 → inode/data remain
  - if link count == 0 and no open references → free inode and free data blocks (made available for reuse)
  - if file still open by process → free delayed until last reference closed/exited #file-deletion
- Data recovery implication:
  - deletion frees blocks but does not zero them; data persists until overwritten (possible recovery until overwritten). #data-recovery
- FD lifecycle:
  - open() returns FD; use read()/write() with FD; close(fd) releases FD back to kernel.limit. #open #read #write #close
- Duplicating FDs:
  - dup/dup2 let one open file be referenced by multiple FDs (useful to redirect stdout/stderr to files or pipes). #dup #dup2
- fcntl and O_NONBLOCK:
  - use fcntl to get/set flags (non-blocking I/O, advisory locks, etc.); O_NONBLOCK enables async-style behavior (no waiting on read/write). #fcntl #O_NONBLOCK
- tmpfs:
  - stores files in RAM, fast, volatile (data lost on reboot), useful for temp data / caches. #tmpfs

---

## Important Properties / Invariants
- Filenames live in directories; inodes do not contain the filename. #inode
- Multiple directory entries (hard links) can reference the same inode; inode has a link count. #hardlink
- Inode numbers and data blocks are reused after being freed (no guarantee of uniqueness over time). #inode-reuse
- A file is only truly freed when link count == 0 AND no process has it open. #file-lifecycle
- FD numbers are per-process and small integers (0..); kernel maps FDs to open-file structures. #filedescriptor
- tmpfs uses RAM: fast but limited and volatile (risk of memory pressure). #tmpfs

---

## Common syscalls / commands (quick ref)
- Syscalls (C / kernel): open(), read(), write(), close(), dup(), dup2(), fcntl()  #open #read #write #close #dup #dup2 #fcntl
- strace: strace -e trace=open,close,read,write <cmd> (trace syscalls & signals) #strace
- lsof: list open files (filter by PID, user, path, port) #lsof
- ulimit: show/set per-shell resource limits (max file size, open files, stack, etc.) #ulimit
- dd: low-level copy/clone disks & partitions — dd if=/dev/sdX of=image.img bs=4M status=progress  #dd
- dumpe2fs: sudo dumpe2fs /dev/xxx or dumpe2fs <mountpoint> — dump ext* filesystem superblock info #dumpe2fs
- debugfs: interactive debugging of ext* FS (dangerous; admin use only) #debugfs
- watch: watch -n <secs> <command> — continuously run and display command output (e.g., watch -n2 df -h) #watch
- df -h: show filesystem usage (type column shows fs type like ext4, tmpfs, xfs, btrfs, zfs) #df

---

## Quick Reference (scannable)
- FD reserved: 0=stdin, 1=stdout, 2=stderr; user FDs start ≥3 #stdin #stdout #stderr
- Delete file steps: remove dir entry → link_count-- → if link_count==0 && no open refs → free data blocks + free inode #file-deletion
- Recoverability: data recoverable until overwritten (blocks are freed but not zeroed) #data-recovery
- Duplicate FD: dup(oldfd) → lowest unused FD; dup2(oldfd,newfd) → force newfd to refer to oldfd #dup #dup2
- Make FD non-blocking:
  - flags = fcntl(fd, F_GETFL)
  - fcntl(fd, F_SETFL, flags | O_NONBLOCK) #fcntl #O_NONBLOCK
- tmpfs: fast, volatile, uses RAM; good for temp/caches; data lost on reboot; watch memory usage #tmpfs
- dd common template: dd if=<source> of=<dest> bs=<blocksize> status=progress (use carefully) #dd
- View filesystem superblock: sudo dumpe2fs <device|mountpoint>  #dumpe2fs
- Trace syscalls: strace -o trace.txt -e trace=open,close,read,write <cmd>  #strace
- List open files: lsof -p <PID>  OR lsof +D <directory>  #lsof
- Monitor FS usage: watch -n 2 df -h  or watch -n 2 'dumpe2fs ...' (admin) #watch

---

## Filesystems to remember
- ext4: common Linux filesystem (superblock, journaling) #ext4
- xfs: high-performance, scalable for large filesystems #xfs
- btrfs: copy-on-write, snapshots, multi-device #btrfs
- zfs: advanced features, checksums, snapshots, pooling (not native everywhere) #zfs
- tmpfs: in-memory temporary fs (volatile) #tmpfs

---

Keep this cheat sheet handy for quick lookups on path→inode resolution, deletion semantics, FD rules, and the admin commands (strace / lsof / dumpe2fs / debugfs / dd / watch / ulimit).

---

## Module 5 — Lecture 36: Kernel I/O Structure & Linux I/O Cheatsheet

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

---

## Module 5 — Lecture 37: Block vs Character Devices — Linux I/O Cheatsheet

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

---

## Module 5 — Lecture 38: Linux Device Drivers — Cheatsheet

#keywords: #deviceDrivers #Linux #kernelSpace #userSpace #kernelModule #deviceFiles #systemCalls #kernelInterfaces #lsmod #modinfo #insmod #rmmod #ls_dev #characterDevice #blockDevice

## Key Definitions
- Device driver: Software that intermediates between hardware and the OS, enabling control and communication. #deviceDrivers
- Kernel-space driver: Driver integrated into the kernel with direct access to kernel resources and hardware. #kernelSpace
- User-space driver: Driver running outside the kernel, using system calls / kernel interfaces to access hardware. #userSpace
- Kernel module: Loadable piece of kernel code that implements a driver or kernel feature. #kernelModule
- Device file (/dev): Special filesystem entries representing devices (block/character). #deviceFiles #blockDevice #characterDevice
- System call: Kernel-provided API for user-space programs to request kernel services. #systemCalls
- Kernel interface: Set of APIs and mechanisms the kernel exposes for drivers. #kernelInterfaces

## Formulas / Equations
- None in transcript (N/A)

## Key Algorithms / Concepts
- Role of drivers:
  - Mediates OS ↔ hardware communication and control. #deviceDrivers
  - Manages peripherals (graphics, network, USB, storage). #deviceFiles
- Types of drivers:
  - Kernel-space: low-level, high-performance, direct hardware access. #kernelSpace
  - User-space: runs in userland, flexible, load/unload dynamically, incurs user↔kernel transition overhead. #userSpace
- Writing drivers:
  - Requires understanding kernel interfaces + target hardware. #kernelInterfaces
  - Correct implementation improves system performance & stability. #deviceDrivers #kernelModule

## Important Properties / Invariants
- Kernel-space drivers:
  - Direct access to kernel resources; preferred for critical/performance-sensitive tasks. #kernelSpace
- User-space drivers:
  - Safer to develop/iterate; can be dynamically loaded/unloaded; performance overhead due to boundary crossing. #userSpace
- Device files:
  - Provide userland access to devices (listed in /dev). #deviceFiles
- Kernel modules:
  - Can be loaded/unloaded at runtime (dynamic). #kernelModule
- Security & stability:
  - Buggy kernel drivers can crash the system; correctness is critical. #kernelSpace #kernelModule

## Commands Quick Reference (scannable)
| Command | Purpose | Typical usage |
|---|---:|---|
| lsmod | List currently loaded kernel modules | lsmod #lsmod |
| modinfo | Display information about a specific module | modinfo <module> #modinfo |
| insmod | Load a kernel module into the running kernel | insmod <module.ko> #insmod |
| rmmod | Unload a kernel module from the running kernel | rmmod <module> #rmmod |
| ls /dev | Show device files (character & block devices) | ls /dev #ls_dev #deviceFiles |

- Notes:
  - insmod/rmmod operate on kernel modules (.ko) and names; modinfo prints metadata (ver, deps, params). #kernelModule
  - ls /dev lists entries representing physical/virtual devices; differentiate block vs character devices. #blockDevice #characterDevice

## Quick Reference — Scannable Facts
- Device drivers = required for OS to control hardware. #deviceDrivers
- Kernel-space: faster, privileged, riskier. #kernelSpace
- User-space: safer/flexible, slower due to system calls. #userSpace
- Kernel modules can be dynamically loaded/unloaded (insmod/rmmod). #kernelModule #insmod #rmmod
- Use lsmod to see loaded modules; use modinfo to inspect a module. #lsmod #modinfo
- Device files live under /dev; used to access hardware from userland. #ls_dev #deviceFiles
- Writing drivers needs kernel API + hardware docs; correct drivers improve performance/stability. #kernelInterfaces

(End of cheatsheet)

---

## Module 5 — Lecture 39: I/O Queuing, I/O Scheduling & Interrupt Handling — Linux (Cheatsheet)

Keywords
- #IO #I/O #IOQueuing #IOScheduling #Interrupts #ISR #irqreturn_t #CFQ #Deadline #NOOP #/sys #/proc #proc_interrupts #blockdevice #SSD #HDD #LinuxKernel

Key Definitions
- I/O queuing: Kernel mechanism that buffers and orders pending I/O requests from CPUs/devices to improve throughput and latency.
- I/O scheduler: Kernel component deciding service order of pending block I/O requests.
- Interrupt: Hardware signal to CPU indicating device needs immediate attention.
- Interrupt handler / ISR: Kernel routine registered to process a specific hardware interrupt.
- irqreturn_t: Return type used by Linux interrupt handlers (indicates handled/not handled).
- Block device: Device that supports buffered block I/O (e.g., /dev/sda).
- /sys filesystem: Kernel interface to view/change device and kernel settings (e.g., schedulers).
- /proc/interrupts: Procfs file showing counts of interrupts handled per CPU/device.

Formulas / Notation
- No explicit mathematical formulas in lecture.
- Common performance terms:
  - Latency: time for single I/O to complete
  - Throughput: I/O per second or MB/s
  - Fairness / deadline = qualitative metrics (no formula provided)

Key Algorithms / Concepts
- #CFQ (Completely Fair Queuing)
  - Fair distribution of I/O bandwidth across processes; good for desktop/interactive workloads.
- #Deadline
  - Ensures time-bounded servicing of requests to improve responsiveness for real-time/latency-sensitive tasks.
- #NOOP
  - Simple FIFO/merge-based scheduler with minimal overhead; good for low-latency devices (e.g., #SSD) or hardware that does its own scheduling.
- Changing scheduler per block device
  - Use /sys/block/<device>/queue/scheduler to view/change scheduler.
- Interrupt Handling
  - Devices raise interrupts -> CPU invokes registered ISR -> ISR services device (quick) and may schedule deferred work.
- Viewing interrupt stats
  - /proc/interrupts shows interrupt counts by CPU and device.

Important Properties / Invariants
- Scheduler choice affects latency vs throughput vs fairness; choose according to workload (interactive vs batch vs realtime) and device (HDD vs SSD).
- NOOP minimizes CPU-side reordering; better when device-level controller optimizes ordering (SSD/NVMe).
- Deadline provides upper bounds on request wait time (improves predictability).
- CFQ provides per-process fairness; may add overhead.
- Interrupt handlers should be short (do minimal work) to avoid blocking CPU; defer long work to bottom halves/tasklets/workqueues.
- Changing scheduler is per-block-device and immediate (takes effect at kernel level).
- Many operations require root privileges (use sudo).

Quick Reference (Commands, Paths, Examples)
- Show current scheduler for /dev/sda:
  - cat /sys/block/sda/queue/scheduler
  - Output format example: "[cfq] noop deadline" (brackets = current)
- Set scheduler for /dev/sda (requires root):
  - echo cfq  > /sys/block/sda/queue/scheduler
  - echo deadline > /sys/block/sda/queue/scheduler
  - echo noop > /sys/block/sda/queue/scheduler
  - Use sudo if needed: sudo sh -c 'echo deadline > /sys/block/sda/queue/scheduler'
- View interrupt statistics:
  - cat /proc/interrupts
- Register / implement ISR (kernel module typical pattern):
  - Prototype: irqreturn_t handler(int irq, void *dev_id)
  - Register: request_irq(irq, handler, flags, name, dev_id)
  - Unregister: free_irq(irq, dev_id)
  - (Use sparingly and with correct flags; requires kernel/module programming)
- Permissions:
  - Many /sys and /proc writes require root. Use sudo and be cautious.

Scheduler Quick Comparison (scannable)
- CFQ (#CFQ)
  - Pros: fairness, good for interactive
  - Cons: overhead, may not suit SSDs
- Deadline (#Deadline)
  - Pros: bounded latency, predictable
  - Cons: less fairness for throughput
- NOOP (#NOOP)
  - Pros: minimal overhead, good for SSD/NVMe or stacked schedulers
  - Cons: no fairness / time guarantees

Gotchas / Tips
- Default scheduler may vary by kernel/version and device (check /sys/block/<dev>/queue/scheduler).
- Writing incorrect values or interfering with drivers can destabilize system—use caution.
- Interrupts can be balanced across CPUs by kernel settings (not covered in depth in this lecture).
- Prefer NOOP for hardware that handles its own queuing (NVMe controllers); prefer Deadline or CFQ when predictability or fairness is required.

One-line summary
- Use /sys/block/<dev>/queue/scheduler to view/change I/O scheduler (#CFQ, #Deadline, #NOOP) based on workload and device; use /proc/interrupts and irqreturn_t/ISRs to monitor and handle hardware interrupts.

---

## Module 5 — Lecture 40: Partitioning & Inspecting Hard Disks in Linux — Cheatsheet

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

---

## Module 5 — Lecture 41: Linux Block Devices & Disk-Utilities — Cheatsheet

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

---

## Module 5 — Lecture 42: hwinfo & parted — Linux hardware & partition cheatsheet

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

---

## Module 5 — Lecture 43: Disk Tools Cheatsheet — cfdisk, sfdisk, smartctl

#hashtags: #cfdisk #sfdisk #smartctl #partitioning #SMART #disks #linux #storage #console #scriptable #io-redirect #sudo #root

---

## Key Definitions
- cfdisk: Interactive, console-based disk partitioning utility.
- sfdisk: Scriptable partitioning utility for programmatic partition table edits.
- smartctl: SMART (Self-Monitoring, Analysis and Reporting Technology) control/monitoring tool for storage devices.
- Partition table: Metadata describing disk partitions (MBR/GPT).
- IO redirection: Shell operators `<` (input) and `>` (output) used to feed or capture command I/O.

---

## Syntax / Commands (Formulas & Examples)
- Run cfdisk (interactive):  
  sudo cfdisk /dev/sdb
- sfdisk from script (create partitions):  
  sudo sfdisk /dev/sdb < partition_script.txt
- sfdisk dump partition table to file:  
  sudo sfdisk -d /dev/sdb > partition_table.txt
- smartctl show all info:  
  sudo smartctl -a /dev/sda
- smartctl device info / SMART support:  
  sudo smartctl -i /dev/sda
- smartctl run short test:  
  sudo smartctl -t short /dev/sda
- smartctl view self-test results:  
  sudo smartctl -l selftest /dev/sda

(Note: most operations require root — use sudo.)

---

## Key Algorithms / Concepts
- #cfdisk: Menu-driven steps — New, Delete, [Type], Write, Quit — good for ad-hoc interactive partitioning.
- #sfdisk: Text-based, repeatable partitioning via scripts; ideal for automation and imaging.
- #smartctl: Query device SMART attributes, run self-tests, review logs to assess drive health.
- #IO-redirection: Use `<` to feed scripts into sfdisk; use `>` to capture sfdisk dumps or smartctl output.

---

## Important Properties / Invariants
- cfdisk changes are not persisted until you select Write and confirm (e.g., "yes").
- sfdisk modifies partition table based on input script — non-interactive and destructive if script is wrong.
- smartctl commands depend on device SMART support — use `smartctl -i` to verify.
- Always operate on device nodes (e.g., /dev/sda, /dev/sdb), not mounted filesystem paths.
- Partitioning operations can cause data loss — always backup before modifying.
- SMART tests take time (short/long); check results with `-l selftest`.

---

## Quick Reference (scannable)
- Interactive partitioning:
  - Command: sudo cfdisk /dev/<disk>
  - UI actions: New → size/type, Delete → select, Write → confirm, Quit
- Scripted partitioning:
  - Create: sudo sfdisk /dev/<disk> < partition_script.txt
  - Dump: sudo sfdisk -d /dev/<disk> > partition_table.txt
- SMART monitoring:
  - Info/support: sudo smartctl -i /dev/<disk>  #check SMART capability
  - Full attributes: sudo smartctl -a /dev/<disk>
  - Start short test: sudo smartctl -t short /dev/<disk>
  - Show self-test log: sudo smartctl -l selftest /dev/<disk>
- Common device names: /dev/sda, /dev/sdb, /dev/nvme0n1 (NVMe devices may require different device paths/options)
- Safety checklist before partitioning:
  - Backup important data
  - Unmount partitions on target disk
  - Confirm target device name (avoid /dev/sda mix-ups)
  - Use scripts with dry-run / verification where possible

---

## Quick Command Table
| Tool | Purpose | Key flags / usage |
|---|---:|---|
| cfdisk | Interactive partition editor | sudo cfdisk /dev/sdX — use menu: New/Delete/Write |
| sfdisk | Scriptable partitioning | sudo sfdisk /dev/sdX < script.txt ; sudo sfdisk -d /dev/sdX > table.txt |
| smartctl | SMART monitoring & tests | sudo smartctl -i/-a/-t short/-l selftest /dev/sdX |

---

Keep this sheet open during the exam for fast lookup of command syntax, flags, and safety reminders.

---

## Module 5 — Lecture 44: smartmontools & smartctl — Disk Health Monitoring (Linux) Cheat Sheet

Keywords: #smartmontools #smartctl #SMART #disk #hdd #ssd #selftest #health #monitoring #linux #apt #smartattributes #selftestlog #temperature #disktemp

---

## Key Definitions
- #SMART — Self-Monitoring, Analysis, and Reporting Technology built into most modern drives.  
- #smartmontools — Package providing smartctl CLI to access SMART data.  
- #smartctl — Command-line tool to query and control SMART on drives.  
- #DevicePath — Block device path (e.g., /dev/sda) passed to smartctl.  
- #ShortSelfTest — Quick built-in SMART test (few minutes).  
- #LongSelfTest — Thorough SMART test (can take hours).  
- #SelfTestLog — Log of past SMART self-tests and results.  
- #SMARTAttribute — Individual health metric reported by SMART (e.g., temperature, reallocated sectors).

---

## Formulas / Command Syntax (quick)
- smartctl [options] <device>  
- Install (Debian/Ubuntu): `sudo apt-get install smartmontools`  #linux #apt  
- Basic info: `smartctl -i <device>`  #smartctl #info  
- Full SMART report: `smartctl -a <device>`  #smartctl #report  
- SMART attributes: `smartctl -A <device>`  #smartattributes  
- Run short test: `smartctl -t short <device>`  #shortselftest  
- Run long test: `smartctl -t long <device>`  #longselftest  
- Show self-test log: `smartctl -l selftest <device>`  #selftestlog  
- Check temperature (example): `smartctl -A <device> | grep -i temperature`  #temperature

---

## Key Concepts / Operations
- Install package: use distro package manager (e.g., apt).  #smartmontools  
- Query device info: `-i` returns model, serial, firmware.  #smartctl  
- Dump SMART data: `-a` shows attributes, error logs, self-test results.  #SMART  
- List attributes: `-A` gives per-attribute raw and normalized values.  #smartattributes  
- Run self-tests: `-t short` (quick) or `-t long` (thorough).  #selftest  
- Inspect self-test results: `-l selftest` displays history and outcomes.  #selftestlog  
- Extract temperature: use `-A` and text filtering (grep).  #disktemp  
- Interpretation rule: non-zero or rising attribute values may indicate problems.  #health #monitoring

---

## Important Properties / Invariants
- SMART is built into most HDDs/SSDs but may vary by vendor.  #SMART  
- Many SMART attributes are counters; increases or non-zero critical fields can signal failure.  #smartattributes  
- Short tests are fast but less thorough; long tests are comprehensive and slower.  #shortselftest #longselftest  
- smartctl usually requires root privileges (use sudo).  #linux  
- Device path is required and must be the correct block device (e.g., /dev/sda).  #DevicePath  
- Regular monitoring helps detect issues early and reduce data-loss risk.  #monitoring

---

## Quick Reference (scannable)
- Install: `sudo apt-get install smartmontools`  #apt  
- Info: `smartctl -i /dev/sdX`  — model, serial, firmware  #smartctl  
- Full dump: `smartctl -a /dev/sdX`  — attributes, logs, tests  #SMART  
- Attributes only: `smartctl -A /dev/sdX`  #smartattributes  
- Start short test: `smartctl -t short /dev/sdX`  — check later with selftest log  #shortselftest  
- Start long test: `smartctl -t long /dev/sdX`  #longselftest  
- View self-test log: `smartctl -l selftest /dev/sdX`  #selftestlog  
- Temperature: `smartctl -A /dev/sdX | grep -i temperature`  #temperature  
- Interpret: watch for increasing counters (e.g., reallocated sectors) and non-zero critical attributes.  #health

---

Tags for quick search: #smartmontools #smartctl #SMART #disk #hdd #ssd #selftest #health #monitoring #linux #apt #smartattributes #selftestlog #temperature

(End of cheatsheet)

---

## Module 5 — Lecture 45: Linux Kernel I/O & Device Management — Cheatsheet

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

---

## Module 5 — Lecture 46: Kernel I/O & Linux I/O Utilities — Cheatsheet

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

---

## Module 6 — Lecture 47: vi Editor Cheatsheet

#vi #editor #linux #terminal #text-editor #modes #navigation #editing #commands #save #quit #delete #copy #paste #redirection #options

## Key Definitions
- Normal mode: Default mode for navigation and issuing commands. (aka command mode)
- Insert mode: Mode to insert/edit text (enter with i).
- Command-line mode: Mode for file-level commands (enter with :).
- Buffer: The in-memory contents of the file you are editing.
- Redirection: Shell operator to write command output to a file (e.g., vi --help > abc.txt).

## Startup Options (as in transcript)
- -r : recover file after crash (#-r)
- -c cmd : run a command after opening the file (#-c)
- -n : open file in read-only mode (#-n)
- -i {ext} : set backup extension (#-i)
- +N : open at line N (# +N)
- --help : show usage (#--help)

## Common Commands / Keybindings
- Open file: vi filename (#vi)
- Show help and save output: vi --help > abc.txt (#redirection)
- Enter Insert mode: i (#i)
- Exit to Normal mode: Esc (#esc)
- Enter Command-line mode: : (colon) (#colon)

Command-line (type after colon):
- :w  — write (save) file (# :w)
- :q  — quit (# :q)
- :wq — save and quit (# :wq)
- :q! — quit without saving (# :q!)

Normal-mode navigation:
- Arrow keys — move cursor (#arrows)
- h — left (#h)
- j — down (#j)
- k — up (#k)
- l — right (#l)

Normal-mode editing:
- x — delete character under cursor (#x)
- dd — delete current line (#dd)
- yy — yank (copy) current line (#yy)
- p — paste after cursor (#p)

## Important Properties / Invariants
- Modal behavior: Only one mode active at a time; Esc returns to Normal.
- : commands are issued from Command-line mode (start with colon).
- dd / yy operate on whole lines. x operates on single character under cursor.
- p pastes after the cursor/line (use P to paste before).
- Normal mode is required to run navigation and most editing commands.
- Insert mode shows -- INSERT -- (or similar) in the status area.

## Quick Reference (scannable)
- Start:
  - vi file.txt
  - vi --help > abc.txt
- Modes:
  - Normal (default) → i → Insert → Esc → Normal → : → Command-line
- Save / Quit:
  - Save: :w
  - Quit: :q
  - Save & quit: :wq
  - Quit w/o saving: :q!
- Navigation:
  - Left/Down/Up/Right: h / j / k / l (or arrow keys)
- Edit:
  - Delete char: x
  - Delete line: dd
  - Copy(yank) line: yy
  - Paste: p
- Startup options:
  - Recover: -r
  - Run command: -c 'cmd'
  - Read-only: -n
  - Backup ext: -i{ext}
  - Start at line: +N
- Tips:
  - Use Esc to ensure you’re in Normal mode before command keys.
  - Use :w before :q to avoid losing changes.
  - Use redirection to capture command output: command > file

## Search/Find (note from standard vi usage)
- Enter Command-line mode then use /pattern or ?pattern (not in transcript but common in vi)

Hashtags for quick search: #vi #editor #modes #normal-mode #insert-mode #command-line-mode #navigation #h #j #k #l #x #dd #yy #p #w #q #wq #q! #-r #-c #-n #-i #+N #--help #redirection

(Concise reference for exam use — focus on commands and mode transitions.)

---

## Module 6 — Lecture 48: Vi Editor — Modes & Essential Commands (cheatsheet)

#hashtags: #vi #vim #editor #NormalMode #InsertMode #CommandMode #ExCommandMode #navigation #search #replace #save #quit #editing #yank #paste

## Key Definitions
- Normal mode: Default modal state for navigation and issuing commands.
- Insert mode: Mode for inserting text (entered with i).
- Command mode: Ex/colon mode for file operations like save/quit (entered with :).
- Ex Command mode: Advanced command-line mode (starts with :), used for search/replace and other Ex commands.
- Cursor navigation: Movement in Normal mode via h/j/k/l (left/down/up/right).

## Formulas / Command Patterns
- Open file: vi filename
- Enter Insert mode: i
- Return to Normal mode: Esc
- Command/Ex mode prompt: :
- Search (transcript form): :/pattern Enter
  - Common alternative: /pattern Enter (forward search)
- Replace (global): :%s/old/new/g
  - Case-sensitive by default (capital/lower matters)

## Key Commands & Concepts
- Opening:
  - vi filename — open/create file (#vi #editor)
- Mode switching:
  - Normal → Insert: i (#InsertMode)
  - Any mode → Normal: Esc (#NormalMode)
  - Normal → Ex/Command: : (#CommandMode #ExCommandMode)
- Navigation (Normal mode): 
  - h = left, j = down, k = up, l = right (#navigation)
- Basic editing (Normal mode):
  - Delete character: x (#editing)
  - Delete line: dd (#editing)
  - Copy (yank) line: yy (#yank)
  - Paste after cursor: p (#paste)
- File operations (Ex/Command mode):
  - Save: :w (#save)
  - Quit: :q (#quit)
  - Save & quit: :wq or :x (#save #quit)
  - Force quit (discard changes): :q! (#quit)
- Search & replace (Ex mode):
  - Search: :/pattern Enter (or /pattern) (#search)
  - Replace all occurrences in file: :%s/old/new/g (#replace)
  - Replace with case matching — by default case-sensitive (watch capitalization)

## Important Properties / Invariants
- Vi is modal: same keys do different things depending on mode (#NormalMode #InsertMode).
- Editor opens in Normal mode by default.
- Esc always returns you to Normal mode from Insert or other modes.
- Ex/Command mode commands begin with : and execute when Enter is pressed.
- Search/replace using :%s is file-wide unless range is specified.
- Case sensitivity: searches and :s replacements are case-sensitive unless modified.

## Quick Reference (one-line commands)
- Open: vi filename
- Insert mode: i
- Back to Normal: Esc
- Move: h (←), j (↓), k (↑), l (→)
- Delete char: x
- Delete line: dd
- Yank line: yy
- Paste: p
- Save: :w
- Quit: :q
- Save & quit: :wq or :x
- Force quit: :q!
- Search (lecture form): :/word Enter
- Common search: /word Enter
- Replace all: :%s/old/new/g
- Replace (case-sensitive): ensure pattern matches exact case (e.g., L vs l)

## Examples (compact)
- Open file: vi ABC.TXT
- Search for "list": :/list Enter  (if case differs, search :/List)
- Replace all "list" → "enumerate": :%s/list/enumerate/g
- If "List" (capital L) present: :%s/List/enumerate/g

Keep this sheet near your notes for quick lookup during the exam.

---

## Module 6 — Lecture 49: vi/vim Quick Cheatsheet — Deleting & Common Shortcuts

#hashtags: #vi #vim #editor #linux #commands #shortcuts #delete #navigation #insertmode #search

---

## Key Definitions
- Normal (command) mode: default mode for commands (press Esc to enter).  
- Insert mode: editing/text-entry mode (enter with i, a, I, A).  
- Motion: movement commands used with operators (e.g., w, $, 0).  
- Count prefix: a number before a command to repeat it (e.g., 3dd).

---

## Formulas / Command Patterns
- [count] + command — repeat command (e.g., 3dd deletes 3 lines).  
- operator + motion — perform operator over a motion (d + w => dw).  
- d$ or D — delete from cursor to end of line.  
- r<char> — replace the character under the cursor with <char>.

---

## Key Commands / Concepts (#hashtags included)
- Delete single char: x (delete under cursor). #x  
  - X (uppercase) deletes character before cursor. #X
- Delete line: dd (delete current line). #dd  
  - [count]dd (e.g., 3dd) deletes that many lines. #count
- Delete to end of line: D or d$ (from cursor to EOL). #D #d$  
- Delete word: dw (delete from cursor to start of next word). #dw  
- Delete word + surrounding space: daw (delete around word). #daw
- Delete from cursor to end-of-line (single-key): D. #D
- Replace single character: r<char>. #r
- Undo / Redo: u (undo), Ctrl+R (redo). #undo #redo
- Save & Quit: :wq  (write and quit). #save #wq
- Quit without saving: :q!  (force quit). #quit #q!
- Insert mode entries: 
  - i (insert at cursor) #i
  - I (insert at beginning of line) #I
  - a (append after cursor) #a
  - A (append at end of line) #A
- Navigation:
  - 0 (zero) — beginning of line. #0
  - $ — end of line. #$
  - gg — beginning of file. #gg
  - G — end of file. #G
- Search:
  - /pattern then Enter — search forward. #search #/
  - n — next match. #n

---

## Important Properties / Invariants
- vi is modal: commands only work in Normal mode; Insert mode is for typing. #modal  
- Many operators use motions (d, c, y + motion). Memorize common motions (w, $, 0, gg, G). #motions  
- Count prefixes apply to most commands (e.g., 5w, 3dd). #count  
- Single-key commands are case-sensitive (x vs X, d vs D). #case

---

## Quick Reference Table (scannable)

| Action | Command(s) |
|---|---|
| Delete char under cursor | x |
| Delete char before cursor | X |
| Replace char with <c> | r<c> |
| Delete current line | dd |
| Delete N lines | Ndd (e.g., 3dd) |
| Delete to end of line | D or d$ |
| Delete word | dw |
| Delete word + surrounding space | daw |
| Enter insert mode (at cursor) | i |
| Insert at line start | I |
| Append after cursor | a |
| Append at line end | A |
| Save & quit | :wq |
| Quit without saving | :q! |
| Undo / Redo | u / Ctrl+R |
| Go to start/end of line | 0 / $ |
| Go to start/end of file | gg / G |
| Search forward | /pattern ↵ , then n for next |

---

## Quick Tips
- Prefix with a number to repeat (e.g., 4w, 2dd). #repeat  
- Use d + motion to delete flexible ranges (d0, d$, dw, da(, etc.). #d+motion  
- When unsure, press Esc to return to Normal mode. #Esc

---

Keep this sheet to quickly find keystrokes and patterns during the exam. Practice a few commands to build muscle memory.

---

## Module 6 — Lecture 50: vi/vim Misc Commands — Cheatsheet

# #vi #vim #editor #commands #search #replace #marks #indentation #linenumbers #navigation #join #split #repeat

## Key Definitions
- Normal mode: vi's default mode for navigation/commands (Esc to enter). #normal-mode  
- Insert mode: mode for inserting text (i, a, o to enter). #insert-mode  
- Command-line / Ex mode: enter with : to run commands (e.g., :s, :25). #ex-mode  
- Mark: named position in file set by m{char} and jumped to by ` or '. #marks  
- Pattern search: use /pattern to find next match. #search  
- Substitute: :s (ex command) to replace text; supports flags g, c, % etc. #substitute

## Formulas / Command Syntax (quick patterns)
- Repeat last edit: .  
- Search: /pattern <Enter>  
- Substitute (current line): :s/old/new/flags  
- Substitute (whole file): :%s/old/new/flags  
  - flags: g = global (all occurrences in line), c = confirm each (use together as gc or cg)  
- Jump to line N: :N (e.g., :25)  
- Set mark: m{a-z} (e.g., ma) — jump: `a (exact pos) or 'a (line)  
- Indent line: >> ; unindent: <<  
- Join lines: J (normal mode) or :join  
- Split line: insert newline at cursor (use i<Enter> or a<Enter>) — (transcript said 's', correct is inserting newline).  
- Toggle line numbers: :set number / :set nonumber

## Key Commands / Concepts
- #repeat
  - .  — repeat last change (works in normal mode).  
- #search
  - /pattern <Enter> — search forward for pattern. Use n (next) / N (prev) after.  
- #replace / #substitute
  - :s/old/new/g  — replace all occurrences on current line.  
  - :%s/old/new/g — replace all occurrences in file.  
  - :%s/old/new/gc — replace all in file with confirmation for each.  
- #marks
  - ma  — set mark 'a' at cursor.  
  - `a  — jump to exact cursor position at mark a.  
  - 'a  — jump to start of the line of mark a.  
- #navigation
  - :N  — go to line N (e.g., :25).  
  - :set number / :set nonumber — enable/disable line numbers.  
- #indentation
  - >>  — indent current line (can use a count, e.g., 3>>).  
  - <<  — unindent current line.  
- #join / #split
  - J  — join current line with next line.  
  - :join  — join lines (ex command).  
  - i<Enter> or a<Enter> — split line at cursor by inserting newline.  
- #misc
  - s  — delete character under cursor and enter insert (not "split line"). Use with caution.

## Important Properties / Invariants
- Commands in normal mode act immediately; many ex commands require leading colon (:). #normal-mode #ex-mode  
- :s without % affects only the current line; use range or % for more lines. #substitute  
- Flags order doesn't matter (e.g., /gc or /cg both valid). #substitute  
- Marks are single-character and local to the file (lowercase a–z). #marks  
- Indentation commands accept counts (e.g., 2>> indents two times). #indentation

## Quick Reference (scannable)
- Repeat last edit: .  
- Search forward: /pattern <Enter> ; next/prev: n / N  
- Replace (current line): :s/old/new/g  
- Replace (whole file): :%s/old/new/g ; confirm: :%s/old/new/gc  
- Go to line 25: :25  
- Toggle line numbers: :set number / :set nonumber  
- Set mark a: ma — jump: `a or 'a  
- Indent line: >>  — Unindent: <<  
- Split line at cursor: i<Enter> or a<Enter>  
- Join lines: J (normal) or :join  
- Delete char + insert: s (use carefully)  

Tags for quick search: #repeat #search #replace #substitute #marks #jump-to-line #indentation #line-numbers #join #split #dot-command

(Notes: cleaned up minor inaccuracies from transcript — primary substitute patterns and split/join commands shown as commonly used in vi/vim.)

---

## Module 6 — Lecture 51: vi — Copy, Cut, Paste Cheatsheet

# #vi #copy #paste #cut #yank #put #buffer #normal-mode #visual-mode #ex-command #yy #dd #p #y$ #range

## Key Definitions (one-line)
- Normal mode: vi's default mode for navigation and commands.  
- Visual mode: selection mode entered with v to highlight text for operations.  
- Yank: copy text into vi's unnamed buffer (command: y).  
- Put: paste text from buffer into file (command: p).  
- Delete (cut): remove text and place it into buffer (command: d).  
- Buffer: temporary storage where yanked/deleted text is kept.  
- Ex commandline: colon (:) commands for ranges and other operations.

## Formulas / Command Patterns
- [count]yy  — yank (copy) count full lines (default count = 1). Example: 3yy
- [count]dd  — delete (cut) count full lines. Example: 2dd
- p — put (paste) buffer contents below the cursor/line
- y$ — yank from cursor to end of line
- :start,end y — yank lines start through end in Ex mode. Example: :5,8 y
- v + movement + y — Visual mode selection then yank selected text

## Key Commands / Concepts (bullet list)
- yy — yank (copy) current entire line into buffer (#yy #yank)
- [n]yy — yank n lines starting at current line (e.g., 3yy) (#count)
- dd — delete (cut) current entire line into buffer (#dd #cut)
- [n]dd — delete n lines (cuts to buffer)
- p — paste (put) buffer contents below current cursor/line (#p #put)
- y$ — yank from cursor position to end of line (#y$)
- :m,n y — yank lines m through n via Ex command (e.g., :5,8 y) (#ex-command #range)
- v then movement then y — select text in Visual mode and yank selection (#visual-mode)
- Start commands in Normal mode (press Esc to ensure)

## Important Properties / Invariants
- p always pastes below (after) the cursor/line (transcript focus).  
- Yanked/deleted text goes to the unnamed buffer and is available to p immediately.  
- Numeric prefix repeats the command on lines (3yy = yank 3 lines; same for dd).  
- y$ uses motion operator pattern: yank + motion (here $ = end-of-line).  
- Ex-range yank uses line numbers and requires Enter after the command.  
- Visual mode selection uses movement keys and ends with y to yank.

## Quick Reference (scannable)
- Mode: Ensure Normal mode (press Esc)
- Copy line: yy
- Copy n lines: n yy (e.g., 3yy)
- Cut line: dd
- Cut n lines: n dd
- Paste below cursor/line: p
- Copy to end of line (from cursor): y$
- Copy line range: :start,end y (e.g., :5,8 y)
- Visual copy: v → move to select → y
- Note: Yank = copy, Put = paste

## Short Examples
- Copy line 10 to current: :10y then navigate and p
- Copy chars from cursor to EOL: position cursor → y$
- Copy 4 lines starting here: 4yy → move → p

#hashtags recap: #vi #yank #put #yy #dd #p #y$ #visual-mode #normal-mode #ex-command #range #buffer

(Keep this sheet handy — all commands assume you begin in Normal mode.)

---

## Module 6 — Lecture 52: Searching & Substitution in vi Editor — Cheatsheet

Keywords: #vi #vim #search #substitute #regex #regular-expressions #case-insensitive #case-sensitive #commands #normal-mode #command-mode

## Key Definitions
- Normal mode: vi mode for navigation and searching (press Esc to ensure).
- Command-line mode: invoked with ":" for commands like substitution.
- Search mode: initiated with "/" to type a search pattern.
- Pattern: a regular expression used to match text.
- Substitute command: :s (line) or :%s (whole file) to replace text.
- Flag: option after substitute (e.g., g, c) that modifies behavior.

## Common Commands (one-line)
- /pattern → start forward search for pattern (press Enter to run).
- n → go to next occurrence (forward).
- N → go to previous occurrence (backward).
- : → enter command-line mode.
- :s/old/new/ → replace first occurrence on current line.
- :s/old/new/g → replace all occurrences on current line.
- :%s/old/new/g → replace all occurrences in whole file.
- :%s/old/new/gc → replace all in file, confirm each change interactively.

## Regex Tokens / Notation (vi/vim)
- . → any single character (#regex)
- * → zero or more of previous atom (#regex)
- ^ → start of line (#regex)
- $ → end of line (#regex)
- \d → digit (in vim “magic” mode; works in many vim regexes) (#regex #digits)
- + → one or more (in basic vi/vim regex must escape: \+ ) — alternative: use very-magic mode \v and then +
- Note: vi/vim uses slightly different escaping rules; \+ is common for "one or more".

Examples:
- /^start → match lines beginning with "start"
- /end$ → match lines ending with "end"
- :%s/\d\+/NUMBER/g → replace digit sequences with NUMBER (use \d\+ or adjust regex magic)

## Case Sensitivity Modifiers
- /\cpattern → case-insensitive search (forces ignore case) (#case-insensitive)
- /\Cpattern → case-sensitive search (forces case-sensitive) (#case-sensitive)
- These modifiers are placed inside the search pattern.

## Important Properties / Invariants
- Searches are started from Normal mode using "/".
- n moves forward; N moves backward relative to the original search direction.
- :s operates on current line by default; prefix with range (e.g., % for whole file) to change scope.
- g flag on substitute = all matches in the addressed range/line; without g only first match per line is replaced.
- gc flags = global + confirm each replacement interactively.
- Regular expressions can be used in search and substitute; be cautious with metacharacters and escaping.
- Always preview or confirm large substitutions to avoid unintended replacements.

## Quick Reference (scannable)
- Open file: vi filename
- Start search: /pattern  (Enter)
- Next / previous match: n / N
- Case-insensitive search: /\cterm
- Case-sensitive search: /\Cterm
- Replace first on line: :s/old/new/
- Replace all on line: :s/old/new/g
- Replace whole file: :%s/old/new/g
- Replace whole file with confirm: :%s/old/new/gc
- Replace digits with word NUMBER: :%s/\d\+/NUMBER/g
- Common meta-chars: . * ^ $ \d \+
- Caution: use g flag carefully — can produce unintended global changes.

Hashtags (major concepts & commands): #vi #vim #search #substitute #regex #regular-expressions #case-insensitive #case-sensitive #normal-mode #command-mode #n #N #s #%s #gc #g

Note: vi/vim flavor differences exist for regex escaping (e.g., + often needs escaping as \+). If a pattern doesn't work, try escaping quantifiers or using very-magic mode (\v).

---

## Module 6 — Lecture 53: vi editor — Quick Cheatsheet

#hashtags: #vi #vim #text-editor #modal-editing #normal-mode #insert-mode #visual-mode #ex-mode #navigation #editing #search-and-replace #copy-paste #registers #macros #undo-redo

---

## Key Definitions
- Modal editor: editor with distinct modes (different keys do different things). #modal-editing  
- Normal mode: default mode for navigation and commands. #normal-mode  
- Insert mode: type text; enter with i/a/o. #insert-mode  
- Visual mode: select text (char/line/block) for commands. #visual-mode  
- Ex/Command-line mode: run commands starting with : or / ? . #ex-mode  
- Operator: command that acts on a text object or motion (e.g., d, c, y). #operators  
- Motion: movement command used by operators (e.g., w, $, t). #navigation  
- Register: named storage for yanks/deletes (", "a, etc.). #registers  
- Macro: recorded sequence of commands stored in a register (q<reg> ... q). #macros

---

## Command Pattern / Formula
- General form: [count] [operator] [motion]  
  - Example: 3dw = delete 3 words  
- Repeat last change: . (dot)  
- Substitute (line scope): :[range]s/pattern/replacement/[flags]  
  - Common: :%s/foo/bar/gc (global + confirm)

---

## Essential Commands (Quick Reference)
Navigation
- h / j / k / l = left / down / up / right  
- w / b / e = next word / back / end of word  
- 0 / ^ / $ = line start / first non-blank / line end  
- gg / G = top / bottom of file  
- Ctrl-d / Ctrl-u = half-page down / up  
- f<char> / t<char> = find / till char; F/T reverse  
- % = jump to matching bracket

Insert & Replace
- i / I = insert before cursor / line-start insert  
- a / A = append after cursor / line-end append  
- o / O = open new line below / above  
- r<char> = replace one char; R = enter replace mode

Editing / Operators
- x = delete char; X = delete before cursor  
- dd = delete line; D or d$ = delete to EOL  
- dw / dW = delete word  
- cw = change word (delete + insert)  
- c$ = change to end of line  
- s / S = substitute/delete and enter insert / line substitute

Yank & Paste
- y / yy = yank (copy) motion / line  
- p = paste after cursor; P = paste before cursor  
- "ay = yank into register a; "ap = paste from register a

Visual Mode
- v = char-wise select; V = line-wise; Ctrl-v = block-wise  
- > / < = indent selection; y/d/c = yank/delete/change selection

Search & Replace
- /pattern (enter) = forward search; ?pattern = backward  
- n / N = next / previous match  
- :%s/pat/repl/g = replace all in file; flags: g (global), c (confirm), i (ignore-case)

Files & Ex Commands
- :w = save; :q = quit; :wq or :x = save & quit; :q! = quit discard  
- :e <file> = open file; :r <file> = read file into buffer  
- :set number / nonumber = toggle line numbers

Undo / Redo
- u = undo (per change)  
- Ctrl-r = redo

Registers & Marks
- "a, "b = explicit register usage for yank/delete/paste  
- ma = set mark a at current cursor; `a = jump to exact position; 'a = jump to start of line of mark

Macros
- q<reg> = start recording into register; q = stop  
- @<reg> = play macro once; @@ = repeat last macro

Misc
- :!cmd = run shell command; :w !sudo tee % = save with sudo (when needed)  
- & = repeat last :s with same flags

---

## Important Properties / Invariants
- Modal behavior: keys do different things per mode — know current mode. #modal-editing  
- Operators compose with motions (operator + motion); counts apply to both. #operators  
- Changes are atomic units for undo (u undoes last change). #undo-redo  
- Dot (.) repeats the last change exactly — powerful for repetitive edits.  
- Registers persist across operations until overwritten; unnamed register holds latest yank/delete. #registers  
- Visual modes: char/line/block change semantics (block for column edits). #visual-mode

---

## Quick Reference Table (Most-Used)
| Action | Command(s) |
|---|---|
| Enter insert | i / a / o |
| Save / Quit | :w / :q / :wq / :q! |
| Undo / Redo | u / Ctrl-r |
| Yank / Paste | y / yy / p / P |
| Delete / Change | x / dd / dw / c(w/motion) |
| Repeat last change | . |
| Search | /pattern ?pattern ; n / N |
| Substitute line/file | :s/pat/repl/flags ; :%s/... |
| Record macro | q<reg> ... q ; play: @<reg> |
| Set mark / jump | ma ; `a / 'a |

---

## Exam Quick Tips
- If unsure of mode: press Esc to return to Normal mode.  
- Use counts to scale commands (e.g., 5>> to indent 5 lines).  
- Combine dot (.) and macros to automate repetitive sequences.  
- Use :%s with g and c flags for file-wide safe replacements.  
- Use registers ("a, "b) to hold important clips; prefix with " when y/d/p.

---

Keep this sheet near your workstation — practice common combos (dw, cw, yyp, :%s) until muscle memory builds.

---

## Module 6 — Lecture 54: vi/vim Editor Cheatsheet

#hashtags: #vi #vim #editor #vi-editor #modes #navigation #editing #copy-paste #search #replace #regex #regular-expressions #backup #swapfile #undo #redo #marks #indentation #line-numbers #commands #command-line #grep #crash-recovery

---

---

## Key Definitions (one-line)
- Normal mode: Default mode for navigation and commands (press Esc to enter). #modes #normal
- Insert mode: Typing mode (enter with i, I, a, A, o, O). #insert
- Command-line mode: Run colon commands (start with `:`). #command-line
- Yank: Copy a line/selection (yy y). #yank #copy #yy
- Paste: Insert yanked/deleted text (p or P). #paste #p
- Delete: Remove text (x=char, dw=word, dd=line). #delete #dd #dw #x
- Swap file (.swp): Hidden auto-save file holding unsaved edits for crash recovery. #swapfile #.swp
- Backup file (.bak / .ba~ / custom): Explicit backup copy when set. #backup
- Mark: Save a cursor position (ma) and return with `\`a or 'a. #marks
- Regex: Pattern syntax used for searches (./^/$/*/+ etc.). #regex #regular-expressions
- Repeat last normal-mode command: `.` (dot). #repeat

---

## Formulas / Notations / Regex symbols
- .  → any single character (dot). #regex
- ^  → start of line. #regex
- $  → end of line. #regex
- *  → zero or more occurrences. #regex
- +  → one or more occurrences. #regex
- [0-9]+  → one or more digits. #regex
- [A-Za-z]+  → one or more letters (upper/lower). #regex
- \c / \C  → case-insensitive / case-sensitive in some contexts (vim search flags). #regex

---

## Key Commands & Concepts
- Modes
  - Enter insert: i, I, a, A, o, O. #i #I #a #A #o #O
  - Return to normal: Esc. #Esc
  - Command-line: `:` then command (e.g., `:w`, `:q`). #:
- File save / quit
  - Save: `:w` (#:w)
  - Quit: `:q` (#:q)
  - Save+Quit: `:wq` or `:x` (#:wq #:x)
  - Quit without saving: `:q!` (#:q!)
- Navigation (normal mode)
  - h (left), j (down), k (up), l (right). #h #j #k #l
  - gg → go to top; G → go to end. #gg #G
  - `$` → end of line, `0` → line start. #$
- Editing basics (normal mode)
  - dd → delete current line. #dd
  - Ndd → delete N lines (prefix with number). #dd
  - yy → yank (copy) line. #yy
  - p → paste after cursor (P to paste before). #p #P
  - x → delete character under cursor. #x
  - dw → delete word from cursor. #dw
  - d$ → delete from cursor to end of line/file (d followed by `$` deletes to line end; dG deletes to file end). #d$
  - r{char} → replace character under cursor with {char}. #r
  - J (capital) → join current line with next. #J
- Undo / Redo
  - u → undo last change. #u
  - Ctrl-r → redo. #Ctrl-r
- Repeating & counts
  - . → repeat last normal-mode command. #.
  - Prefix with number to repeat (e.g., 4>> to indent 4 lines). #counts
- Indentation
  - > (shift-right) and < (shift-left) in normal/visual mode; prefix N to affect N lines (`N>`). #indentation #>
- Marks
  - ma → mark current position as mark 'a'. #ma
  - `a  or 'a → jump back to mark a (backtick vs apostrophe differences: exact pos vs start of line). #`a #'a
- Search & Replace
  - Search forward: `/pattern` then n (next), N (previous). #/ #n #N
  - Replace on current line: `:s/old/new/` (#:s)
  - Replace globally in file: `:%s/old/new/g` (#:%s #g)
  - With confirmation: `:%s/old/new/gc` (ask on each). #:%s #gc
- Command-line options (when launching vi)
  - `vi +N file` → open file and place cursor at line N. #+N
  - `vi -n file` → no swap file (disable .swp). #-n
  - `vi -r file` → recover a swap file (.swp) — use `vi -r filename`. #-r
  - `vi -c "command"` → run ex command after opening (e.g., `-c "w my.bak"`). #-c
  - `vi -i` → can control creation/usage of viminfo (depends on config). #-i
- Swap & Backup behavior
  - On normal editing: vim creates .swp (hidden swap) storing unsaved changes. #.swp
  - On crash: open vim shows recovery option or use `vi -r file` to recover. #-r #recovery
  - To enable explicit backups: `:set backup` and `:set backupdir` or `:set backupext=.ba` / `:set backupcopy` (session-dependent). #backup #set
  - Example backup extension: filename.ba~ or filename.bak depending on settings. #backup
- Misc
  - `:set number` / `:set nonumber` → show/hide line numbers. #:set-number
  - `.` (dot) repeats last normal-mode edit. #.
  - Use visual mode (v, V, Ctrl-v) for block/line/char selections (not covered in transcript but useful). #visual

---

## Quick Reference Table (most-used commands)
| Action | Command (normal or command-line) | Mode |
|---|---:|---|
| Enter insert | i / I / a / A / o / O | normal → insert |
| Save | :w | command-line |
| Quit | :q / :q! / :wq | command-line |
| Move left/down/up/right | h / j / k / l | normal |
| Go to top / end | gg / G | normal |
| Delete line | dd (Ndd for N lines) | normal |
| Yank (copy) line | yy | normal |
| Paste | p / P | normal |
| Delete char | x | normal |
| Delete word | dw | normal |
| Replace char | r{c} | normal |
| Join lines | J | normal |
| Undo / Redo | u / Ctrl-r | normal |
| Repeat last | . | normal |
| Mark / jump | ma  → `a / 'a | normal |
| Search | /pattern → n / N | normal |
| Replace (current line) | :s/old/new/ | command-line |
| Replace (whole file) | :%s/old/new/g (add c for confirm) | command-line |
| Show numbers | :set number / :set nonumber | command-line |
| Recover swap | vi -r filename | shell |
| No swap mode | vi -n filename | shell |
| Open at line | vi +N filename | shell |
| Execute command on open | vi -c "cmd" filename | shell |

---

## Important Properties / Invariants
- Normal-mode commands (no colon) are required for most navigation & editing (must press Esc first). #modes
- Colon commands run in command-line mode and affect files/settings (start with `:`). #:
- Numeric prefixes apply to many commands (e.g., 3dd deletes 3 lines). #counts
- `.` repeats the last normal-mode change only (not command-line commands). #.
- Swap files exist only for unsafely-closed sessions; graceful save+quit removes the swap. #.swp
- Use `:%s/.../g` for global replace; add `c` for confirmation per match. #:%s

---

Keep this sheet near your exam materials; use the Quick Reference Table for rapid lookup. Good luck.

---

## Module 7 — Lecture 55: Vi/Vim — Auto-recovery, Backup & Version-control Cheatsheet

#keywords: #vi #vim #viminfo #swap #backup #backupext #backupdir #versioncontrol #git #vimrc #autosave

## Key Definitions
- vim: "Vi IMproved" (modern vi implementation).  
- .vimrc: per-user Vim configuration file (~/.vimrc).  
- .viminfo: file that stores persistent session info (history, marks, registers).  
- swap file (.swp): temporary file used for crash recovery (unsaved edits).  
- backup: an automatic copy of the file made when saving (preserves previous version).  
- backupext (backupextension): extension added to backup files (default: ~).  
- backupdir: directory where backup files are stored.  
- :recover / -r: commands to recover from swap files.  
- Version control: tracking file history; Vim backups provide a basic form; use Git for full VCS.

## Formulas / Notation
- Vim option syntax: set <option> or set <option>=<value>  
- Example viminfo format (option string): '100,<1000,s10,h'  
  - 100 = max saved lines; <1000 = max chars per line; s10 = save session every 10s; h = include history

## Key Concepts / Commands
- Enabling/disabling options (in command mode, press Esc then type):
  - :set backup         — enable backups (#backup)
  - :set nobackup       — disable backups
  - :set backupext=.bak — set backup extension to .bak (#backupext)
  - :set backupdir=~/.vim/backups — set centralized backup directory (#backupdir)
  - :set viminfo='100,<1000,s10,h' — configure viminfo behavior (#viminfo)
- Common actions:
  - :w                 — write/save file
  - :q / :q!           — quit / force quit
  - vim filename       — open file in vim
  - git init; git add <file>; git commit -m "msg" — external VCS workflow (#git, #versioncontrol)
- Recovery:
  - Swap files (.swp) used for crash recovery — use :recover or vim -r to restore
  - viminfo stores persistent session data (history, marks, registers) across normal exits

## Important Properties / Invariants
- Default backup suffix is tilde (~). Backup files typically named file.txt~ unless changed. (#backup)
- By default backup files are created in the same directory as the original file unless backupdir is set. (#backupdir)
- Vim automatically updates .viminfo on normal exit; abnormal exits (crash) may still leave swap files for recovery. (#viminfo, #swap)
- Setting backup preserves the previous version of the file at each save (basic versioning). (#versioncontrol)
- For robust versioning/history use an external VCS (Git) — Vim backups are not a replacement. (#git)

## Quick Reference (scannable)

Options & example .vimrc lines
- set viminfo='100,<1000,s10,h'    — configure auto-recovery/history (#viminfo)
- set backup                       — enable backup files (#backup)
- set nobackup                     — disable backup files
- set backupext=.bak               — change backup file extension (#backupext)
- set backupdir=~/.vim/backups     — store backups centrally (#backupdir)
- set swapfile                     — enable swap file creation (default) (#swap)
- set noswapfile                   — disable swap files

Commands (in Vim command mode; press Esc then :)
- :set backup
- :set nobackup
- :set backupext=.bak
- :set backupdir=~/.vim/backups
- :w    — save file
- :recover or vim -r <file> — recover from swap file

Basic Version-control workflow (recommended)
- Initialize: git init
- Stage: git add <file>
- Commit: git commit -m "meaningful message"
- Use Vim for editing, Git for history and branching (#git, #versioncontrol)

File locations / names
- ~/.vimrc     — user Vim config
- ~/.viminfo   — viminfo file (session/history)
- default backup: <filename>~ or <filename>.bak (if backupext set)
- swap files: .<filename>.swp (in file dir or swapdir if configured)

Notes (exam-friendly)
- Backups = simple local copy on save; useful for quick rollback. (#backup)  
- Swap = crash recovery; use :recover if Vim or system crashes. (#swap)  
- viminfo stores persistent history/marks across sessions; configure with set viminfo. (#viminfo)  
- Prefer Git for real version control; Vim can call external commands and works well inside a Git workflow. (#git)

End of cheatsheet.

---

## Module 7 — Lecture 56: Vi/Vim Crash Recovery Cheatsheet

#hashtags: #vi #vim #recovery #swapfile #undo #autorecovery #backup #vimrc #viminfo #commands

## Key Definitions
- Swap file: .filename.swp — temporary file created while editing to store unsaved changes. #swapfile  
- Undo history: in-memory (or persistent if configured) record of edits allowing undo/redo. #undo  
- Auto recovery: use of saved recovery info (viminfo/undo files) to restore unsaved work after a crash. #autorecovery  
- Backup file: a saved copy of the previous file version created when saving (controlled by `set backup`). #backup  
- viminfo: file that stores registers, command/history, marks, etc.; its size can be limited (KB). #viminfo  
- .vimrc: user configuration file (~/.vimrc) to enable recovery/backup settings. #vimrc

## Formulas / Notations
- Swap filename pattern: .<original_filename>.swp  
- Example viminfo size setting (transcript example): viminfo maxsize = 1000 (kilobytes)  
- Time complexity: N/A (editor actions; not algorithmic complexity)

## Key Concepts / Commands
- Recover from swap file:
  - Automatic swap creation: .document.txt.swp while editing document.txt. #swapfile
  - Recover via command: vim -r <file>  (or vim -r .<file>.swp) — attempts recovery. #commands
  - Open file normally: Vim will prompt to recover if a swap exists. #commands
- Undo / Redo:
  - Undo: u  (in normal mode). #undo
  - Redo: CTRL+R (in normal mode). #undo
  - Navigate undo history to restore desired state. #undo
- Auto recovery / persistent history:
  - Configure via ~/.vimrc; viminfo and persistent undo settings control auto-recovery. #vimrc #viminfo
  - Example limits: remember up to 1000 lines/history; max viminfo file size 1000 KB (example). #viminfo
- Backups:
  - Enable backup: :set backup  (or add to ~/.vimrc). #backup
  - Backup creates copy before writing file (helps after crash). #backup

## Important Properties / Invariants
- Swap files live in the same directory by default; they are removed on clean exit. #swapfile  
- Swap contains unsaved edits; opening a file with an existing swap will prompt recovery options. #swapfile  
- Undo history is available in-session; to persist across sessions, enable persistent undo (undofile) in config. #undo  
- viminfo controls what history/registers are saved between sessions and has size limits (KB). #viminfo  
- Backups provide the last saved version; swap provides unsaved changes. #backup #swapfile

## Quick Reference (Scannable)
- Swap filename: .<file>.swp  
- Common prompts when swap exists: options include (R)ecover, (E)dit anyway, (D)elete swap, (Q)uit. #swapfile
- Commands:
  - Open file normally: vim document.txt  #commands
  - Recover: vim -r document.txt  OR vim -r .document.txt.swp  #commands
  - Manual recover from within vim: :recover  (then :w to save recovered file)  #commands
  - Save file: :w  (write changes)  #commands
  - Enable backup (session/config): :set backup  / add to ~/.vimrc  #backup #vimrc
  - Undo: u  — Redo: CTRL+R  #undo
- Config tips (put in ~/.vimrc):
  - set backup                  " enable backup files  #backup  
  - set undofile                " enable persistent undo (recommended)  #undo  
  - set viminfo='1000,<1000     " example: remember 1000 lines/history, max viminfo size 1000 KB  #viminfo
- Recovery workflow (crash -> restore):
  1. cd to file directory.  
  2. Check for swap: ls -a | grep .<file>.swp  (swap exists => recovery possible). #swapfile  
  3. Run: vim -r <file>  OR open file in vim and choose Recover when prompted. #commands  
  4. Inspect recovered buffer, use u/CTRL+R to navigate undo history. #undo  
  5. Save recovered content: :w [newname] (optionally back up old file). #commands

Keep these handy in your exam notes: swap files (.swp), vim -r for recovery, u / CTRL+R for undo/redo, :w to save, and set backup / viminfo / undofile in ~/.vimrc to reduce future data loss.

---

## Module 7 — Lecture 57: Vi/vim: Undelete & Buffer Recovery — Cheatsheet

#keywords: #vi #vim #editor #undelete #undo #recover #registers #buffer #paste #yank #commands

## Key Definitions
- Undo (`u`): revert the last change.  
- Redo (`Ctrl-R`): reapply an undone change (vim).  
- Register: named temporary storage for deleted/yanked text (`"a`..`"z`, `"0`..`"9`).  
- Numbered registers (`"0`–`"9`): hold recent deletes/yanks in rotation.  
- Named registers (`"a`–`"z`): user-controlled storage for yanks/deletes.  
- Unnamed register (`""`): default register used by most delete/yank/paste commands.  
- Buffer: generic temporary area (in vi/vim, registers implement buffer storage for paste).

## Formulas / Syntax (quick patterns)
- Specify a register: `"x` where x ∈ {0-9, a-z}  
- Paste from register x: `"xp` (paste after cursor) or `"xP` (paste before cursor)  
- Yank (copy) into register x: `"x{yank-command}` (e.g., `"ayy` to yank a line into register a)  
- Undo: `u` (repeat `u` to undo multiple changes)  
- Redo (vim): `Ctrl-R`  
- Paste default: `p` (after), `P` (before)

## Key Commands / Concepts
- Undo last change:
  - `u` — undo last change (press repeatedly to step back through changes). #undo
  - (Lecture: `U` mentioned — historically restores whole line in original vi; behavior differs in modern vim). #U
- Paste last deleted/yanked text:
  - `p` — paste contents of unnamed/default register after cursor. #paste
  - `P` — paste before cursor. #paste
- Use registers to recover specific deleted text:
  - `"0p` or `"0P` — paste contents of register 0. #registers #numbered-registers
  - `"1p` — paste from register 1 (older deleted text). #registers
  - `"ap` — paste from named register a. #named-registers
- Yank (copy) to a named register:
  - `"xy{motion}` or `"xY` / `"x y` pattern — place selection into register x (e.g., `"ayy` to yank current line into `a`). #yank #registers
- Delete behavior and registers:
  - Deletes and yanks are stored in registers so you can paste them later. #recover

## Important Properties / Invariants
- Paste position:
  - `p` → after the cursor/selection.  
  - `P` → before the cursor/selection. #paste
- Register precedence (canonical behavior):
  - `"0` — most recent yank (only updated by yank commands). #numbered-registers
  - `"1` — most recent delete; `"2`..`"9` hold successively older deletes. #numbered-registers
  - Named registers (`"a`..`"z`) persist until overwritten by explicit use. #named-registers
  - Unnamed register receives the most recent delete/yank used by default commands. #unnamed-register
- Undo is sequential (stack-like): repeated `u` steps backward through change history. #undo

## Quick Reference (scannable)
- Undo last: `u` (#undo)
- Undo multiple: press `u` repeatedly (#undo)
- Redo (vim): `Ctrl-R` (#undo #redo)
- Paste default: `p` (after), `P` (before) (#paste)
- Paste from register: `"<register>p` or `"<register>P` (e.g., `"0p`, `"1p`, `"ap`) (#registers)
- Yank into register: `"<register>y{motion}` or `"<register>yy` (e.g., `"ayy`) (#yank #registers)
- Delete (stores into delete register): `d{motion}` — deleted text goes to numbered registers (#delete #registers)
- Inspect registers (vim): `:registers` or `:reg` — show register contents (#registers)
- Named registers are explicit; numbered rotate for deletes; `"0` reserved for last yank (#named-registers #numbered-registers)

## Examples (one-line)
- Undo last deletion: press `u`. #undo  
- Paste most recent delete (default): press `p`. #paste  
- Paste from register 0: `"0p`. #registers  
- Yank current line into register a, then paste it: `"ayy` then move cursor and `"ap`. #yank #named-registers

#tags: #vi #vim #undelete #undo #registers #buffer #paste #yank #commands

(Keep this sheet near your editor during the exam: quick commands above allow recovering deleted text and using registers to manage paste/recovery.)

---

## Module 7 — Lecture 58: VA Editor / vi: Mark (Bookmark) Command — Cheatsheet

#hashtags: #vi #VAEditor #mark #marks #bookmark #bookmarks #navigation #cursor #delmarks #backtick #apostrophe #commands

## Key Definitions
- Mark / Bookmark: a named pointer set at a specific cursor location in a file.  
- Cursor position: exact character location where the cursor sits.  
- Mark name: single lowercase letter used to identify a mark (e.g., a, b, c).

## Command Syntax (Formulas / Equations)
- Set mark: m{letter}  (e.g., ma)
- Jump to mark: '{letter}  (apostrophe + letter)
- Jump to beginning of line of mark: `{letter}  (backtick + letter)
- Delete mark(s): :delmarks {name(s)}  (e.g., :delmarks a)

## Key Algorithms / Concepts
- Setting a mark:
  - Place cursor at desired location → press m then a lowercase letter (ma sets mark 'a').  
- Navigating to a mark:
  - Use apostrophe + letter to move cursor to the mark (e.g., 'a).  
- Jumping to the marked line start:
  - Use backtick + letter to jump to the beginning of the line where the mark is set (e.g., `a).  
- Deleting marks:
  - Use :delmarks followed by the mark name(s) to remove bookmarks.

## Important Properties / Invariants
- Marks are pointers created at the current cursor position when set.
- Mark names are single lowercase letters (per transcript example).
- Marks speed up navigation between different parts of a file.
- :delmarks removes specified mark(s).

## Quick Reference (Scannable)
| Action | Command | Example |
|---|---:|---|
| Set mark at cursor | m{letter} | ma  (set mark "a") |
| Move cursor to mark | '{letter} | 'a  (go to mark "a") |
| Jump to start of marked line | `{letter} | `a  (go to line start of mark "a") |
| Delete mark | :delmarks {name} | :delmarks a |

## Example Quick Workflow
- Move to line 10 → press ma (sets mark a).  
- Move elsewhere → press `a to jump back to beginning of the marked line (or 'a per navigation need).  
- Remove mark → :delmarks a

(Concise reference based on lecture transcript.)

---

## Module 7 — Lecture 59: Standard Input Redirection (Linux) — Cheatsheet

#hashtags: #stdin #input-redirection #redirection #shell #linux #bash #pipes #cat #wc #grep #sort #automation

## Key Definitions (one-liners)
- STDIN: Standard input stream (file descriptor 0), default = keyboard. #stdin
- Input redirection ("<"): Shell operator that makes a command read its stdin from a file. #input-redirection
- Pipe ("|"): Sends stdout of left command to stdin of right command. #pipes
- Command reading stdin: A program that reads input from file descriptor 0 (keyboard by default). #shell

## Syntax / Formulas
- Basic input redirection:
  - command < input-file
- Pipe:
  - command1 | command2
- Combined:
  - command < file | command2
- File descriptor:
  - STDIN = 0 (redirects affect FD 0)

## Key Commands / Concepts (brief)
- cat
  - Displays file contents. Example: cat < input.txt or cat input.txt. #cat
- wc
  - Word/line/byte counts. Options: -w (words), -l (lines), -c (bytes/chars). Example: wc -w < input.txt (counts words). #wc
- grep
  - Search for patterns in input. Example in pipeline: grep example. #grep
- sort
  - Sort lines of text. Example: sort < input.txt. #sort
- Pipes + redirection
  - Use < to feed a file into a pipeline or use commands that output to pipe. Example: cat < input.txt | grep example | wc -l. #pipes
- Use cases
  - Automation, batch processing, pipelines, combining commands. #automation

## Important Properties / Invariants
- "<" directs file → command stdin; it does not change the file. #input-redirection
- Only affects commands that read from STDIN (FD 0). If a command does not read stdin, "<" has no effect. #stdin
- Many utilities accept filenames as arguments; using "<" is equivalent only if the program reads stdin when no filename is given. #shell
- You can chain redirection and pipes: redirection happens before piping into next command (shell sets up FDs then runs commands). #pipes
- STDIN is FD 0; stdout FD 1; stderr FD 2. (Useful when combining redirections.) #stdin

## Quick Reference (scannable)
- Syntax examples:
  - Read file into command: command < input.txt
  - Count words in file: wc -w < input.txt  → outputs number of words  #wc
  - Count lines matching pattern: cat < input.txt | grep example | wc -l  → outputs count of matching lines  #grep
  - Sort a file: sort < input.txt  → prints sorted lines  #sort
- Common wc options:
  - -w = words, -l = lines, -c = bytes/chars  #wc
- When to use "<":
  - Command expects interactive/STDIN input and you want to supply a file automatically. #input-redirection
- When "<" is meaningless:
  - Command only works with filenames passed as arguments and doesn't read stdin. #shell
- File descriptor note:
  - Redirecting stdin uses FD 0:  command 0< file  (equivalent to command < file)

Keep this sheet for quick lookup during open-book exams: look up syntax, which commands read stdin, and common one-line examples.

---

## Module 7 — Lecture 60: Standard Output Redirection & Appending — Cheatsheet

#hashtags: #stdout #standardoutput #redirection #append #pipe #piping #bash #shell #ls #grep #echo #files #logging #backup #filedescriptors #stdin #stderr

---

## Key Definitions
- STDOUT: Standard output stream (default destination = terminal). #stdout #standardoutput  
- Redirection: Changing where a command's output goes (file, another command). #redirection  
- Append: Add output to end of an existing file (do not overwrite). #append  
- Pipe: Send stdout of one command as stdin to another command (|). #pipe #piping  
- File descriptor: Integer identifier for I/O streams (1 = stdout, 2 = stderr, 0 = stdin). #filedescriptors

---

## Syntax / Formulas (quick patterns)
- Redirect stdout (replace): command > file
- Append stdout: command >> file
- Pipe stdout to another command: command1 | command2
- Explicit fd redirection: command 1> file   (same as >) ; command 2> file (stderr)
- Combine stdout+stderr to file: command &> file  (bash) or command > file 2>&1

---

## Key Algorithms / Concepts
- Output capture: Use > or >> to store command output into files (#logging, #backup).  
  - Example: ls > list.txt  — store directory listing (overwrites). #ls #files
  - Example: echo "note" >> list.txt  — append line to list.txt. #echo
- Appending vs Overwriting:  
  - > truncates/overwrites file. #redirection  
  - >> appends to existing file (creates file if missing). #append
- Piping (connect commands):  
  - command1 | command2 — passes stdout of command1 into stdin of command2. #pipe  
  - Example: ls /usr/bin | grep zip > zipfiles.txt  — filter and save results. #ls #grep
- Use cases: creating logs, backups of output, filtering output before saving. #logging #backup

---

## Important Properties / Invariants
- Default STDOUT destination = terminal; redirection changes that for the command. #stdout  
- > creates the target file if it doesn't exist; truncates if it does. #redirection  
- >> creates the target file if it doesn't exist; preserves existing content and appends. #append  
- Pipe (|) transfers only stdout by default (stderr not piped unless redirected). #pipe #stderr  
- Order matters: redirections and pipes are set up by the shell before executing commands. #bash  
- File permissions affect ability to create/overwrite files (may require sudo). #files
- Use explicit fd (1,2) when you need to separate or combine stdout/stderr. #filedescriptors

---

## Quick Reference (scannable)
- Overwrite file: cmd > file
- Append to file: cmd >> file
- Pipe to filter: cmd1 | cmd2
- Save filtered output: cmd1 | cmd2 > out.txt
- Append filtered output: cmd1 | cmd2 >> out.txt
- Redirect stderr only: cmd 2> errors.log
- Redirect both to same file: cmd > all.log 2>&1   OR   cmd &> all.log (bash)
- Check contents: cat file.txt
- Example workflows:
  - Snapshot directory: ls > list.txt        (#backup)
  - Add a log line: echo "update" >> list.txt (#logging)
  - Filter & save: ls /usr/bin | grep zip > zipfiles.txt (#ls #grep)

---

Keep this sheet handy during open-book exams for quick lookup of redirection/appending patterns and examples.

---

## Module 7 — Lecture 61: Standard Error Redirection (Shell/Bash)

#keywords: #stderr #stdout #redirection #bash #shell #pipes #filedescriptors #2> #2>&1 #&> #>/dev/null #append #grep

## Key Definitions
- stdin (fd 0): standard input stream.  
- stdout (fd 1): standard output stream (normal program output).  
- stderr (fd 2): standard error stream (error/diagnostic messages).  
- redirection: send a file descriptor to a file or another descriptor (e.g., 2>error.log).  
- pipe (|): sends stdout of left command to stdin of right command (stderr unaffected unless redirected).

## Notation / File descriptors
- 0 = stdin, 1 = stdout, 2 = stderr  
- > : redirect (truncate) stdout (same as 1>)  
- >> : append stdout (same as 1>>)  
- 2> / 2>> : redirect/append stderr  
- 2>&1 : duplicate fd 2 to point where fd 1 currently points  
- &> / &>> (bash): redirect both stdout+stderr (truncate/append)

## Common Commands / Examples
- Redirect stderr to a file:
  - command 2> error.log
  - e.g., ls nonexistingdir 2> error.log
- Redirect stdout and stderr to separate files:
  - command > out.txt 2> error.log
  - e.g., ls /usr/bin > file.txt 2> error.log
- Combine stdout and stderr into one file:
  - command > output.log 2>&1
  - bash shorthand: command &> output.log
- Pipe combined stdout+stderr to another command:
  - command 2>&1 | grep pattern
  - e.g., ls nonexist 2>&1 | grep bin
- Discard output:
  - stdout: command > /dev/null
  - stderr: command 2> /dev/null
  - both: command &> /dev/null
- Append instead of overwrite:
  - stderr append: command 2>> error.log
  - both append (bash): command &>> output.log
  - combined append without &>>: command >> out.log 2>&1

## Important Properties / Invariants
- Default destination for stdout/stderr: terminal (tty).  
- Pipes only carry stdout by default; redirect stderr to pipe explicitly (2>&1 | ...).  
- Order matters: 
  - Correct to combine both to file: command > out 2>&1 (redirect stdout to file, then make stderr go to same place).
  - Wrong order example: command 2>&1 > out — this makes stderr point to the original stdout (usually terminal), then redirects stdout to file, leaving stderr going to terminal.
- & notation (2>&1) duplicates file descriptors, not strings — it follows current target of fd 1 at time of duplication.
- > truncates file; >> appends.

## Quick Reference Table
| Action | Syntax | Notes |
|---|---:|---|
| Redirect stdout (truncate) | command > out.txt | same as 1>out.txt |
| Append stdout | command >> out.txt | 1>>out.txt |
| Redirect stderr (truncate) | command 2> err.log | |
| Append stderr | command 2>> err.log | |
| Redirect both (bash) | command &> all.log | bash shorthand |
| Redirect both (portable) | command > all.log 2>&1 | portable POSIX form |
| Pipe stderr+stdout | command 2>&1 \| other | sends both into pipe |
| Discard stderr | command 2> /dev/null | |
| Discard both | command &> /dev/null | |

## Quick Patterns / Cheats
- Capture only errors: cmd 2>errors.txt
- Capture only normal output: cmd >out.txt
- Capture both: cmd >all.txt 2>&1
- Send errors to stdout (so they flow into a pipe): cmd 2>&1 | grep ...
- Keep stdout to terminal, send errors to file: cmd 2>err.log
- Keep errors to terminal, send stdout to file: cmd >out.txt
- Append instead of overwrite: replace > with >>

Keep this sheet near your exam for fast lookup of syntax and common pitfalls (especially the order rule for 2>&1).

---

## Module 7 — Lecture 62: /dev/null (Linux) — Quick Cheatsheet

#Keywords: #devnull #/dev/null #stdout #stderr #stdin #redirection #bash #shell #scripting #background #IO #quiet

---

## Key Definitions
- /dev/null: special character device that discards all data written to it and returns EOF on read. #devnull
- stdout (1): standard output file descriptor. #stdout
- stderr (2): standard error file descriptor. #stderr
- stdin (0): standard input file descriptor. #stdin
- Redirection: shell operators that change where fd 0/1/2 point (>, 2>, &>, 2>&1). #redirection
- Quiet/silent mode: executing a command with its output/error sent to /dev/null. #quiet

---

## Formulas / Syntax (common patterns)
- Redirect stdout only:
  - command > /dev/null
- Redirect stderr only:
  - command 2> /dev/null
- Redirect both stdout and stderr (POSIX-safe):
  - command > /dev/null 2>&1
  - (order matters: 2>&1 must come after stdout redirection)
- Bash shorthand (non-POSIX):
  - command &> /dev/null
- Run quietly in background:
  - command > /dev/null 2>&1 &
- Read from /dev/null:
  - returns EOF immediately (no output)

---

## Key Concepts / Usage
- Suppress unwanted output in scripts and CLI: send output to /dev/null. #scripting
- Separate stdout vs. stderr control: use > vs. 2>. #stdout #stderr
- Merge streams: use 2>&1 to point stderr to where stdout currently points. #merge
- Bash-specific &> is shorthand for merging both streams. #bash
- Running background jobs: redirect outputs to avoid terminal clutter. #background
- Common examples:
  - echo "msg" > /dev/null            (discard stdout)
  - ls nonexist 2> /dev/null         (discard errors only)
  - make > /dev/null 2>&1            (run make quietly)

---

## Important Properties / Invariants
- Writes to /dev/null are discarded (no storage). #discard
- Reads from /dev/null immediately give EOF. #EOF
- /dev/null is a device file (character device), available system-wide. #linux
- 2>&1 semantics: duplicates fd 2 to the current target of fd 1; placement matters. #fd
- &> is convenient but not portable to all shells (POSIX sh vs bash). #portability

---

## Quick Reference (scannable)

| Command syntax                      | Effect                                  | Portable? |
|-------------------------------------|-----------------------------------------|-----------|
| command > /dev/null                 | Discard stdout only                      | Yes       |
| command 2> /dev/null                | Discard stderr only                      | Yes       |
| command > /dev/null 2>&1            | Discard stdout and stderr (portable)     | Yes       |
| command &> /dev/null                | Discard stdout and stderr (bash only)    | No (bash) |
| command > /dev/null 2>&1 &          | Quietly run command in background        | Yes       |
| cat /dev/null                       | Immediately EOF (no data)                | Yes       |

Tips:
- Always put 2>&1 after the stdout redirection: wrong order (2>&1 > /dev/null) will not redirect stderr to the file.
- Use 2>/dev/null when you only want to hide error messages but still see normal output.
- Use &>/dev/null for brevity in bash scripts, but prefer > /dev/null 2>&1 for POSIX compatibility.

---

#Tags: #devnull #/dev/null #stdout #stderr #stdin #redirection #bash #shell #scripting #background #ls #rm #echo #make

---

## Module 7 — Lecture 63: Sort (Linux sort filter) — Cheatsheet

#hashtags: #sort #Linux #command-line #sorting #text-processing #options #r_option #n_option #k_option #u_option #f_option #o_option #case-insensitive #numeric-sort #field-sort #remove-duplicates

## Quick Syntax
- Basic: sort [options] [file...]
- Pipe: some-command | sort [options]
- Write to file: sort [options] input.txt
- Using -o: sort [options] input.txt -o sorted.txt
- Equivalent redirection: sort input.txt > sorted.txt

## Key Definitions (one-line)
- sort: command that rearranges lines of text in a file or stream.
- ascending order: default lexical order from smallest to largest.
- descending order: reverse of ascending (use -r).
- lexical (character) sort: compares characters (ASCII/locale).
- numeric sort: compares numeric values (use -n).
- key/field: a specified column/field within a line used as the sort key (use -k).
- case-sensitive: uppercase/lowercase considered different.
- case-insensitive: case ignored when comparing (use -f).
- duplicate line: identical entire lines; can be removed with -u.
- output file (-o): store sorted result into a file instead of stdout.

## Options (quick reference)
- -r : reverse sort order (descending) — #r_option #reverse
- -n : numeric sort (compare numbers, not strings) — #n_option #numeric-sort
- -k POS : sort by key/field POS (e.g., -k2 for second field) — #k_option #field-sort
- -u : unique — remove duplicate lines in output — #u_option #remove-duplicates
- -f : fold lower to upper — case-insensitive sort — #f_option #case-insensitive
- -o FILE : write result to FILE (like redirection) — #o_option #output
- (note) default field separator: whitespace (use -t to set a different delimiter)

## Examples (compact)
- sort file.txt
- sort -r file.txt
- sort -n numbers.txt
- sort -k2 data.txt              (sort by 2nd field)
- sort -t, -k3 file.csv         (specify delimiter , and sort by 3rd field)
- sort -f names.txt             (case-insensitive)
- sort -u duplicates.txt        (remove duplicate lines)
- sort input.txt -o sorted.txt

## Important Properties / Invariants
- Default sort is lexical/character-based (not numeric).
- -n changes comparison to numeric; without -n "10" < "2" (character order).
- -k causes the entire line to move with its key — lines remain intact.
- -u removes duplicate lines from the final sorted output.
- -f treats 'A' and 'a' as equal for sorting purposes.
- Options can be combined (e.g., sort -n -r -k2 file).

## Quick Reference Table

| Option | Meaning | Short example |
|--------|---------|----------------|
| (none) | Lexical ascending | sort file.txt |
| -r | Reverse (descending) | sort -r file.txt |
| -n | Numeric sort | sort -n nums.txt |
| -k pos | Sort by field/key pos | sort -k2 data.txt |
| -f | Case-insensitive | sort -f names.txt |
| -u | Remove duplicate lines | sort -u list.txt |
| -o FILE | Write output to FILE | sort input.txt -o out.txt |

## Common Patterns
- Sort and save: sort input.txt -o sorted.txt
- Sort numerically by 2nd field: sort -t ' ' -k2,2 -n file
- Remove duplicates after sorting: sort file | uniq  (or sort -u file)
- Pipeline usage: cmd | sort -k3 -n | head -n 10

## Tips (exam quick-facts)
- If numbers are treated oddly, add -n.
- If different cases mix order, use -f.
- To sort by a specific column, use -k and possibly -t for delimiter.
- To persist output use -o or shell redirection (>).
- Use combinations: sort -k2 -n -r -u (sort by field 2, numeric, reverse, unique).

End of cheatsheet.

---

## Module 7 — Lecture 64: Linux head — Quick Cheatsheet

#keywords: #head #linux #command #text-processing #filter #pipe #stdin #stdout #cat #glob #log #lines #bytes #options

## Key Definitions
- head: display the first part of files or stdin (default: first 10 lines). #head
- stdin / stdout: standard input / output streams. #stdin #stdout
- pipe (|): send stdout of one command as stdin to another. #pipe
- glob: wildcard filename expansion (e.g., *.log). #glob

## Syntax & Options (quick)
- Basic: head [OPTIONS] [FILE...]
- When no FILE given → reads from stdin (use with pipe). #stdin
- Options:
  - -n N, --lines=N : show first N lines (default N = 10). #lines #-n
  - -c K, --bytes=K : show first K bytes. #bytes #-c

## Key Algorithms / Concepts
- Preview file start: head file.txt (shows first 10 lines). #preview
- Specific lines: head -n 5 file.txt (first 5 lines). #-n
- Specific bytes: head -c 20 file.txt (first 20 bytes). #-c
- From pipeline: cat data.txt | head (head reads piped input). #pipe #cat
- Multiple files / globbing: head *.log → prints head of each file in turn, usually with filename headers between outputs. #glob #log

## Important Properties / Invariants
- Default output = first 10 lines if neither -n nor -c supplied. #default10
- -n and -c are mutually exclusive behaviors (choose lines or bytes). #mutual
- When reading multiple files, head outputs each file’s beginning sequentially (identifies files). #multifile
- head does not load entire file into memory — good for large files/logs. #scalable

## Quick Reference (scannable)
- Default: head file.txt → first 10 lines. #default10
- First N lines: head -n N file.txt or head --lines=N #-n
- First K bytes: head -c K file.txt or head --bytes=K #-c
- From pipe: somecmd | head → first 10 lines of somecmd output. #pipe
- Multiple files: head file1 file2 or head *.log → shows head for each file. #glob
- Use to: preview large files, inspect log headers, check file format/structure. #log #preview

## Examples
- head myfile.txt                → first 10 lines
- head -n 5 myfile.txt           → first 5 lines
- head -c 20 myfile.txt          → first 20 bytes
- cat data.txt | head -n 3       → first 3 lines of piped content
- head *.log                     → head of every .log file in directory

## Quick Tips
- Combine with other filters (grep, awk, tail) for targeted inspection. #grep #awk #tail
- Use head before processing large files to confirm format/headers. #safety
- Remember difference: head = start-of-file, tail = end-of-file. #tail

(Concise reference for open-book exams — quick lookup of syntax, options, and common usage.)

---

## Module 7 — Lecture 65: Linux tail command — Cheatsheet

#keywords: #tail #linux #logfiles #monitoring #streaming #commandline #grep #textutils

## Key Definitions
- tail: displays the last part (end) of a file or stream.  
- follow (-f): keep reading and display new data appended to a file in real time.  
- line count (-n): show the last N lines of input.  
- byte count (-c): show the last N bytes of input.  
- log file: frequently-updated file where recent events/errors are appended to the end.

## Syntax / Short formulas
- Basic: tail [options] [file]  
- Common options: -n N (lines), -c N (bytes), -f (follow)  
- Default behavior: tail file → last 10 lines

## Key Commands & Examples
- tail file.txt
  - Output: last 10 lines (default)
- tail -n 2 file.txt
  - Output: last 2 lines
- tail -c 20 file.txt
  - Output: last 20 bytes
- tail -f logfile.log
  - Output: show end of file and continuously show new lines as they are added
- Combining with grep (filter + recent matches)
  - grep "error" logfile.log | tail -n 10
  - Output: last 10 lines that match "error"

## Key Concepts / Use Cases
- #monitoring: Observe real-time updates to logs (use -f).  
- #troubleshooting: Quickly view recent errors or events at file end.  
- #efficiency: View end of large files without reading entire file.  
- #composition: Pipe/chain with other commands (grep, awk, sed) for focused output.

## Important Properties / Invariants
- Default last-lines = 10.  
- -n and -c accept numeric arguments specifying what to return from file end.  
- -f causes tail to continue running and print appended data as it arrives.  
- tail is useful when recent updates are appended to file ends (typical for logs).

## Quick Reference (scannable)
- tail file                → last 10 lines  
- tail -n N file           → last N lines  
- tail -c N file           → last N bytes  
- tail -f file             → follow (show appended lines in real time)  
- grep "pattern" file | tail -n N  → last N matching lines  
- Use tail to: monitor logs, inspect recent entries, stream appended output

#tags: #tail #linux #logfiles #monitoring #grep #follow #lines #bytes #commandline

---

## Module 7 — Lecture 66: grep Cheatsheet — Search & Filter Text in Linux

#grep #linux #regex #regular_expressions #search #filter #log_analysis #text_processing #recursive #case_insensitive #invert_match #count #line_numbers #list_files #stdin

---

---

## Key Definitions
- grep: command-line tool to locate lines matching a pattern in files or input streams.  
- Pattern (PATTERN): the text or regular expression grep matches.  
- Regular expressions (#regex): patterns describing sets of strings; grep supports them.  
- Input stream (#stdin): data piped into grep (e.g., cat file | grep PATTERN).  
- Match: a line that contains text conforming to PATTERN.

---

## Syntax / Quick Pattern
- Basic syntax: grep [options] PATTERN [FILE...]
- Use quoted PATTERN to protect shell meta-characters: grep 'pattern' file

---

## Options Summary (quick reference)
| Option | Effect |
|---|---|
| -i | Case-insensitive search (#case_insensitive) |
| -r | Recursive search in directories (#recursive) |
| -l | List file names that contain the pattern (#list_files) |
| -v | Invert match — show non-matching lines (#invert_match) |
| -c | Count matching lines per file (#count) |
| -n | Show line numbers with matching lines (#line_numbers) |

(Flags may be combined, e.g., grep -rin 'TODO' /path)

---

## Key Algorithms / Concepts
- Pattern matching using regular expressions (#regex)
- Line-based search: grep processes input line-by-line and prints matching lines
- Recursive directory traversal: grep -r descends into subdirectories and searches files
- Filtering in pipelines: grep reads from stdin if FILE omitted (e.g., ps aux | grep ssh) (#stdin)
- Inverted selection: exclude lines matching a pattern with -v

---

## Important Properties / Invariants
- grep prints whole matching lines (unless combined with other tools/options).  
- -i affects only case-sensitivity, not pattern semantics.  
- -r searches files under a directory path (including subdirectories).  
- -l lists only file names (no matching lines) when pattern found.  
- -c reports counts, not content; when multiple files are searched, output shows counts per file.  
- -v returns lines that do NOT match the pattern (useful to exclude entries).  
- grep supports standard regex syntax (basic/extended depending on flags like -E, not covered here).

---

## Quick Reference / Examples
- Search for literal "error" in logfile:
  - grep 'error' logfile.txt
- Case-insensitive search for "warning":
  - grep -i 'warning' logfile.txt
- Recursive search for "config" in directory:
  - grep -r 'config' /path/to/dir
- List file names containing "password":
  - grep -l 'password' /path/to/dir/*
- Count matches of "failed" in file:
  - grep -c 'failed' logfile.txt
- Show matching lines with line numbers:
  - grep -n 'pattern' file.txt
- Invert match (show lines without "success"):
  - grep -v 'success' log.txt
- Combined flags example (recursive, case-insensitive, show line numbers):
  - grep -rin 'TODO' /project

---

## Quick Patterns / Tips
- Use quotes around PATTERN to avoid shell expansion.  
- Omit FILE to read from stdin (useful in pipes).  
- Combine with other tools (sed/awk/xargs) for extraction or batch operations.  
- For extended regex, use grep -E (not detailed in transcript).  

---

Keep this sheet handy for log analysis, filtering outputs, and quick text searches.

---

## Module 7 — Lecture 67: Linux Pipe Command — Cheatsheet

#hashtags: #pipe #linux #shell #bash #filters #stdin #stdout #stderr #pipeline #grep #sort #uniq #wc #awk #xargs #ps #kill #ls #cat #tee #cut #head #tail #pipefail

## Key Definitions
- Pipe (|): connect stdout of one command to stdin of the next. #pipe
- Pipeline: sequence of commands joined by |. #pipeline
- Filter: a command that reads stdin, writes transformed output to stdout (e.g., #grep, #sort). #filters
- stdout (fd 1): standard output stream. #stdout
- stdin (fd 0): standard input stream. #stdin
- stderr (fd 2): standard error stream (not piped by default). #stderr
- Pipe buffer: kernel buffer used to transfer data between processes (no temp files). #pipe
- Exit status of pipeline: by default the last command’s exit code; use `set -o pipefail` to detect failures earlier. #pipefail

## Syntax / Formulas / Notation
- Basic pipeline: command1 | command2 | command3
- Redirect stderr into pipe:
  - Bash shorthand: command |& cmd2   (equivalent to 2>&1 |)
  - Explicit: command 2>&1 | cmd2
- Ensure pipeline fails if any command fails:
  - set -o pipefail
- Common pattern: producer | filters... | consumer

## Key Commands / Concepts (quick bullet points)
- #ls | #grep
  - ls -l | grep 'pattern' → filter listing lines matching pattern
- #cat | #grep | #wc
  - cat file | grep 'pattern' | wc -l → count matching lines (wc -l)
- #sort | #uniq
  - cat file | sort | uniq → sorted unique lines
  - uniq requires sorted input for full de-duplication; use `uniq -c` to count
- #ps | #grep | #awk | #xargs
  - ps aux | grep firefox | awk '{print $2}' | xargs kill -9  
    → find PIDs for processes with "firefox" and force-kill
- #awk
  - awk '{print $n}' → extract nth whitespace-separated column
- #xargs
  - xargs -r -n1 command → run command with arguments from stdin; -r avoid running if no input
- #tee
  - cmd | tee file | nextcmd → split stream: write to file and pass through
- Common text utilities: #cut, #head, #tail, #tr, #sed

## Important Properties / Invariants
- Each pipeline stage runs as its own process; stages execute concurrently. #pipeline
- Order of lines is preserved through standard text filters (unless a filter reorders them, e.g., #sort). #filters
- No intermediate temp files (efficient for large streams); uses kernel pipe buffer. #pipe
- stderr is not piped by default — must redirect if you want it included. #stderr
- Pipeline exit code behavior:
  - Default: exit code = last command’s exit code
  - With `set -o pipefail`: non-zero if any stage fails → better for scripts. #pipefail
- Quoting matters: protect patterns and whitespace when piping to commands that interpret them. #shell

## Quick Reference (scannable)
- Basic:
  - command1 | command2
- Common flags:
  - grep: -i (ignore-case), -v (invert), -E (extended regex), -F (fixed strings)
  - sort: -n (numeric), -r (reverse)
  - uniq: -c (count), -d (duplicates), -u (unique)
  - wc: -l (lines), -w (words), -c (bytes)
  - awk: '{print $1}' (column 1)
  - xargs: -n1 (one arg per command), -r (no run if empty), -I{} (replace token)
  - ps: ps aux or ps -ef (full listings)
  - kill: -9 (SIGKILL), prefer graceful term first (kill PID)
- Examples:
  - List files with "file" in name: ls -l | grep 'file'
  - Count pattern matches: grep 'pattern' file | wc -l
  - Unique sorted list: sort file | uniq
  - Kill processes by name: ps aux | grep name | awk '{print $2}' | xargs kill
  - Pipe stderr: cmd 2>&1 | grep 'error'  OR  cmd |& grep 'error'
  - Split output to file and next cmd: cmd | tee out.txt | othercmd
- Performance notes:
  - Streaming via pipes is memory-efficient for large data (no temp files).
  - Excessive use of external commands may cost CPU; combine work in single tool (e.g., awk) when possible.

Keep this cheatsheet next to your terminal: focus on patterns (producer | filters | consumer) and common flags for quick composition.

---

## Module 7 — Lecture 68: Linux tee — Cheatsheet

#hashtags: #tee #pipe #stdin #stdout #redirection #append #ignore-interrupt #logfile #ls #echo #file #shell

---

## Key Definitions
- tee: Reads from standard input and writes to standard output and one or more files simultaneously. #tee #stdin #stdout
- pipe (|): Connects stdout of one command to stdin of another. #pipe
- redirection (>): Sends stdout to a file (overwrites). (>>) Appends to file. #redirection #file
- append (-a): Option to add output to end of file(s) instead of overwriting. #append
- ignore-interrupt (-i): Option to ignore interrupt (SIGINT) while writing. #ignore-interrupt

---

## Syntax / Formulas
- Basic: other-command | tee [options] file1 [file2 ...]
- Common options:
  - -a : append to files (not overwrite)
  - -i : ignore interrupt signals (SIGINT)

---

## Key Commands / Examples
- Capture ls output to file and still print:
  - ls -l | tee list.txt  #ls #tee
- Append a line to a log while printing:
  - echo "message" | tee -a log.txt  #echo #append #logfile
- Duplicate output to multiple files:
  - ls | tee file1.txt file2.txt  #multiple-files
- Overwrite default behavior:
  - tee file.txt  (overwrites file.txt) #redirection

---

## Important Properties / Invariants
- Writes to stdout and to all listed files (simultaneous duplication). #stdout
- By default, tee overwrites files; use -a to append. #append
- Accepts multiple file arguments — duplicates output to each file. #multiple-files
- Useful for creating logs while preserving interactive terminal output. #logfile
- tee processes data from stdin (so always used in a pipeline or with input redirection). #stdin #pipe

---

## Quick Reference (scannable)
- Syntax: cmd | tee [ -a | -i ] file1 [file2 ...]
- Overwrite file: tee file.txt  → file.txt replaced
- Append file: tee -a file.txt  → new content appended
- Ignore Ctrl+C while writing: tee -i file.txt
- Multiple files: tee f1 f2 f3  → same output saved to all
- Use when you want both terminal output and saved file (vs > which hides terminal). #redirection

---

## One-line Reminders
- Use tee to "tee-off" output to terminal + files. #tee
- Use -a to preserve existing file contents. #append
- Use -i to avoid interruption while logging. #ignore-interrupt

---

End of cheatsheet — quick search tags at top for fast lookup.

---

## Module 7 — Lecture 69: VI/Vim Recovery & Linux IO Redirection — Cheatsheet

#hashtags: #vi #vim #editor #recovery #buffers #swapfile #undo #io #io-redirection #stdin #stdout #stderr #pipes #filters #tee #heredoc #redirection #process-substitution

---

## Key Definitions
- vi / vim: modal text editor commonly used on Unix/Linux.  
- Swap file (.swp): temporary file Vim creates to recover crashes/unsaved changes.  
- Buffer: in-memory file copy opened in the editor (multiple buffers possible).  
- Undo/Redo: u = undo, Ctrl‑R = redo; time-travel with :earlier / :later.  
- stdin / stdout / stderr: standard input (fd 0), standard output (fd 1), standard error (fd 2).  
- IO redirection: shell operators that reroute stdin/stdout/stderr to/from files or other commands.  
- Pipe: operator (|) that connects stdout of one command to stdin of another.  
- Filter: command that transforms a data stream (e.g., grep, sed, awk, sort).

---

## Formulas / Notation
- File descriptors: stdin=0, stdout=1, stderr=2  
- Redirect syntax summary:
  - cmd > file  (stdout → file, overwrite)
  - cmd >> file (stdout → file, append)
  - cmd < file  (stdin ← file)
  - cmd 2> file (stderr → file)
  - cmd > file 2>&1 (stdout and stderr → file)  
  - cmd &> file (bash shorthand for both stdout+stderr → file)
  - cmd1 | cmd2 (stdout of cmd1 → stdin of cmd2)
  - <<EOF ... EOF (here‑document: multi-line stdin)
  - <(cmd) or >(cmd) (process substitution)

---

## Key Commands & Concepts — VI / VIM Recovery (#vi #vim #recovery #buffers)
- Swap / crash recovery:
  - When opening a file with existing .swp: follow prompts or use `vim -r filename` to recover.
  - Find swap files: `ls -a | grep '\.swp'` or check /var/tmp, /tmp.
  - Recover manually: `vim -r path/to/.swp` then `:w filename` to save.
- Undo / Redo:
  - `u` = undo, `Ctrl-R` = redo
  - `:earlier 10m` / `:later 5m` = move through time-based undo history
- Buffer navigation:
  - `:ls` or `:buffers` = list buffers
  - `:bN` or `:buffer N` = switch to buffer N
  - `:bn` / `:bp` = next / previous buffer
  - `:bd N` = delete buffer N
- Restore previous version:
  - Use version control (recommended) or use `:earlier` / swap recovery; save with `:w`.
- Quick-safe editing:
  - Abort changes: `:q!` ; Save & exit: `:wq` ; Open another file: `:e filename`
- Practical tips:
  - Save often. If crash, check `.swp` and `vim -r`.
  - Use `:set backup` and `:set undofile` for persistent backups/undo.

---

## IO Redirection Operators & Examples (#io #io-redirection #pipes #filters #tee #heredoc)
- Basic examples:
  - ls > out.txt            # overwrite stdout to out.txt
  - echo "x" >> log.txt    # append to file
  - sort < unsorted.txt | uniq -c | sort -nr > freq.txt
  - grep "pattern" file | wc -l  # filter then count
- stderr handling:
  - cmd 2> err.log          # send stderr to file
  - cmd > out.log 2>&1      # combine stdout+stderr to out.log
  - cmd &> all.log          # bash shorthand: both stdout+stderr
- Pipes & filters:
  - cmd1 | cmd2 | cmd3      # sequential filters; each receives stdout of previous
  - Useful filters: #grep #sed #awk #sort #uniq #head #tail #cut #tr #wc
- tee:
  - cmd | tee file          # write stdout to terminal and file
  - cmd | tee -a file       # append to file
- Here-documents:
  - cat <<EOF > file
    multi-line
    EOF
- Process substitution:
  - diff <(cmd1) <(cmd2)    # compare outputs without temp files

---

## Important Properties / Invariants
- Order matters: redirections are evaluated left-to-right; `cmd >f 2>&1` differs from `cmd 2>&1 >f`.
- Pipe passes stdout only (use 2>&1 if you need stderr).
- Overwrite vs Append: > overwrites; >> appends.
- Filters operate on streams (stdin/stdout) — they do not alter files unless redirected.
- Vim swap files indicate unclean exit; do not blindly delete .swp — recover first when possible.
- Persistent undo requires `:set undofile` (stores undo history on disk).

---

## Quick Reference (Scannable)
- Vim recovery:
  - Open with swap message → follow prompt or `vim -r file`
  - List buffers: `:ls` | switch: `:b N` | close: `:bd N`
  - Undo/Redo: `u` / `Ctrl-R`; timeline: `:earlier` / `:later`
- Common redirections:
  - stdout → file: >
  - stdout append: >>
  - stdin ← file: <
  - stderr → file: 2>
  - combine errs: > file 2>&1  OR &> file
  - pipe: |
  - tee to file + stdout: | tee file
- Examples:
  - Save command output: ps aux > procs.txt
  - Capture errors: gcc prog.c 2> compile.err
  - Save output+errors: ./run > out.log 2>&1
  - Use filters: cat file | grep foo | sort | uniq -c > counts.txt
  - Here-doc: sqlplus user <<EOF ... EOF
- Useful filters (one-word lookup):
  - #grep #sed #awk #sort #uniq #head #tail #cut #tr #wc #tee

---

Keep this sheet for quick lookup during the exam. Practice the exact Vim commands and shell examples to internalize behavior (especially fd ordering and swap recovery steps).

---

## Module 7 — Lecture 70: Week 7 Cheatsheet — vi editor recovery, Linux I/O redirection & common text utilities

#Keywords
#vi #vim #swapfile #backup #registers #undo #redirection #stdin #stdout #stderr #devnull #wc #sort #head #tail #grep #pipe #tee #linux #commands

---

## Key Definitions (one-liners)
- Swap file (.swp): auto-created temp file by vi when editing unsaved content — used for recovery after a crash.  
- Backup file (.bak): explicit copy of a file created in a vi session when backup is enabled.  
- Register: small named storage in vi (names 0–9, A–Z) holding deleted/yanked text.  
- Undo/Redo: revert or reapply edits (undo key used in vi).  
- stdin (fd 0): standard input.  
- stdout (fd 1): standard output.  
- stderr (fd 2): standard error.  
- /dev/null: "black hole" — discard output (no storage).  
- Pipe (|): connect stdout of one command to stdin of another.  
- tee: duplicate output to screen and one or more files.

---

## Formulas / Notation / File descriptors
- stdin = 0, stdout = 1, stderr = 2  
- Redirect stdout: command > file  
- Append stdout: command >> file  
- Redirect stderr: command 2> file  
- Redirect both stdout+stderr to same file: command &> file  (or command >file 2>&1)  
- Send output to black hole: command > /dev/null  (or 2> /dev/null for errors)  
- Pipe: cmd1 | cmd2  
- tee: cmd | tee file1 file2   (append: tee -a)

---

## Key Commands / Concepts (short bullets)
- vi swap/recovery
  - Swap file appears as filename.swp when you re-open an edited-but-unsaved file.
  - Recover: vi -r filename  (prompts to recover from the .swp).
  - If you press Enter at the prompt without recovering, unsaved edits are lost.
- vi backups (per session)
  - Enable backup for session: in command mode type: :set backup
  - Set extension: :set backupextension=.bak
  - Saved backup file appears as filename.bak after write/quit (wq).
- Registers (vi/vim)
  - Numbered registers: 0–9 (transcript: used to store deleted/yanked text).
  - Lettered registers: A–Z (also usable).
  - Deleted/yanked contents can be pasted from a register (examples in lecture: 1p, 2p to paste recent deletions).
  - Inspect registers: :registers (or :reg) shows contents.
- Undo / Redo
  - Use undo key (lecture uses U / undo) to revert recent edits; repeat to step back through changes.
- Redirection & appending
  - Overwrite output: cmd > file  (creates file if missing)
  - Append output: cmd >> file
  - Example: ls > o.txt  (save listing), ls >> o.txt (append another listing)
- Error redirection & combining
  - Redirect stderr: cmd 2> err.txt
  - Send stderr to same destination as stdout: cmd >log.txt 2>&1  (or cmd &>log.txt)
  - Use /dev/null to discard output or errors: cmd > /dev/null  (stdout discarded), cmd 2> /dev/null (errors discarded)
- Pipes
  - Connect commands: ls -l | grep pattern   (grep reads output of ls -l)
- tee (duplicate output)
  - Show output and write to files: cmd | tee out.txt
  - Multiple destinations possible: cmd | tee file1 file2
  - Append mode: tee -a
- wc (word count)
  - wc -w file  → number of words
  - wc -l file  → number of lines
  - wc -c file  → number of bytes/characters
- sort (line sorting)
  - sort file
  - Options:
    - -r : reverse (descending)
    - -n : numeric sort
    - -k N : sort by field/key N
    - -u : unique (remove duplicate output lines)
    - -f : case-insensitive
    - -o out.txt : write sorted output to file
- head / tail
  - head -n N file : first N lines
  - head -c N file : first N bytes
  - tail -n N file : last N lines
  - tail -c N file : last N bytes
  - tail -f file : follow file — show appended lines in real time (useful for logs)
- grep (search/filter)
  - grep pattern file(s)
  - Common options:
    - -i : case-insensitive
    - -r : recursive (search directory and subdirectories)
    - -l : print filenames containing matches (no matching lines)
    - -v : invert match (show non-matching lines)
    - -c : count matching lines
    - -n : show line numbers for matches
  - Use regex/patterns to extract structured data (e.g., emails).
- Practical examples (short)
  - Recover vi swap: vi -r na.txt
  - Create session backup: in vi: :set backup | :set backupextension=.bak | :wq
  - Redirect ls output: ls > o.txt
  - Append with ls -lt: ls -lt >> o.txt
  - Discard ping output: ping host > /dev/null
  - Compile and suppress errors: gcc prog.c 2>/dev/null && echo "compilation done"
  - Pipe + grep example: ls -l | grep fifo
  - Duplicate output to screen and file: somecmd | tee out.txt

---

## Important Properties / Invariants
- Swap file only exists when edits are unsaved and a crash/abnormal close occurs. Reopen prompts recovery.  
- Backup files are only created when backup is explicitly enabled for the session (or via config).  
- Standard descriptors: 0(stdin), 1(stdout), 2(stderr) — use these numbers when redirecting.  
- Pipes pass stdout of the left command as stdin to the right command (stderr unaffected unless redirected).  
- /dev/null discards data; use for suppressing unwanted output.  
- tail -f is for live monitoring (logs); head shows start of files.  
- grep options allow fast filtering/search across files/directories (use -r for recursion, -l to list files only).

---

## Quick Reference (scannable)
- vi recovery: vi -r filename  (.swp = swap file)  #vi #swapfile  
- Make backup in session: :set backup ; :set backupextension=.bak ; :wq  #backup  
- Registers: 0–9, A–Z — store deleted/yanked text; view with :reg  #registers  
- Undo: undo key (repeat to step back)  #undo  
- File descriptors: stdin=0 stdout=1 stderr=2  #stdin #stdout #stderr  
- Redirect stdout: >   (overwrite)  
- Append stdout: >>  (append)  
- Redirect stderr: 2>  ; combine: >file 2>&1  or &>file  
- Discard output: > /dev/null  or 2> /dev/null  #devnull  
- Pipe: cmd1 | cmd2  (stdout->stdin)  #pipe  
- tee: cmd | tee file  (show+save) ; tee -a to append  #tee  
- wc: -w words, -l lines, -c bytes  #wc  
- sort: -r -n -k <field> -u -f -o out  #sort  
- head/tail: head -n / -c ; tail -n / -c ; tail -f (follow)  #head #tail  
- grep: -i -r -l -v -c -n  — pattern/regex search  #grep

---

Keep this sheet handy for quick lookup of commands, options, redirects, and vi recovery steps during the open-book exam. If you want, I can convert this into a single-page PDF or a one-column printable format.

---

## Module 8 — Lecture 71: Shell Scripting — Cheatsheet

#hashtags: #shell #scripting #bash #sh #ksh #csh #tcsh #zsh #shebang #automation #backup #datacenter #ERP #GNUplot #bootscript #systemadmin

---

## Key Definitions
- Shell: command-line interpreter that runs user commands on Unix/Linux. #shell
- Shell script: a text file of shell commands treated as a single executable recipe. #scripting
- Shebang (hashbang): first-line marker that tells OS which interpreter to use (#!/path/to/shell). #shebang
- Interpreter: program that reads and executes script lines at runtime (not compiled). #interpreter
- Automation: using scripts to repeat, schedule, or compose system tasks without manual intervention. #automation

---

## Formulas / Syntax / Notation
- Shebang format:
  - #! /path/to/interpreter
  - Example: #!/bin/bash
- Execution model:
  - script-file -> shell-interpreter -> interpreted commands (no compile step)
- Simple repetition pattern (conceptual): run command N times (e.g., create users)
  - for user in userlist; do adduser $user; done

---

## Key Algorithms / Concepts
- Automation of repetitive tasks (backups, user creation, batch updates). #automation #backup
- Command composition: combine existing utilities into new commands/pipelines. #pipeline
- Scripts as single-entity commands: encapsulate lengthy command sequences. #encapsulation
- Use of functions in scripts to operate on datasets (cleaning, align fields). #function
- Data visualization by script-driven tools (e.g., gnuplot). #GNUplot
- Interpreted vs compiled: scripts are interpreted (easier to write/debug; no type declarations). #interpreter

---

## Common Shells (quick reference)
| Shell | Common path | Notes |
|---|---:|---|
| sh (Bourne) | /bin/sh | original Unix shell. #sh |
| bash (Bourne-Again) | /bin/bash | widely used on Linux (used in module). #bash |
| ksh (Korn) | /bin/ksh | Korn shell. #ksh |
| csh | /bin/csh | C-style shell. #csh |
| tcsh | /bin/tcsh | enhanced csh. #tcsh |
| zsh | /bin/zsh | feature-rich interactive shell. #zsh |

---

## Important Properties / Invariants
- Scripts are interpreted by the specified shell (via shebang). #shebang
- Scripts allow grouping many commands into one executable unit. #encapsulation
- Shells (traditional) have limited programming features compared to full languages:
  - limited single-command focus; only special combos otherwise. #limitations
  - limited/primitive support for strings and arrays (depends on shell). #limitations
- Easier to write and debug than many compiled programs due to no data-type declarations. #debugging
- Ideal for system admin tasks, repetitive workflows, startup/boot scripts, and batch maintenance. #systemadmin #bootscript

---

## Use Cases (scannable)
- Backup automation for high-frequency transactions (banks). #backup
- Bulk user creation and environment setup (ERP, LMS deployments). #ERP #LMS
- Server/service health monitoring, resource collection, capacity planning (data centers). #datacenter
- Boot scripts, application install/uninstall automation, batch updates. #bootscript
- Data preprocessing pipelines and plotting via external tools (gnuplot). #GNUplot

---

## Quick Reference (rules & patterns)
- When to use shell scripts:
  - repetitive OS-level tasks, orchestration of command-line utilities, simple text/file manipulation. #automation
- When NOT to rely solely on shell scripts:
  - heavy data-structure manipulation, complex string/array logic, performance-critical code (prefer higher-level language). #limitations
- Shebang must be first line to select interpreter; otherwise default interactive shell used. #shebang
- Scripts are executed by invoking interpreter or setting executable + invoking file:
  - chmod +x script.sh; ./script.sh
  - or: bash script.sh
- Create new commands by composing utilities (pipe |, redirect > >>). #pipeline
- Debugging tips:
  - run with -x for trace: bash -x script.sh
  - add set -e to exit on error (shell support permitting)

---

Keep this sheet handy during open-book exams for quick lookup of shell types, shebang usage, when to use shell scripts, and typical system-administration use cases.

---

## Module 8 — Lecture 72: Shell Script Basics — Quick Cheatsheet

#keywords: #shell #shellscript #bash #shebang #comments #linecontinuation #semicolon #exitstatus #echo #chmod #permissions #execution #stdout #scripting

## Key Definitions
- Shebang (#shebang): First-line marker starting with #! specifying the interpreter (e.g., #!/bin/bash).
- Shell script (#shellscript): A plaintext file containing shell commands and logic to be executed by a shell.
- Comment (#comments): Line beginning with # (ignored by shell; except shebang uses #!).
- Line continuation (#linecontinuation): Ending a line with backslash \ to join with next line.
- Command separator (#semicolon): Semicolon ; separates multiple commands on one line.
- Exit status (#exitstatus): Integer return code from a script/command (0 = success, non‑zero = error).
- Standard output (#stdout): Default stream for normal program output (e.g., echo prints to stdout).
- Execute permission (#permissions): File permission bit required to run file directly (set via chmod).

## Formulas / Notation
- Exit codes range: 0 = success; 1–255 = failure/error (shell uses unsigned 8-bit).
- Last command status variable: $? contains the exit status of most recently run command.
- Shebang format: #! /path/to/interpreter [optional-arg]

## Key Concepts / Commands (#bash #echo #chmod #execution)
- Shebang usage:
  - Place as first line: #!/bin/bash (or #!/usr/bin/env bash).
  - Kernel uses shebang when executing file directly (./script).
- Comments:
  - Use #: # this is a comment
  - Shebang is an exception: starts with #! and is not a regular comment.
- Line continuation:
  - Use backslash at end of line: echo "long \
    line"
- Command separator:
  - Use semicolon: cmd1; cmd2 (executes sequentially).
- Exit status:
  - Explicit exit: exit N
  - If no exit, script returns exit status of last executed command.
  - Check with: echo $?
- Printing:
  - echo "Hello World" prints to stdout.
- Execution methods:
  - Invoke interpreter explicitly: bash script.sh
  - Make executable and run directly:
    - chmod +x script.sh
    - ./script.sh
  - If run via interpreter explicitly, shebang ignored for interpreter selection.
- Permissions:
  - Add execute bit: chmod +x script.sh
  - Common mode for executables: chmod 755 file (owner rwx, group/others rx)
- Interpreter selection rules (priority):
  - If run with interpreter: interpreter chosen by command (bash script.sh).
  - If run directly (./script): kernel reads shebang to choose interpreter; if missing, default shell behavior varies.

## Important Properties / Invariants
- Shebang must be the very first line to be recognized as interpreter directive.
- Comments (starting with #) do not affect execution.
- Backslash at EOL is the only portable line-joining mechanism in shell scripts.
- Semicolon is equivalent to a newline for separating commands on same line.
- Scripts without execute bit can still run by calling an interpreter explicitly.
- Exit codes are limited to 0–255; larger values are truncated modulo 256.
- $? is updated after each command — read it immediately if needed.

## Quick Reference (scannable)
- Create script header:
  - #!/bin/bash
- Basic hello world:
  - echo "Hello World"
  - exit 0
- Run script (two ways):
  - bash script.sh
  - chmod +x script.sh
  - ./script.sh
- Make executable:
  - chmod +x script.sh
  - chmod 755 script.sh (common)
- Check last exit status:
  - echo $?
- Explicit exit:
  - exit N  # N in [0..255]
- Line continuation:
  - command arg1 arg2 \
    arg3
- Multiple commands same line:
  - cmd1; cmd2; cmd3
- Comment:
  - # comment text
- Shebang examples:
  - #!/bin/bash
  - #!/usr/bin/env bash

Keep this sheet near your exam sheet for quick lookup of syntax and execution rules. #scripting #shell #bash #shebang #chmod #exitstatus

---

## Module 8 — Lecture 73: Bash Wildcards (Globbing) Cheatsheet

#keywords: #wildcards #glob #bash #shell #filematching #star #questionmark #brackets #negation #ranges #ls #quoting #escaping #dotfiles

## Key Definitions
- Wildcard (globbing): pattern characters the shell expands to matching filenames/pathnames. #wildcards #glob
- * (star): matches zero or more characters. #star
- ? (question mark): matches exactly one character. #questionmark
- [chars] (character class): matches exactly one character listed (e.g., [aeiou]). #brackets
- [!chars] or [^chars] (negation inside brackets): matches exactly one character not listed. #negation
- Range in brackets: [a-z] matches any single character in that range. #ranges
- Quoting/escaping: prevents shell expansion (e.g., '\*' or "*" or 'pattern'). #quoting #escaping
- Globbing vs Regex: glob patterns are simpler than regular expressions. #glob

## Formulas / Pattern Equivalents
- '*'  => matches 0..n characters (glob) — roughly equivalent to regex '.*'. #star
- '?'  => matches exactly 1 character — roughly regex '.'. #questionmark
- '[abc]' => matches exactly one of 'a' or 'b' or 'c' — regex '[abc]'. #brackets
- '[a-z]' => matches one character in inclusive range a..z. #ranges
- '[!abc]' or '[^abc]' => matches one character not in set — regex '[^abc]'. #negation

## Key Concepts / Usage
- Basic usage examples:
  - ls *.html -> list files ending with ".html". #ls #star
  - ls A*.html -> files starting with 'A' and ending with ".html". #star
  - ls project.?? -> files named "project." plus exactly two-character extension. #questionmark
  - ls [aeiou]* -> files starting with a vowel (a,e,i,o,u). #brackets
  - ls [!aeiou]* -> files starting with any character except listed vowels. #negation
  - ls [0-9]* -> files starting with a digit (range). #ranges
- Patterns match filenames, not arbitrary text — used by shell commands (ls, rm, cp, mv, etc.). #filematching
- Use quoting/escaping to treat wildcard characters literally (prevent expansion). #quoting #escaping

## Important Properties / Invariants
- '*' can match an empty string (zero characters). #star
- '?' always matches exactly one character. #questionmark
- Bracket expressions match exactly one character from the set or range. #brackets #ranges
- Negation ([!...] or [^...]) inside brackets matches any single character not in the set. #negation
- Globbing happens before the command runs (shell expands patterns to filenames). #glob
- If a pattern matches no files, behavior depends on shell options:
  - Bash default: pattern remains unchanged (or can be removed with nullglob). (Note: exam check: shell settings affect behavior.) #bash
- Leading dotfiles: patterns normally do NOT match filenames starting with '.' unless explicitly included (e.g., .*) or shell option shopt -s dotglob is set. #dotfiles

## Quick Reference (scannable)
- Pattern -> Meaning -> Example
  - * -> zero or more chars -> *.txt (all .txt files) #star
  - ? -> exactly one char -> file?.txt (file1.txt, fileA.txt) #questionmark
  - [abc] -> one of a,b,c -> [aeiou]* (starts with a vowel) #brackets
  - [!abc] -> not a,b,c -> [!aeiou]* (starts with non-vowel) #negation
  - [a-z] -> any lowercase letter a..z -> [A-Za-z]* (starts with any letter) #ranges
- Tips / Pitfalls
  - To list files literally named '*' or '?' use quoting: ls '*' or ls '\*'. #quoting #escaping
  - Use quotes to pass patterns to commands that should interpret them (e.g., find) without shell expanding. #quoting
  - Combine patterns: ls proj?.[ch] -> matches proj1.c, projA.h, etc. (#combine)
  - Ranges are inclusive and depend on locale for ordering. #ranges
  - For recursive matching, combine with find or use shell options (globstar ** in bash with shopt -s globstar). #globstar (note: advanced)

## Examples (compact)
- ls *.html -> all .html files #star
- ls A*.html -> files starting 'A' and ending '.html' #star
- ls project.?? -> two-character extension #questionmark
- ls [aeiou]* -> starts with vowel #brackets
- ls [!aeiou]* -> starts with non-vowel #negation
- ls [a-c]* -> starts with a, b, or c (range) #ranges

Keep this sheet nearby for quick pattern-to-behavior lookup during open-book exams.

---

## Module 8 — Lecture 74: Shell Metacharacters & Redirection — Cheatsheet

#hashtags: #shell #metacharacter #redirection #stdin #stdout #pipe #append #quoting #escape #comment #conditional-execution #sequential-execution #command-substitution #wc #greater-than #less-than #semicolon #ampersand #double-ampersand #double-pipe #backslash #backquote #single-quote #double-quote #newline #space #tab

---

## Key Definitions (one-line)
- Metacharacter: a character the shell treats specially (terminates/controls words) unless quoted.  
- stdout: standard output stream (file descriptor 1).  
- stdin: standard input stream (file descriptor 0).  
- Redirection: sending stdout/stdin to/from files using special symbols.  
- Pipe: connect stdout of one command to stdin of another.  
- Quoting: using single/double quotes or backslash to prevent special treatment of metacharacters.  
- Escape (backslash \): makes the next character literal.  
- Command separator (;): run commands sequentially, regardless of success.  
- Conditional AND (&&): run second command only if first succeeds (exit status 0).  
- Conditional OR (||): run second command only if first fails (non-zero exit status).  
- Comment (#): marks the rest of the line as a comment.  
- Backquote (`...`): command substitution (execute enclosed command and use its output).

---

## Formulas / Notation (quick mapping)
- command > file         — redirect stdout to file (overwrite)  
- command >> file        — append stdout to file  
- command < file         — take stdin from file  
- cmd1 | cmd2            — pipe: stdout(cmd1) → stdin(cmd2)  
- cmd1 ; cmd2            — run cmd1 then cmd2 (always)  
- cmd1 && cmd2           — run cmd2 only if cmd1 exits 0 (success)  
- cmd1 || cmd2           — run cmd2 only if cmd1 exits non-zero (failure)  
- # comment text         — comment; ignored by shell  
- `command` or $(command) — command substitution (backquote mentioned)  
- \char                  — escape char so it's treated literally

---

## Key Algorithms / Concepts (bulleted)
- Redirection: use > (overwrite) and >> (append) to send stdout to files. #> #>> #redirection  
- Input redirection: use < to feed a file as stdin to a command. #< #stdin  
- Pipes: use | to chain commands, passing output → input. Commands run concurrently; data flows via pipe buffer. #pipe  
- Sequential execution: use ; to run commands one after another regardless of exit status. #semicolon #sequential-execution  
- Conditional execution:  
  - && (AND): next runs only on success of previous. #&& #conditional-execution  
  - || (OR): next runs only on failure of previous. #|| #conditional-execution  
- Quoting / escaping: prevent metacharacter interpretation with single quotes, double quotes, or backslash. #quoting #backslash #single-quote #double-quote  
- Comments: # begins a comment to end-of-line. #comment  
- Command substitution: use backquotes (`...`) (transcript) to use command output as text. #backquote #command-substitution

---

## Important Properties / Invariants
- Quoted metacharacters are treated as literal characters (no special meaning). #quoting  
- Whitespace (space, tab, newline) and metacharacters terminate words unless quoted/escaped. #space #tab #newline  
- Exit status convention: 0 = success; non-zero = failure — used by && and ||. #exit-status  
- Semicolon (;) does not check exit status — both commands always run. #semicolon  
- && short-circuits on failure; || short-circuits on success. #&& #||  
- A pipe connects stdout of left command to stdin of right command (no file intermediate). #pipe  
- Appending (>>) preserves existing file contents and adds output to end. #append

---

## Quick Reference (scannable)
- > file         : overwrite file with command stdout     — e.g., cat file1 > out.txt  #>  
- >> file        : append stdout to file                  — e.g., echo Hello >> out.txt  #>> #append  
- < file         : use file as stdin                      — e.g., wc < temp.txt  #< #stdin  
- cmd1 | cmd2    : pipe output to next command            — e.g., cat temp.txt | wc  #pipe #wc  
- cmdA ; cmdB    : run A then B (always)                  — e.g., date ; who  #semicolon  
- cmdA && cmdB   : run B only if A succeeds               — e.g., mkdir d && cd d  #&&  
- cmdA || cmdB   : run B only if A fails                  — e.g., test -f f || echo "missing"  #||  
- # text         : comment the rest of the line           — e.g., # this is a comment  #comment  
- `cmd` or $(cmd): substitute output of cmd into line     — e.g., echo `date`  #backquote #command-substitution  
- \char          : escape a special character             — e.g., echo \$HOME prints $HOME  #backslash  
- Quoting rules:  
  - 'single quotes'  — everything literal, no expansion  #single-quote  
  - "double quotes"  — literal except $, `, \ (some expansion)  #double-quote

---

Examples from lecture (copyable)
- cat file > temp.txt        — write output to temp.txt  #>  
- echo Theekshna >> temp.txt — append string to file     #>>  
- wc < temp.txt              — count words from file     #< #wc  
- cat temp.txt | wc          — pipe cat → wc             #pipe #wc  
- cmd1 ; cmd2                — run cmd1 then cmd2        #semicolon  
- cmd1 && cmd2               — run cmd2 only if cmd1 succeeds  #&&  
- cmd1 || cmd2               — run cmd2 only if cmd1 fails     #||

---

Keep this sheet near your reference material for quick lookup of metacharacter behavior and common redirection/pipe patterns.

---

## Module 8 — Lecture 75: Shell Special Variables — Quick Reference

#keywords: #shell #bash #special-variables #positional-parameters #script #arguments #pid #exit-status #$0 #$1 #$$ #$# #$* #$@ #$?

## Key Definitions
- Special variable: a variable with predefined meaning in the shell/scripting environment.  
- Positional parameter: argument passed to a script, referenced by an integer index (e.g., $1).  
- Script name ($0): the name/path of the running script.  
- Argument count ($#): total number of positional parameters.  
- All arguments ($* / $@): the list of all positional parameters.  
- Process ID ($$): PID of the current shell/process.  
- Exit status ($?): exit code of the last executed command (0 = success).

## Formulas / Notation
- $# = number of arguments (integer ≥ 0)  
- $n = nth argument (n is positive integer)  
- $0 = script name (may be path or basename)  
- $$ = PID of current shell/process  
- $? = exit status (0 → success; nonzero → error)  
- Use braces for multi-digit positional indexes: ${10}, ${11}, ...

## Key Variables / Concepts
- $0 — script filename or command used to invoke the script. (#$0)  
- $1, $2, ... $n — positional parameters (first, second, …). (#$1)  
- $# — number of positional parameters. (#$#)  
- $* — all positional parameters as a single word (unquoted) or single string when quoted. (#$*)  
- $@ — all positional parameters but preserves separation when quoted ("$@"). (#$@)  
- $$ — process ID of the current shell. (#$$)  
- $? — exit status of the most recently executed command. (#$?)  

## Important Properties / Invariants
- $0 may include path or just the name depending on how invoked.  
- If no arguments: $# = 0; $1, $2, ... are empty/unset.  
- Quoting difference:
  - "$*" expands to all args as one string: "arg1 arg2 arg3".  
  - "$@" expands each arg as separate quoted word: "arg1" "arg2" "arg3".  
- Positional parameters beyond $9 must be referenced with braces: ${10}.  
- $? is set immediately after a command; executing another command (including echo) changes it.  
- $$ is constant within the script (the shell’s PID).  
- Exit status convention: 0 = success; nonzero = error (shell builtin/command-dependent codes).

## Quick Reference (table)
| Variable | Meaning | Typical example |
|---|---:|---|
| $0 | Script/command name | echo "$0" |
| $1 | 1st argument | echo "$1" |
| $2 | 2nd argument | echo "$2" |
| $n | nth argument | echo "${n}" |
| $# | Number of args | if [ $# -lt 1 ]; then ... fi |
| $* | All args (single word if quoted) | echo "$*" → "a b c" |
| $@ | All args (preserve boundaries when quoted) | for x in "$@"; do ...; done |
| $$ | PID of current shell | echo $$ |
| $? | Exit status of last command | cmd; echo $? |

## Quick Tips
- Use "$@" for safe iteration over args (preserves spaces). (#$@)  
- Check exit with if [ $? -ne 0 ]; then ... fi — but prefer conditional constructs directly (if cmd; then ...). (#$?)  
- Use ${N} when N >= 10 (avoid ambiguity).  
- $# is useful for validating required args.

(End of cheatsheet)

---

## Module 8 — Lecture 76: Bash Variables — Types, Usage & Common System Variables

#hashtags: #variable #bash #shell #environment #systemvariable #uservariable #ENV #echo #BASH #BASH_VERSION #BASHPID #HOME #PATH #PWD

## Key Definitions
- Variable: Named memory location (container) that holds a value which can change.
- System variable / Environment variable: Shell/OS-created variable required for shell operation (maintained by system).
- User-defined variable: Variable created and maintained by the programmer/user for scripts.
- Shell variable: Variable attached to a shell instance (e.g., stores shell path or settings).
- Memory location: Unique address in primary memory referred to by a variable name.

## Formulas / Syntax (quick reference)
- Access value: $VARNAME  (use dollar sign before name to read value)
- List environment variables: env
- Print variable: echo $VARNAME
- Note: System variables are conventionally in ALL CAPS.

## Key Concepts
- Purpose of variables: store data in memory, allow changing parts of commands dynamically.
- Types in Bash:
  - #systemvariable / #environment: created by OS/shell, used by shell to function.
  - #uservariable: created by user for scripts/programs.
- Viewing/printing:
  - Use env to list environment variables.
  - Use echo $VAR to print a variable’s value.

## Important System Variables (quick table)
| Variable | Meaning / stored value | Example command |
|---|---:|---|
| BASH | Absolute path to the current bash shell invoked | echo $BASH |
| BASH_VERSION | Version of the bash shell | echo $BASH_VERSION |
| BASHPID | Process ID (PID) of current bash process | echo $BASHPID |
| HOME | User’s home directory path | echo $HOME |
| PATH | Colon-separated list of directories to search for commands | echo $PATH |
| PWD | Present working directory | echo $PWD |

## Important Properties / Invariants
- System variables are defined in capital letters (convention).
- The shell relies on environment variables to function correctly.
- A variable holds one value at a time (value can change).
- To access a variable’s value you must prefix its name with $ (e.g., $HOME).
- env shows the environment variable list maintained by the system/shell.

## Quick Reference (scannable)
- List env vars: env
- Print var: echo $VARNAME
- Access syntax: $VARNAME
- Naming: SYSTEM variables => ALL_CAPS
- Types: #systemvariable (OS/shell) vs #uservariable (user-created)
- Common vars: $BASH, $BASH_VERSION, $BASHPID, $HOME, $PATH, $PWD

(Use this sheet to quickly locate commands and meanings during an open-book exam.)

---

## Module 8 — Lecture 77: User-defined Variables in Bash — Cheatsheet

#bash #shell #variables #user-defined #naming-rules #assignment #case-sensitive #null-variable #system-variables #regex #naming-conventions

## Key Definitions
- User-defined variable: A name/value pair created by the programmer in a shell script.
- System variable: Environment or shell-provided variables (commonly ALL_CAPS).
- Assignment: The syntax that gives a value to a variable (no spaces around =).
- Null variable: A variable defined with no value (empty string).
- Variable reference: Using a variable’s value (typically with $VAR).

## Formulas / Syntax / Regex
- Assignment syntax: VAR=value    (NO spaces around '=')
- Empty assignment: VAR=
- Reference: $VAR or "${VAR}"
- Valid-name regex: ^[a-zA-Z_][a-zA-Z0-9_]*$
- Common pattern: Start with letter or underscore, followed by letters/digits/underscores

## Key Concepts / Rules
- Naming rules:
  - Must start with a letter (A–Z, a–z) or underscore (_).
  - Remaining characters: letters, digits (0–9), or underscore.
  - Cannot start with a digit.
  - Case-sensitive: VAR and var are different.
- Assignment specifics:
  - No spaces around '=' — spaces break assignment (interpreted differently).
  - Use uppercase for conventional system variables; user variables often lowercase or mixed.
- Null variables:
  - Allowed: VAR= creates an empty value.
  - Printing a null var yields no output (empty).
- Avoid using characters with shell meaning:
  - Do not use ?, *, !, -, +, etc. in variable names (they have special shell semantics).

## Important Properties / Invariants
- Invariant: Variable names conform to regex ^[a-zA-Z_][a-zA-Z0-9_]*$.
- Invariant: Assignments require exact VAR=value (no whitespace).
- Invariant: Variables are case-sensitive and distinct by case.
- Convention: System/environment variables are usually ALL_CAPS (not enforced).

## Quick Reference — Examples & Common Pitfalls
- Valid examples:
  - NAME=John
  - _count=0
  - user1=alice
- Invalid examples (and why):
  - 1var=10       — starts with digit
  - my var=val    — contains space (breaks assignment)
  - name?=x       — contains special char (bad practice / error)
- Empty/null:
  - EMPTY=
  - echo "$EMPTY"   -> prints nothing
- Usage:
  - Assign: VAR=value
  - Print: echo $VAR   or   echo "$VAR"
- Remember:
  - No spaces around '='
  - Use $ to access value
  - Case matters: PATH ≠ path

Keep this as a quick checklist during the exam to verify variable naming and assignment correctness.

---

## Module 8 — Lecture 78: Interactive Shell Scripts — Read Input Cheatsheet

#keywords: #shell #bash #interactive #read #echo #stdin #stdout #variables #signals #CtrlC #kill #timeout #prompt #I/O

## Key Definitions
- Interactive script: a script that exchanges data with the user (input and/or output). #interactive
- stdin: standard input stream (typically keyboard). #stdin
- stdout: standard output stream (typically console). #stdout
- read: shell builtin that reads a line from stdin and assigns it to variable(s). #read
- echo: prints text to stdout. #echo
- Ctrl+C: keyboard interrupt that sends SIGINT to kill process (manual termination). #CtrlC #signals
- kill: command to send signals (e.g., terminate) to processes. #kill
- timeout: remote connection/session may expire causing script to stop waiting. #timeout
- Variable assignment (by read): input tokens mapped to variables in order. #variables

## Syntax / Formulas / Equations
- Basic read:
  - read var
- Read multiple values:
  - read var1 var2
- Prompt + read (single statement):
  - read -p "Prompt text: " var
- Print:
  - echo "text $var"
- Data flow directions:
  - script -> user: echo (stdout)
  - user -> script: read (stdin)

## Key Algorithms / Concepts
- Making a script interactive:
  - Use echo to ask for input; use read to capture it. #interactive #echo #read
- Waiting behavior when read expects input:
  - Script blocks (waits) until input + Return. #stdin
- Handling multiple inputs:
  - read can split a line into multiple variables (space-separated). #read #variables
- Single-step prompt+read:
  - read -p displays prompt and reads input in one step. #read #prompt
- Outcomes if user provides no input:
  - Wait indefinitely until input. #blocking
  - User can kill process (Ctrl+C or kill). #CtrlC #kill
  - Remote session may timeout and terminate waiting. #timeout

## Important Properties / Invariants
- read reads a single line (terminated by Return) from stdin and assigns to variables in sequential order. #read
- If fewer variables than fields: last variable gets the remainder. #variables
- If more variables than fields: extra variables become empty. #variables
- echo writes output immediately to stdout; useful to prompt or display results. #echo
- Combining prompt and read reduces lines and makes script concise: read -p. #prompt

## Quick Reference (scannable)
- Prompt then read (two lines)
  - echo -n "Enter name: "
  - read name
- Prompt+read (one line)
  - read -p "Enter two numbers (a b): " a b
- Read two values into x and y:
  - read x y
  - echo "x=$x, y=$y"
- Print result (example sum):
  - echo "Sum = $((x + y))"
- Blocking behavior:
  - While read waiting → script pauses until Return or termination. #blocking
- Terminate waiting:
  - Ctrl+C (SIGINT) from same terminal. #CtrlC
  - kill <pid> from another shell. #kill
  - remote session timeout/disconnect. #timeout

## Examples (compact)
- Single value:
  - read -p "Name: " name
  - echo "Hello, $name"
- Two values:
  - read -p "Enter two numbers: " x y
  - echo "x=$x y=$y"

#hashtags (all major items): #interactive #shell #bash #read #echo #stdin #stdout #variables #prompt #CtrlC #kill #timeout #signals


---

## Module 8 — Lecture 79: expr (Shell) — Quick Cheatsheet

Keywords: #expr #shell #bash #commandline #arithmetic #string #relational #variables #escaping #quoting #length #index #substr #operators

## Key Definitions
- expr: POSIX utility to evaluate integer or string expressions and print the result to stdout. #expr
- Arithmetic expression: uses +, -, \*, /, % between operands (requires spaces). #arithmetic #operators
- Relational expression: compares values; returns 1 if true, 0 if false. #relational
- String operations: built-in keywords `length`, `index`, `substr` for string queries. #string #length #index #substr
- Variable assignment (shell): use no spaces around `=` (e.g., A=10). #variables

## Syntax / Important Rules (short)
- Always put spaces around operators in expr: expr 10 + 20
- Quote or escape the whole expression when it contains shell-special characters: expr "A \* B" or expr A \* B
- Escape `<` and `>` (they are redirection operators): expr 5 \< 3
- Use a single `=` for string/number compare (with spaces): expr a = b
- expr uses 1-based indexing for strings (index/ substr). #1based

## Formulas / Examples
- Arithmetic:
  - expr 10 + 20 -> 30
  - expr 20 - 5  -> 15
  - expr 4 \* 3  -> 12  (escape `*`) 
  - expr 10 / 3  -> 3   (integer division)
  - expr 10 % 3  -> 1
- Relational (returns 1 if true, 0 if false):
  - expr 5 \< 3   -> 0  (escape `<`)
  - expr 5 \> 3   -> 1  (escape `>`)
  - expr 5 = 5    -> 1
- Strings:
  - expr length "hello"    -> 5
  - expr index "hello" e   -> 2   (first position of 'e'; 0 if not found)
  - expr substr "hello" 2 3 -> ell  (substr STRING POS LEN; POS is 1-based)

## Key Algorithms / Concepts (bullet)
- #ArithmeticOperations: +, -, \*, /, % — integer-only, integer division truncates.
- #RelationalOps: <, >, = — must be escaped (<, >) and spaced; return 1/0.
- #StringOps:
  - length STRING -> integer length
  - index STRING CHARS -> position of first occurrence of any char in CHARS (0 if none)
  - substr STRING POS LEN -> substring from POS (1-based) of length LEN
- #QuotingEscaping: Quote entire expr or escape special symbols to prevent shell interpretation.
- #VariableRules: assignment with no spaces (A=10); when using variables in expr, expand them: expr "$A" + "$B" or expr $A + $B

## Important Properties / Invariants
- Spaces are mandatory around expr operators; without them, expr treats token as a string.
- Relational results are numeric (1 = true, 0 = false), not boolean words.
- expr outputs plain text to stdout; capture with command substitution: result=$(expr 1 + 2)
- `*`, `<`, `>` must be escaped or quoted to avoid shell globbing/redirects.
- Indexing for strings is 1-based; index returns 0 for not-found.

## Quick Reference (scannable)
- Arithmetic operators: + - \* / %  — remember to escape `*`
- Relational: \< \> =  — returns 1 or 0
- String keywords: length, index, substr
- Common examples:
  - expr 10 + 20        -> 30
  - expr "10+20"        -> 10+20 (no spaces => string)
  - expr A=10           -> (invalid inside expr; use shell assignment `A=10`)
  - A=10; B=20; expr $A + $B -> 30
  - expr length "hi"    -> 2
  - expr index "abc" d  -> 0
  - expr substr "hello" 2 3 -> ell
- Pitfalls:
  - Forgetting spaces: expr 10+20 outputs "10+20"
  - Not escaping `*` or `<`/`>` leads to unintended shell behavior
  - Using `==` or `-eq` inside expr: use single `=` (expr syntax differs from [ ] tests)

Keep this sheet handy for quick lookup of expr syntax, operators, and common gotchas.

---

## Module 8 — Lecture 80: Shell Scripting — Week 7 Cheatsheet

Keywords: #shellscript #bash #shebang #variables #wildcards #metacharacters #read #echo #expr #arithmetic #logical-operators #special-variables #system-variables #redirection #pipes

---

## Key Definitions
- Shebang: #! /path/to/interpreter (e.g., #!/bin/bash) — specifies the interpreter for the script.  
- Comment: line starting with # (except shebang) — ignored by shell.  
- Variable: name given to a memory location that stores data; used via $name to access value.  
- Positional parameters: $0, $1, $2, ... — command-line arguments passed to script.  
- Special variables: predefined symbols that provide shell/process info (see list).  
- Wildcards (metacharacters): patterns used by the shell to match filenames: *, ?, [range], [!range].  
- Exit status: numeric return code of a command; 0 = success, non-zero = failure.

---

## Formulas / Notation
- Access value of variable: $name  
- Positional args: $0 (script), $1, $2, ...  
- Count of args: $#  
- All args (unquoted/quoted): $* / $@ (see Quick Reference)  
- Last command exit status: $?  
- Current script PID: $$  
- Last background PID: $!  
- Basic arithmetic with expr: expr $a + $b  (spaces required around operators)  
- Preferred arithmetic expansion: $(( a + b ))  (no external command)

---

## Key Commands & Concepts
- Shebang: #!/bin/bash — put as first line to indicate interpreter. #bash #shebang
- Run script:
  - Explicit interpreter: bash script.sh  (works even without shebang)
  - Executable script: chmod +x script.sh; ./script.sh  (requires shebang or executable)
- Echo: echo "text" — prints text; echo -n "prompt"  (suppresses trailing newline so prompt and read appear on same line) #echo
- Read input (interactive scripts): read var  — reads a line from stdin into var #read
- Variables:
  - Assign: name=value  (no spaces around =)
  - Use: echo "$name" or echo $name  (use quotes to preserve whitespace) #variables
- Arithmetic:
  - expr: expr $a + $b  (spaces mandatory)  #expr
  - Arithmetic expansion: result=$((a + b))  (recommended)
- Wildcards / Metacharacters:
  - * = zero or more characters
  - ? = exactly one character
  - [a-z0-9] = one character in range
  - [!...] = one character NOT in range
  Examples: file?.txt, file[1-3].txt, *.txt  #wildcards #metacharacters
- Logical operators:
  - cmd1 && cmd2  — run cmd2 only if cmd1 succeeds (exit status 0)  #logical-operators
  - cmd1 || cmd2  — run cmd2 only if cmd1 fails (non-zero exit)  #logical-operators
- Redirection & pipes (reminder):
  - >, >> (truncate/append), < (input redirect), | (pipe)  #redirection #pipes

---

## Important Properties / Rules
- Variable names:
  - Case-sensitive (NAME ≠ name).  
  - Must not contain spaces; use underscores for separation.  
  - Cannot start with a digit; may start with letter or underscore.  
  - No spaces around assignment: wrong → a = 1 ; correct → a=1.  
- Always use $ to expand a variable when you want its value (e.g., echo "$var").  
- expr requires spaces around operators; failure to space breaks the command.  
- Exit status convention: 0 ⇒ success; any non-zero ⇒ failure/error.  
- Use quotes around expansions that may contain spaces: "$var", "$@".

---

## Special & System Variables (Quick list)
- $0 — script name  
- $1, $2, ... — positional arguments  
- $# — number of positional arguments  
- $* — all positional parameters as a single word/string (when quoted: "$*" → single string)  
- $@ — all positional parameters, expands to separate quoted words (when quoted: "$@" → preserves arg separation)  
- $? — exit status of last command  
- $$ — current shell/script PID  
- $! — PID of last background command  
- $- — current shell options  
- PATH, SHELL, HOME, PWD, USER, UID — environment/system variables (usually uppercase)  #system-variables

---

## Quick Reference (scannable)
- Shebang: #!/bin/bash  (put at top)
- Comment: # this is a comment
- Create/print prompt + read input:
  - echo -n "Enter name: "  ; read name
  - echo "Hello, $name"
- Assign & print:
  - a=10 ; b=20
  - echo "sum=$(expr $a + $b)"   (or sum=$((a+b)); echo "$sum")
- Variable rules:
  - good: my_var=1, _temp=2, var2=3
  - bad: 2var=1, my var=1, var =1
- Wildcards examples:
  - ls *.txt  → all .txt files
  - ls file?.txt  → file plus exactly 1 char before .txt
  - ls file[1-3].txt  → file1.txt file2.txt file3.txt
  - ls file[!0-9].txt  → file followed by non-digit
- Logical operators:
  - mkdir dir && echo "created"    # prints only if mkdir succeeds
  - mkdir dir || echo "already exists"  # prints only if mkdir fails
- Positional args sample usage:
  - script.sh a b c
  - $0 → script.sh ; $1 → a ; $# → 3 ; "$@" → ("a" "b" "c")
- Exit codes:
  - Use exit N to return code N from script; check with $?

---

Keep this as a quick lookup during exams. For usage examples, prefer read + "$@" handling, and prefer $((...)) for arithmetic unless specifically required to use expr.

---

## Module 9 — Lecture 81: Bash test / [ ] Cheatsheet

#hashtags: #bash #shell #test #brackets #conditionals #if #comparison #integeroperators #stringoperators #fileoperators #exitstatus #read #modulus

---

---

## Key Definitions (one-line)
- test: builtin that evaluates a command, expression, or file test; returns exit status 0 (true) or 1 (false).  
- [ ... ]: POSIX synonym/alias for test (must have surrounding spaces and closing ]).  
- exit status ($?): numeric status of last command; 0 = true/success, non‑0 = false/failure.  
- integer comparison operators: operators used to compare numeric values inside test/[ ].  
- file test: test of filesystem properties (regular file, directory, executable, etc.).  
- modulus (%): arithmetic remainder operator (used via arithmetic expansion $((...)) or ((...))).  
- read: builtin to read user input into a variable.

---

## Syntax / Forms
- test expression
- [ expression ]    (must have spaces: [ x -eq y ] )
- if test ...; then ... fi
- if [ ... ]; then ... fi
- Use $? to check last command exit status.

Examples:
- test 10 -gt 5
- [ "$num" -eq 0 ]
- if [ "$n" -eq 0 ]; then echo "zero"; fi

---

## Formulas / Notations
- test true -> exit code 0  
- test false -> exit code 1  
- check status: echo $?  (0 means true)  
- arithmetic expansion: $(( expression ))  
- modulus example: remainder=$(( n % 2 ))

---

## Key Operators (Quick Tables)

Integer comparisons (use inside test/[ ])
- -eq : equal
- -ne : not equal
- -gt : greater than
- -lt : less than
- -ge : greater or equal
- -le : less or equal

String tests
- =   : string equality (in test/[ ])
- !=  : string inequality
- -z  : string length is zero
- -n  : string length is non-zero

File tests (common)
- -e : file exists
- -f : file exists and is regular file
- -d : file exists and is directory
- -x : file is executable
- -r : readable
- -w : writable
- -s : size > 0 (non-empty)

Logical / other
- !   : logical NOT (negation)
- -a  : logical AND (supported but can be ambiguous)
- -o  : logical OR  (supported but can be ambiguous)
- Prefer separate tests combined with && and || in shell scripts for clarity.

---

## Key Algorithms / Concepts (bulleted)
- #input-checking: Use read to get user input; perform numeric comparison with test/[ ].
- #parity-check: Compute remainder and compare to 0 for even/odd:
  - remainder=$(( n % 2 )); [ "$remainder" -eq 0 ]
  - or: if (( n % 2 == 0 )); then ... (arithmetic context)
- #control-flow: Use test/[ ] inside if statements to drive conditional behavior.
- #file-validation: Use file test operators (e.g., -f, -x) to check file type/permissions before operations.
- #exit-status: Use $? immediately after a command to inspect success/failure.

---

## Important Properties / Invariants
- Spaces matter: [ and ] must be separated by spaces from the expression.
- Quote variables: use "$var" inside test to avoid word-splitting and empty-string errors.
- test/[ ] return 0 on true, 1 on false (check with $?).  
- Use $((...)) or ((...)) for arithmetic; test only does string-tokenized comparisons.
- File tests test filesystem metadata, not contents (except -s for non-empty).

---

## Quick Reference (scannable)

Usage examples:
- Numeric compare: [ "$a" -gt "$b" ]
- Equality: [ "$s1" = "$s2" ]
- Not equal: [ "$s" != "" ]  or [ -n "$s" ]
- Null/empty: [ -z "$s" ]
- File exists: [ -e "/path" ]
- Regular file: [ -f "/path" ]
- Directory: [ -d "/path" ]
- Executable: [ -x "/path" ]
- Non-empty file: [ -s "/path" ]

Parity example:
- read -p "Enter n: " n
- if [ $((n % 2)) -eq 0 ]; then echo "even"; else echo "odd"; fi

Check last command:
- some_cmd
- echo $?   # 0 = success/true

Best practices (short):
- Always quote variables inside [ ]. Example: [ "$var" -eq 0 ]
- Ensure spaces around [ and ]
- Prefer arithmetic context (( ... )) for complex numeric expressions
- Use logical && / || between commands for clearer control flow when combining tests

---

End of cheatsheet — concise lookup for using test and [ ] in Bash.

---

## Module 9 — Lecture 82: Bash comparison-based branching — Cheatsheet

#bash #shell #if #if-else #if-elif-else #case #test #[] #comparison #operators #-eq #-ne #-lt #-le #-gt #-ge #exit-status #$?

## Key Definitions
- Decision-making: executing different actions based on conditions.
- if statement: branch executed when a condition is true (closed by `fi`).
- if-else / if-elif-else: variants to select alternate branches or multiple conditions.
- case statement: switch-like construct for branching on a single variable's value.
- test command (`test`) / bracket alias (`[ ... ]`): evaluate comparisons, return exit status.
- Exit status: numeric return code of a command; 0 = true/success, non-zero = false/failure.
- `$?`: exit status of the last executed command.

## Syntax & Short Examples
- Basic if:
  - multiline:
    ```
    if CONDITION
    then
      COMMANDS
    fi
    ```
  - with else:
    ```
    if CONDITION; then
      COMMANDS
    else
      OTHER_COMMANDS
    fi
    ```
  - with elif:
    ```
    if C1; then
      ...
    elif C2; then
      ...
    else
      ...
    fi
    ```
- Using test or brackets:
  - `if test A -eq B; then ... fi`
  - `if [ A -eq B ]; then ... fi`
- Quick `$?` check:
  - `some_cmd; echo $?`  # prints exit status (0 → true)

- case (conceptual):
  - Branch on one variable's value (similar to switch). Useful when all branches depend on a single input.

## Operators / Comparisons (numeric)
| Operator | Meaning |
|---:|---|
| `-eq` | equal to |
| `-ne` | not equal to |
| `-lt` | less than |
| `-le` | less than or equal to |
| `-gt` | greater than |
| `-ge` | greater than or equal to |

Usage forms:
- `test A -eq B`
- `[ A -eq B ]`

## Important Properties / Invariants
- Exit status semantics: 0 means condition true (success), any non-zero means false (failure).
- `test` and `[ ... ]` return an exit status — used directly by `if`.
- Bracket form requires spaces: `[ A -eq B ]` (space after `[` and before `]`).
- `then` starts the true-block; `fi` ends the if-block (reverse of `if`).
- `case` is best when branching solely on a single variable's value.

## Quick Reference (scannable)
- if structure: `if COND; then ...; fi`
- if-else: `if COND; then ...; else ...; fi`
- if-elif: `if C1; then ...; elif C2; then ...; else ...; fi`
- test forms:
  - `test A -eq B`
  - `[ A -eq B ]`  ← must have spaces
- Numeric operators: `-eq -ne -lt -le -gt -ge`
- Condition truth: `exit status == 0` → condition is true
- Check last status: `echo $?`
- Use `case` when selecting among many values of one variable (switch-like)

## Quick pitfalls (exam-friendly reminders)
- Missing spaces in `[ ... ]` → syntax error.
- Forgetting `then` or `fi` → syntax error.
- Treat exit status 0 as true (inverted thinking leads to bugs).
- Use numeric operators shown above for integer comparisons.

#hashtags: #bash #shell #if #if-else #if-elif-else #case #test #[] #comparison #operators

---

## Module 9 — Lecture 83: Bash conditionals cheatsheet

#hashtags: #Bash #shell #if #else #fi #elif #conditionals #comparison #arithmetic #modulus #expr #arithmetic-expansion #exit-status

---

---

## Key Definitions (one-line)
- if statement: branch that executes a "true" block when CONDITION is true.
- else: block executed when if-condition is false.
- elif: "else if" — additional condition checked if previous were false.
- fi: terminator for if/elif/else block.
- CONDITION: any test/command whose exit status determines true (0) or false (non‑0).
- exit status: 0 means success/true, non‑0 means false/failure.
- modulus operator (%): returns remainder of integer division.
- expr: external command for arithmetic (older style).
- (( )): arithmetic evaluation/compound expression (preferred for readability).

---

## Syntax (quick snippets)
- Basic if-else
  ```
  if CONDITION; then
    # true block
  else
    # false block
  fi
  ```
- If-elif-else ladder
  ```
  if COND1; then
    CMD1
  elif COND2; then
    CMD2
  else
    CMD_else
  fi
  ```
- Numeric comparison with test/[ ]
  ```
  if [ "$n" -gt 0 ]; then ...
  ```
- Arithmetic expression (recommended)
  ```
  if (( n % 2 == 0 )); then echo "even"; else echo "odd"; fi
  ```

---

## Comparison operators (numeric)
| Operator | Meaning |
|---:|---|
| -eq | equal |
| -ne | not equal |
| -gt | greater than |
| -ge | greater or equal |
| -lt | less than |
| -le | less or equal |

(When using (( )) you can use standard C-style operators: ==, !=, >, >=, <, <=, %, etc.)

---

## Formulas / Mappings
- CONDITION true  -> exit status 0
- CONDITION false -> exit status != 0 (commonly 1)
- Even/odd check: n % 2 == 0 => even; otherwise odd
- Using arithmetic:
  - (( expr )) returns exit 0 if expr evaluates non-zero; in tests use comparisons for boolean

---

## Key Algorithms / Concepts (bulleted)
- #if: single decision between two blocks (#true-block, #false-block)
- #elif ladder: chain multiple mutually exclusive checks; first true branch executed
- #else: fallback executed only if all prior conditions false
- #(( )) arithmetic expansion: preferred for integer math and readability vs #expr
- #expr: older arithmetic tool — often replaced by (( )) or $(( ))
- Exit-status-driven control: any command/test can be CONDITION (not just comparisons)

---

## Important Properties / Invariants
- fi is required to close an if block.
- Only the first true branch in an if/elif chain executes; remaining branches skipped.
- else is optional.
- For [ ... ] tests, spaces around brackets and operators are required (e.g., [ "$a" -lt 0 ]).
- (( )) treats expression semantics; no extra quoting needed for integers.
- Numeric operators differ between [ ] (use -gt/-lt) and (( )) (use >/<).
- Return/print of exit status: true -> 0, false -> non‑0 (commonly 1).

---

## Quick Reference (scannable)
- Basic pattern: if COND; then ...; else ...; fi
- If-elif: if A; then X; elif B; then Y; else Z; fi
- Even test:
  - if (( n % 2 == 0 )); then echo even; else echo odd; fi
- Positive/negative/zero:
  - if [ "$n" -lt 0 ]; then echo negative
  - elif [ "$n" -gt 0 ]; then echo positive
  - else echo zero; fi
- Common numeric comparisons: -eq, -ne, -gt, -ge, -lt, -le
- Use (( )) for arithmetic: (( n += 1 )), (( n % 2 ))
- Condition truth: command exit status 0 == true
- Debug tip: check $? immediately to inspect last command’s exit code

---

Keep this page for fast lookup of syntax, operators, and common conditional patterns in Bash.

---

## Module 9 — Lecture 84: Case Statement (Linux shell) — Cheatsheet

#hashtags: #case #shell #bash #if-elif #multilevel-if #patternmatching #default #string #integer #switch

---

## Key Definitions
- case statement: branching construct that selects a block based on a single expression's value.  
- if-elif ladder (multilevel-if): series of if/elif/else checks; alternative to case.  
- pattern: value or glob used to match the expression in a case branch.  
- default (star): `*` pattern that matches when no other pattern does.

---

## Syntax (quick template)
- General:
  ```
  case <expression> in
    pattern1) commands ;; 
    pattern2|pattern3) commands ;;
    *) default-commands ;;
  esac
  ```
- Notes:
  - Use `|` to separate multiple patterns for one branch.
  - Terminate each branch with `;;`.
  - End the construct with `esac`.

---

## Formulas / Notation
- First-match wins: evaluation stops when a matching pattern is found.
- Expression types: #integer or #string (case works for both).
- Efficiency: case is generally more efficient than repeated #if-elif when all branches depend on the same variable.

---

## Key Concepts / Usage
- Use #case when all branches depend on the value of a single variable.
- Use `*` as the default branch (fallback) when no patterns match.
- Patterns support shell-style globbing (basic wildcards) — useful for matching ranges/sets of values.
- Branch grouping: `patternA|patternB)` executes the same commands for multiple matches.
- Input examples from lecture:
  - Numeric option example: `3` → prints "information technology".
  - Unknown numeric `4` or `5` → falls to `*` and prints "other branch".
  - String example: input `"CSE"` → matches and prints "computer science and engineering".
  - Unknown string `"PHY"` → falls to `*` and prints "other branch".

---

## Important Properties / Invariants
- Single-expression dispatch: case examines one expression and compares against patterns.
- Order matters: put more specific patterns before more general ones.
- Deterministic: the first matching pattern determines the executed block.
- Can match both strings and numbers (both treated as text for matching).
- Cleaner and often more efficient than multiple `if/elif` blocks when branching on one value.

---

## Quick Reference (scannable)
- Start: `case <expr> in` — End: `esac`
- Branch end: `;;`
- Multiple patterns: `a|b|c)`
- Default/fallback: `*)`
- When to use:
  - Use #case if: many branches, all depend on same variable.
  - Use #if-elif if: branches have different conditions not tied to a single value.
- Behavior:
  - Checks patterns sequentially → first match executed → then exits case.
  - If no match → `*` executes (if present); otherwise no branch runs.
- Inputs:
  - Works for both numeric and text inputs (treated as strings for matching).

---

Keep this sheet next to your exam questions as a quick lookup for #case syntax, patterns, and when to prefer it over #if-elif.

---

## Module 9 — Lecture 85: Bash String Operations in if Statements — Cheatsheet

#bash #strings #if #test #[] #test-command #string-comparison #-n #-z #equality #inequality #exit-status #quoting #read

## Key Definitions
- test / [ ]: POSIX command/alias used to evaluate conditions in if statements.  
- if statement: executes commands based on test command exit status.  
- -n: returns true if string is non-empty.  
- -z: returns true if string is empty (inverse of -n).  
- "=": string equality operator in test / [ ].  
- "!=": string inequality operator.  
- Exit status: 0 = true (condition met), non‑zero = false.

## Formulas / Notation
- exit status: true ⇨ 0, false ⇨ 1 (or any non‑zero)  
- Common pattern: if [ condition ]; then ...; fi

## Key Concepts / Operations
- #StringEquality: [ "$a" = "$b" ] → true if strings are equal (returns 0).  
- #StringInequality: [ "$a" != "$b" ] → true if strings differ.  
- #NonEmptyCheck: [ -n "$s" ] → true if s is not empty.  
- #EmptyCheck: [ -z "$s" ] → true if s is empty.  
- #ReadInput: read var to get user input, then test the variable in if.  
- #IfElse: use if ... then ... else ... fi to branch on string tests.

## Important Properties / Invariants
- #Spacing: In [ ... ] ensure spaces around brackets and tokens: [ "$a" = "$b" ] (NOT ["$a"="$b"]).  
- #Quoting: Always quote variables: "$var" to avoid word-splitting and errors when empty.  
- #POSIX vs Bash: [ ] is POSIX-compatible; use "=" for equality. [[ ]] (bash) permits == and pattern matching.  
- #ReturnValues: test returns 0 for true conditions — if interprets 0 as success/true.

## Quick Reference (scannable)
| Test expression | Meaning | Example |
|---|---:|---|
| [ -n "$s" ] | string non-empty | if [ -n "$s" ]; then echo "non-empty"; fi |
| [ -z "$s" ] | string empty | if [ -z "$s" ]; then echo "empty"; fi |
| [ "$a" = "$b" ] | strings equal | if [ "$a" = "$b" ]; then echo "same"; fi |
| [ "$a" != "$b" ] | strings not equal | if [ "$a" != "$b" ]; then echo "different"; fi |

Quick patterns:
- Read + check non-empty:
  - read s
  - if [ -n "$s" ]; then echo "true"; else echo "false"; fi
- Read two strings + compare:
  - read a b
  - if [ "$a" = "$b" ]; then echo "strings are same"; else echo "strings are different"; fi

## Exam Tips (one-liners)
- Always put spaces inside [ ] and quote variables. #Spacing #Quoting  
- Remember: test returns 0 for true — if checks for success. #exit-status  
- Use "=" with [ ]; use "==" only in [[ ]] when doing pattern matches. #POSIX

--- 
Hashtags included above for quick searching: #bash #strings #test #if #-n #-z #equality #inequality #quoting #exit-status

---

## Module 9 — Lecture 86: Bash Logical Operators & File Tests — Cheatsheet

#keywords: #bash #logical-operators #if-statement #AND #OR #NOT #short-circuit #test #file-operators #-e # -f # -d # -x

## Key Definitions (one-line)
- Logical AND (&&): true only if both sub-expressions are true.  
- Logical OR (||): true if at least one sub-expression is true.  
- Logical NOT (!): negates the truth of an expression.  
- Short-circuit evaluation: second operand not evaluated if result determined by first.  
- Test expression brackets: [[ ... ]] indicate a compound/complex condition.  
- File test operators: unary checks that test file/directory properties (e.g., -e, -f, -d, -x).

## Formulas / Syntax (quick)
- Compound tests:
  - if [[ expr1 && expr2 ]]; then ... fi
  - if [[ expr1 || expr2 ]]; then ... fi
  - if [[ ! expr ]]; then ... fi
- Numeric comparisons:
  - a -eq b  (equal), -ne (not equal), -gt (greater), -lt (less), -ge (>=), -le (<=)
- File tests:
  - -e file  (exists)
  - -f file  (regular file)
  - -d file  (directory)
  - -x file  (executable)

## Key Concepts / Examples
- #Logical-AND:
  - Use && (two ampersands) inside [[ ... ]] for combined requirement.
  - Example (two-digit check): [[ $n -gt 9 && $n -lt 100 ]]
- #Logical-OR:
  - Use || (two pipes) inside [[ ... ]] for either/or checks.
  - Example (out-of-range check): [[ $n -lt 10 || $n -gt 99 ]]
- #Logical-NOT:
  - Use ! to invert a condition: [[ ! -e "$file" ]]  (true when file does not exist)
- #Short-circuit:
  - AND: if first expr is false, second is not evaluated.
  - OR: if first expr is true, second is not evaluated.
- #File-tests:
  - Example (exists): if [[ -e "$name" ]]; then echo "exists"; else echo "no"; fi
  - Example (is file): [[ -f "$name" ]]; then ...
  - Example (is directory): [[ -d "$name" ]]; then ...
  - Example (is executable): [[ -x "$name" ]]; then ...

## Important Properties / Invariants
- Complex condition typically enclosed with double square brackets [[ ... ]] (signals compound tests).
- Logical operators inside [[ ... ]] are boolean operators for test expressions.
- Short-circuiting can avoid errors (e.g., skip second test that would fail when first false/true).
- Use numeric test operators (-gt, -lt, etc.) for integers, not > or < without quotes/escaping.
- File tests return true/false; handle both cases to avoid script errors.

## Quick Reference (scannable)
- Logical
  - &&  — AND (both true)
  - ||  — OR  (any true)
  - !   — NOT (invert)
- Numeric compare
  - -eq, -ne, -gt, -lt, -ge, -le
- File tests
  - -e file  — exists
  - -f file  — is regular file
  - -d file  — is directory
  - -x file  — is executable
- Example one-liners
  - Two-digit check: if [[ $n -gt 9 && $n -lt 100 ]]; then echo "valid"; fi
  - Out-of-range check: if [[ $n -lt 10 || $n -gt 99 ]]; then echo "wrong input"; fi
  - File exists: if [[ -e "$file" ]]; then echo "found"; else echo "not found"; fi
- Notes
  - First operand may prevent second from running (short-circuit).
  - Always enclose complex conditions in [[ ... ]] for readability and safety.

#tags: #bash #logical-operators #if-statement #file-tests #-e # -f # -d # -x #short-circuit

---

## Module 9 — Lecture 87: Bash For-Loop Cheatsheet

#hashtags: #bash #shell #forloop #for-in #c-style #loops #range #braceexpansion #variables #syntax #increment #decrement

---

## Key Definitions
- for loop: A construct to repeat commands over a list or range.  
- for-in loop: Iterates over a specified list of values (space-separated).  
- C-style for loop: Three-part loop (initializer; condition; step) similar to C.  
- list: Sequence of items separated by spaces used by for-in.  
- brace expansion / range: `{start..end}` (optionally `{start..end..step}`) producing a list of values.  
- initializer: Expression run once before loop (C-style).  
- condition / loop test: Boolean check evaluated each iteration (C-style).  
- accounting expression / step: Update run after each iteration (C-style).

---

## Syntax / Formulas
- For-in style:
  - Syntax: for <var> in <list>; do <commands>; done
  - Example: for item in one two three; do echo $item; done
- For-in range (brace expansion):
  - `{start..end}` -> sequence from start to end
  - `{start..end..step}` -> sequence with increment/decrement (step can be negative)
  - Examples: `{1..10}`, `{1..10..2}`, `{10..1..-1}`
- C-style for:
  - Syntax: for (( init; condition; step )); do <commands>; done
  - Example: for (( i=1; i<=10; i++ )); do echo $i; done
- Keywords: for, in, do, done

---

## Key Algorithms / Concepts
- Iteration over explicit lists: for x in a b c; do ...
- Iteration over variable words: for w in $var; do ...  (each space-separated word)
- Iteration over numeric ranges via brace expansion: for n in {start..end[..step]}; do ...
- C-style numeric iteration for fine-grained control: for (( init; cond; step )); do ...

---

## Important Properties / Invariants
- #for-in:
  - Items are separated by spaces (word-splitting defines items).
  - List items can be integers, characters, strings, mixed types.
  - Can iterate over words from a variable (word-splitting applies).
  - Brace expansion produces a literal list before loop execution.
- #c-style:
  - Uses round parentheses with three expressions separated by semicolons.
  - Initializer runs once; condition checked each iteration; step runs after each iteration.
  - Syntax and operators resemble C (e.g., i++, i+=2).

---

## Quick Reference (scannable)
- Basic for-in:
  - for x in a b c; do cmd "$x"; done
- From variable words:
  - line="learn bash loops"
  - for word in $line; do echo "$word"; done
- Range (ascending):
  - for i in {1..10}; do echo $i; done
- Range with step:
  - for i in {1..10..2}; do echo $i; done
- Range descending:
  - for i in {10..1..-1}; do echo $i; done
- C-style numeric:
  - for (( i=1; i<=10; i++ )); do echo $i; done
- Keywords reminder:
  - for / in / do / done

---

Keep this sheet handy for syntax lookups and quick examples during an open-book exam.

---

## Module 9 — Lecture 88: Bash Loops & Flow Control — #while #until #break #continue #bash

## Keywords
#bash #loops #controlflow #while #until #break #continue #do-done #infinite-loop #ctrl-c

---

## Key Definitions
- #while: Loop that repeats while a command/condition evaluates to true (exit status 0).  
- #until: Loop that repeats until a command/condition evaluates to true (runs while false / non‑zero exit).  
- #break: Exit the current loop (or N levels with argument).  
- #continue: Skip remainder of current iteration and proceed to next (or N levels with argument).  
- #do-done: Delimiters that enclose the loop body in shell.  
- #infinite-loop: A loop with a condition that always evaluates true (e.g., `while true`).  
- #ctrl-c: Keyboard interrupt to forcibly stop a running loop/process.

---

## Formulas / Evaluation Rules
- Shell truth: command exit status 0 → true; non‑zero → false. (#bash)
- while syntax: `while <command>; do <body>; done` — executes while `<command>` returns 0. (#while)
- until syntax: `until <command>; do <body>; done` — executes while `<command>` returns non‑zero; stops when it returns 0. (#until)
- Arithmetic test examples:
  - `[ "$i" -lt 10 ]` → test builtin (0=true)
  - `(( i < 10 ))` → arithmetic (0=true)

---

## Key Algorithms / Concepts
- #while loop
  - Re-evaluates condition before each iteration.
  - Typical use: iterate while index less than limit.
- #until loop
  - Reverse of while: runs while condition is false; stops when true.
  - Use when you want to run until some success condition.
- #infinite-loop
  - `while true; do ...; done` — must be terminated (e.g., `break` or Ctrl+C).
- #break
  - `break` : exit current loop immediately.
  - `break N` : exit N nested loops (bash supports numeric arg).
- #continue
  - `continue` : skip remainder of current iteration, proceed to next.
  - `continue N` : apply to Nth enclosing loop.
- Scope
  - `break`/`continue` valid inside `for`, `while`, `until`. (#do-done)

---

## Important Properties / Invariants
- Condition checked before entering each iteration (pre-check loop). (#while #until)
- Loop body is strictly between `do` and `done`. (#do-done)
- `while` runs while condition is true (exit status 0); `until` runs while condition is false (non‑zero).
- `continue` does not exit loop — it jumps to next condition evaluation.
- `break` terminates loop immediately and resumes after `done`.
- Use `Ctrl-C` to interrupt long or infinite loops manually. (#ctrl-c)
- When using test `[` or `(( ))`, ensure proper spacing and quoting for variables.

---

## Quick Reference (scannable)
Syntax:
- while:
  - `while <command>; do <commands>; done`
- until:
  - `until <command>; do <commands>; done`
- infinite:
  - `while true; do <commands>; done`  # use `break` or Ctrl+C to stop
- break / continue:
  - `break` / `break N`
  - `continue` / `continue N`

Common examples:
- Count up (while):
  - `i=1; while [ "$i" -le 10 ]; do echo $i; i=$((i+1)); done`
- Skip a value (continue):
  - `i=1; while [ $i -le 10 ]; do (( i==5 )) && { i=$((i+1)); continue; }; echo $i; i=$((i+1)); done`
- Break on condition:
  - `i=1; while true; do echo $i; (( i==8 )) && break; i=$((i+1)); done`
- Until example:
  - `i=1; until [ "$i" -gt 10 ]; do echo $i; i=$((i+1)); done`  (#runs while i <= 10)

Behavior checklist:
- Condition success = exit status 0 → treated as true.
- `while` executes when condition is true; `until` executes when condition is false.
- `do`/`done` required block markers.
- `break`/`continue` affect innermost loop unless numeric arg used.

---

Keep this sheet nearby when writing shell loops — copy common patterns and adjust conditions/tests accordingly.

---

## Module 9 — Lecture 89: Arrays in Bash — Declaration, Initialization, Access, and Operations

Keywords: #array #bash #declare #declare-a #indexing #slicing #iteration #keys #assignment #compound-assignment #heterogeneous #no-multidim #access

## Key Definitions
- Array: ordered collection of elements addressed by numeric indices. #array  
- Bash array: an array in Bash (can be heterogeneous; no built-in multidimensional arrays). #bash #heterogeneous #no-multidim  
- Index / key: integer position of an element (first index = 0). #indexing  
- Element: a single value stored at an index.  
- declare -a: explicitly declares a variable as an array. #declare  
- Compound assignment: assigning multiple elements at once using parentheses and optional explicit indices. #compound-assignment

## Formulas / Notation
- Indexing base: first element index = 0  
- Slice syntax (start,length): ${array[@]:start:length} — e.g., to get indices 2–4 use ${array[@]:2:3}  
- Time (common): access O(1), iterate O(n) (informational, not from transcript)

## Key Syntax & Examples (quick)
- Declare empty array:
  - declare -a arr
- Indexed assignment:
  - arr[0]=val
  - arr[3]=x
- Compound / list initialization:
  - arr=(a b c d)         # indexes 0..3
  - arr=( [0]=a [2]=c )   # explicit indices
- No spaces around assignment:
  - WRONG: arr = (a b)
  - RIGHT: arr=(a b)
- Access single element:
  - ${arr[2]}              # element at index 2
- First element shortcuts:
  - ${arr[0]} or ${arr}    # both yield first element
- All elements:
  - ${arr[@]} or ${arr[*]} # expand all elements
- Slice / range:
  - ${arr[@]:start:length} # e.g., ${arr[@]:2:3} -> indexes 2,3,4
- Keys / indices:
  - ${!arr[@]} or ${!arr[*]}  # list of indices (0-based)
- Iteration:
  - for v in "${arr[@]}"; do ...; done

## Key Algorithms / Concepts (bulleted)
- Declaration: use declare -a name to explicitly declare an array. #declare  
- Initialization methods:
  - Indexed assignment (arr[index]=value). #assignment  
  - Compound/list assignment (arr=(elem1 elem2 ...)). #compound-assignment  
- Access patterns:
  - Single element by index. #access  
  - All elements via @ or *. #access #slicing  
  - Range/slice via ${arr[@]:start:length}. #slicing  
  - Keys via ${!arr[@]}. #keys  
- Iteration: use for-loops over ${arr[@]}. #iteration  
- Variable index: use a variable as an index (e.g., i=2; echo ${arr[$i]}). #indexing

## Important Properties / Invariants
- Indexing starts at 0 (first element stored at index 0). #indexing  
- Bash arrays may contain mixed-type elements — no homogeneous-type requirement. #heterogeneous  
- Bash does not natively support multidimensional arrays. #no-multidim  
- Use declare -a to make intention explicit (not required but recommended). #declare  
- No spaces around the = when assigning arrays.  
- ${arr} (unindexed) is equivalent to ${arr[0]} in many contexts (first element). #access  
- ${arr[@]} vs ${arr[*]}: both expand all elements; behavior differs when quoted ( informational ). #access

## Quick Reference (scannable)
- declare array:
  - declare -a myarr
- init (list):
  - myarr=(1 2 3 4)
- init (indexed):
  - myarr[0]=1
  - myarr[4]=9
- print element i:
  - echo "${myarr[i]}"
- print first element:
  - echo "${myarr[0]}" or echo "${myarr}"
- print all elements:
  - echo "${myarr[@]}"    # or "${myarr[*]}"
- slice indices 2–4:
  - echo "${myarr[@]:2:3}"
- print all keys/indices:
  - echo "${!myarr[@]}"
- iterate:
  - for v in "${myarr[@]}"; do echo "$v"; done
- common mistakes:
  - Do not put spaces around = in assignments.
  - Expectation of multidimensional arrays — Bash does not support them natively.

Hashtags (major): #array #bash #declare #indexing #slicing #iteration #keys #assignment #compound-assignment #heterogeneous #no-multidim

(Use this sheet as a quick lookup for Bash array operations and common syntaxes.)

---

## Module 9 — Lecture 90: Bash Arrays — Advanced Operations (cheatsheet)

Keywords: #bash #array #arrays #indexing #length #slice #slicing #unset #append #+= #iteration #for-loop #indices #sparse

## Key Definitions
- Array: ordered collection of string values indexed by integers (in Bash). #array
- Index: integer position of element; first element is index 0. #indexing
- Length: number of elements currently present (not max index). #length
- Slice: contiguous subarray copied from an array. #slice
- Append: add element(s) to end of array using +=. #append
- Unset: remove a single element or entire array (using unset). #unset
- Sparse array: array with missing indices (after unset of elements). #sparse
- Indices list: list of present keys/indices (useful for iteration). #indices

## Formulas / Notation (Bash)
- Get number of elements: ${#arr[@]}  — returns length. #length
- Get all values: ${arr[@]}  — expands to all elements. #array
- Get all indices: ${!arr[@]}  — expands to present indices. #indices
- Access element i: ${arr[i]}  — value at index i. #indexing
- Slice (copy): new=( "${arr[@]:start:length}" )  
  - start = starting index (0-based).  
  - length = number of elements to copy. #slice
- Append elements: arr+=(val1 val2 ...)  #append
- Assign element: arr[index]=value  #indexing
- Remove element: unset arr[index]  — removes single element (creates hole). #unset
- Remove entire array: unset arr  — deletes array completely. #unset

## Key Algorithms / Concepts (quick bullets)
- Iteration over indices:
  - for i in "${!arr[@]}"; do echo "$i ${arr[$i]}"; done  — index + value. #for-loop #indices
- Iteration over values:
  - for v in "${arr[@]}"; do echo "$v"; done  — values only. #for-loop
- Append multiple items:
  - arr+=( "csh" "ksh" "zsh" )  — adds items to end. #+=
- Delete element vs delete array:
  - unset arr[3]  — delete element at index 3 (sparse result).  
  - unset arr     — delete whole array. #unset
- Slice semantics:
  - Slicing produces a new array copy; original array remains unchanged. #slice
- Zero-based indexing reminder:
  - First element = index 0. #indexing

## Important Properties / Invariants
- ${#arr[@]} counts present elements, not the largest index.
- unset arr[i] removes the element but does not reindex remaining elements (creates sparse indices).
- ${!arr[@]} only lists present indices (skip holes).
- Slicing uses start + length; order preserved; result is a separate copy.
- arr+=(...) appends at next numeric index (if numeric indices used).
- Assigning arr[index]=value can create non-contiguous indices.

## Quick Reference (syntax & examples)
- Declare/initialize:
  - arr=( "bash" "sh" "csh" "ksh" "zsh" )  #init
- Get length:
  - ${#arr[@]}  → e.g., 5
- Access:
  - ${arr[0]}  → first element ("bash")
- Iterate indices & values:
  - for i in "${!arr[@]}"; do echo "$i : ${arr[$i]}"; done
- Iterate values:
  - for v in "${arr[@]}"; do echo "$v"; done
- Append elements:
  - arr+=( "csh" "ksh" "zsh" )
- Delete element:
  - unset arr[3]  # removes index 3
- Delete whole array:
  - unset arr
- Slice (copy elements 0..1):
  - high_level=( "${arr[@]:0:2}" )  # copies arr[0] and arr[1]
- List indices present:
  - echo "${!arr[@]}"  # e.g., 0 1 2 4 7

Keep this sheet for quick lookup of common bash array operations and syntax.

---

## Module 9 — Lecture 91: Bash File Handling — Reading & Writing Cheatsheet

#keywords: #bash #file-handling #redirection #cat #read #while-loop #tee #stdout #input-redirection #append #overwrite #command-substitution

---

## Key Definitions
- cat: prints file(s) to stdout; can be used for command-substitution. #cat
- Redirection: changing where a command reads input from or writes output to. #redirection
- stdout: standard output stream (file descriptor 1). #stdout
- Input redirection `<`: supply a file as stdin to a command or loop. #input-redirection
- Output redirection `>`: write stdout to file (creates/overwrites). #overwrite
- Append redirection `>>`: append stdout to file (creates if missing). #append
- tee: writes stdin to both screen (stdout) and file. #tee
- Command substitution: capture command output into a variable, e.g. `var=$(cmd)` or faster `var=$(<file)`. #command-substitution
- while read loop: iterates file line-by-line using input redirection. #while-loop

---

## Formulas / Syntax (quick)
- Read whole file into variable:
  - `value=$(cat "file.txt")`  # uses cat
  - `value=$(< file.txt)`      # faster, no forked process
- Input redirection to a command:
  - `command < input.file`
- Line-by-line:
  - `while read line; do <commands>; done < input.file`
- Write output (overwrite):
  - `command > out.txt`
- Write output (append):
  - `command >> out.txt`
- tee (write & display):
  - `command | tee out.txt`
  - append with tee: `command | tee -a out.txt`

---

## Key Concepts / Usage (bulleted)
- #ReadingEntireFile
  - Use `cat` or command substitution to capture entire file content into a variable.
  - Prefer `$(< file)` for performance (no fork).
- #ReadingLineByLine
  - `while read line; do ...; done < file` — common pattern for processing each line.
- #WritingToFile
  - `>` creates file or overwrites existing file.
  - `>>` creates file or appends to existing file.
- #DisplayAndSave
  - `tee` lets you see output on terminal and save to file at same time.
  - `tee -a` appends instead of overwriting.
- #StdStreams (note)
  - Redirections above affect stdout by default. Use `2>` for stderr (not from transcript but useful).

---

## Important Properties / Invariants
- `>` overwrites file contents; existing data is lost.
- `>>` preserves existing content and appends new output.
- Using redirection (`>` / `>>`) sends command output to file only — nothing appears on terminal unless you also use `tee` or duplicate output streams.
- `while read` consumes stdin — use input redirection (`< file`) to feed a file rather than piping if you need the loop to read from the file.
- Command substitution `$(cmd)` executes cmd and captures its stdout; `$(< file)` is a shortcut that reads file directly without running `cat`.
- If target file does not exist, `>` and `>>` will create it.

---

## Quick Reference (scannable)
- Read file into var:
  - `v=$(cat "f")`  OR  `v=$(< f)`  ← faster
- Loop lines:
  - `while IFS= read -r line; do echo "$line"; done < file`
- Overwrite file:
  - `echo hi > out.txt`  (#creates or replaces)
- Append file:
  - `echo hi >> out.txt` (#creates or appends)
- Show and save:
  - `ls | tee list.txt`  (#prints and writes)
  - Append with tee: `cmd | tee -a file`
- Input redirection:
  - `cmd < input.file`
- Behavior summary table:

| Symbol/Command | Effect | Creates file? | Overwrites? | Shows on terminal? |
|---|---:|:---:|:---:|:---:|
| `>` | write stdout to file | yes | yes | no |
| `>>` | append stdout to file | yes | no (append) | no |
| `<` | feed file as stdin to command | n/a | n/a | n/a |
| `| tee file` | write stdout to file and stdout | yes | depends (tee vs tee -a) | yes |

---

Keep this sheet handy for quick commands and syntax during an open-book exam.

---

## Module 9 — Lecture 92: Shell Scripting Cheatsheet (Decision making, loops, arrays, I/O)

#hashtags: #shell #bash #scripting #if #elif #else #case #for #while #until #break #continue #arrays #string #test #comparison #redirection #fileio #slicing #patternmatching

---

## Key Definitions (one-liners)
- test / [ ] / [[ ]] — evaluate a condition (returns exit status 0 = true).  
- if / then / fi — single-decision block; ends with fi.  
- elif — else-if ladder (multiple mutually exclusive checks).  
- else — default branch for if / elif ladder.  
- case / esac — multi-pattern branch (like switch); patterns end with `;;`.  
- for in — iterate over a list or array elements.  
- C-style for — numeric loop form: arithmetic init/cond/inc.  
- while / until — looping constructs (until runs while condition is false).  
- break — exit the innermost loop.  
- continue — skip rest of current iteration and continue loop.  
- array — ordered collection of elements of same type in bash (declare -a).  
- redirection — `< file` (input), `>` (overwrite output), `>>` (append).  
- read — read a line from stdin (use `read -r` to avoid backslash escapes).  
- expr / $(( )) — arithmetic evaluation; prefer `$(( ))`.  
- pattern `|` in case — acts as OR between patterns; `*)` is default.

---

## Syntax & Quick Examples
- Variables: use `$var` to access; assignment: `var=value` (no spaces).
- if:
  - Single-line: `if [ condition ]; then command; fi`
  - Multi-branch:
    ```
    if [ cond1 ]; then
      ...
    elif [ cond2 ]; then
      ...
    else
      ...
    fi
    ```
  - Use `[[ ... ]]` when variables may contain spaces or for extended tests.
- case:
  ```
  case $var in
    pattern1) commands ;;
    pattern2|pattern3) commands ;;
    *) default ;;
  esac
  ```
- for-in:
  ```
  for item in a b c; do
    echo "$item"
  done
  ```
- C-style for:
  ```
  for ((i=1; i<=5; i++)); do
    echo $i
  done
  ```
- while / until:
  ```
  while read line; do
    ...
  done < file         # input redirection

  until [ condition ]; do
    ...
  done
  ```

---

## Comparison Operators (quick table)
- Integer comparisons (use with test/[ ] / [[ ]]):
  - -eq (==), -ne (!=), -gt, -ge, -lt, -le
- String comparisons:
  - `=` or `==` (in `[[ ]]`) — equal  
  - `!=` — not equal  
  - -z str — true if length is zero  
  - -n str — true if length is non-zero
- Boolean/exit status: test returns 0 for true, non-zero for false.
- Important: always include spaces around [ and ]: `[ "$a" -gt 10 ]`

---

## Arrays (bash)
- Declare: `declare -a arr` or `arr=(Java Python PHP)`
- Access:
  - All elements: `${arr[@]}` or `${arr[*]}`
  - Index: `${arr[2]}` (0-based)
  - Length (#elements): `${#arr[@]}`
  - String length of element: `${#arr[index]}`
- Append:
  - Single: `arr+=(JavaScript)`
  - Multiple: `arr+=("CSS" "SQL")`
- Insert by index: `arr[3]="JavaScript"`
- Delete:
  - Element: `unset 'arr[2]'`
  - Entire array: `unset arr`
- Slicing:
  - `${arr[@]:start:length}` e.g. `${arr[@]:1:3}`
  - Negative start counts from end (example: `${arr[@]: -3}` gives last 3 elements; note the space before negative offset in some shells)

---

## I/O & File Processing
- Input redirection to loop: `while read -r line; do ...; done < input.txt`
- Output redirection:
  - Overwrite: `cmd > file`
  - Append: `cmd >> file`
- Example: print even numbers from file:
  ```
  while read -r n; do
    if (( n % 2 == 0 )); then echo "$n"; fi
  done < integers.txt
  ```
- Prefer `$(( ))` for arithmetic: `(( i % 2 == 0 ))` or `res=$((i * i))`

---

## Break vs Continue (semantics)
- break — immediately exit the current loop (for/while/until).
- continue — skip remaining commands in current iteration and proceed to next iteration.

---

## Common Pitfalls / Important Properties
- Use spaces around brackets: `[ "$x" = "" ]` (missing spaces -> syntax error).
- `[ ... ]` vs `[[ ... ]]`:
  - `[[ ]]` is safer: supports pattern matching, `==` with glob, and avoids word-splitting for variables with spaces.
  - Use `[[ ]]` when variables may contain spaces or for advanced tests.
- Test return values: 0 = true, non-zero = false.
- In `if [ ... ]; then` you must place `;` or newline before `then`.
- In `case` patterns, separate alternatives with `|` and terminate commands with `;;`.
- When slicing negative offsets, some expansions require a space before the negative number: `${arr[@]: -3}`.
- Use `read -r` to avoid interpretation of backslashes.
- Prefer `$(( ))` over `expr` for clarity and reliability.

---

## Quick Reference (one-line cheats)
- Check integer: `[ "$a" -gt 10 ]`
- Check string empty: `[ -z "$s" ]`
- Check string non-empty: `[ -n "$s" ]`
- String equal: `[[ "$a" == "$b" ]]`
- If template: `if [[ cond ]]; then ... fi`
- Case template: `case $v in pat) ... ;; *) ... ;; esac`
- For-in: `for x in "${arr[@]}"; do ...; done`
- C-for: `for ((i=0;i<n;i++)); do ...; done`
- While-file: `while read -r line; do ...; done < file`
- Append to array: `arr+=(new)`
- Array all items: `${arr[@]}` ; length: `${#arr[@]}`
- Overwrite file: `> file` ; Append: `>> file`

---

Keep this sheet handy for syntax lookups in the exam — practice writing small scripts to internalize semicolons, `fi`/`done`/`esac` endings, and correct bracket spacing.

---

## Module 10 — Lecture 93: Processes & Process States (Linux) — Cheatsheet

# #process #program #Linux #process-life-cycle #process-states #foreground #background #scheduler #CPU #I/O #new #ready #running #waiting #blocked #terminated

---

## Key Definitions
- Program: an executable file on storage (machine code + data). #program  
- Process: an active/running instance of a program. #process  
- Process execution: the sequential progression of a process's instructions. #CPU  
- Foreground process: interactive process that depends on user input (e.g., editor). #foreground  
- Background process: non-interactive, runs independently (e.g., scheduler, daemons). #background  
- Scheduler: OS component that assigns ready processes to CPU(s). #scheduler

---

## Formulas / Notations
- Common life-cycle variants: 2-stage, 5-stage, 7-stage (this lecture uses 5-stage). #process-life-cycle  
- Typical 5-stage notation (compact): New → Ready → Running → Waiting/Blocked → Terminated

---

## Key Algorithms / Concepts
- Process life cycle (5 stages): defines states a process can occupy during its lifetime. #process-life-cycle  
- State transitions: created → queued → dispatched → blocked → resumed → exit. #process-states  
- Foreground vs Background operation: distinction used to control interactivity and resource handling. #foreground #background

---

## Important Properties / Invariants
- A process is tied to a program but represents runtime activity (context, registers, memory). #process  
- Execution is sequential (single instruction stream per process). #CPU  
- Only processes in Ready can be scheduled to Running; Running can become Waiting/Blocked if it needs I/O or resources. #ready #running #waiting #blocked  
- Waiting (blocked) means the process is stalled for some resource (keyboard, disk, network, etc.). #I/O  
- Terminated indicates process has finished and will be removed/cleaned up by OS. #terminated

---

## State Reference (5-stage)
| State | One-line meaning | Typical cause/example |
|---|---:|---|
| New | Process being created | exec/spawn system call |
| Ready | Waiting to be assigned to a processor | in scheduler queue |
| Running | Instructions executing on CPU | currently dispatched |
| Waiting / Blocked | Waiting for resource or event | disk I/O, keyboard input, network |
| Terminated | Finished execution; awaiting cleanup | exit/kill |

#new #ready #running #waiting #blocked #terminated

---

## Quick Reference (scannable)
- Start: execute program → process enters New. #program #new  
- New → Ready: creation complete, queued for CPU. #ready  
- Ready → Running: scheduler dispatches process to CPU. #scheduler #running  
- Running → Waiting/Blocked: requests I/O or resource; yields CPU. #I/O #blocked  
- Waiting → Ready: awaited resource becomes available; re-queued. #ready  
- Running → Terminated: process completes or is killed; resources freed. #terminated  
- Foreground = interactive (user input required) ; Background = non-interactive (runs autonomously). #foreground #background  
- Variants: some OSes use simplified 2-state or expanded 7-state models (same core ideas). #process-life-cycle

---

Use this sheet to quickly identify state names, transitions, and the difference between program vs process and foreground vs background operation.

---

## Module 10 — Lecture 94: Kernel vs User Mode — Cheatsheet

#kernel-mode #user-mode #context-switch #system-call #interrupt #trap #privileged-instruction #mode-bit #interrupt-handler #CPU #process #operating-system #kernel #user-space #memory #hardware

---

## Key Definitions
- Kernel mode: CPU mode with full access to hardware and all memory addresses; used by the OS/kernel.  
- User mode: Restricted CPU mode for user processes; no direct access to hardware or all RAM.  
- System call: Controlled request by a user process to the OS to access hardware or privileged services.  
- Context switch (mode switch): Transition of CPU execution between user mode and kernel mode.  
- Interrupt: Signal (hardware/software) that causes the CPU to stop current execution and transfer control to an interrupt handler.  
- Trap: Entering a special handler/state (often triggered by a system call) to switch to kernel mode.  
- Privileged instruction: CPU instructions only executable in kernel mode (e.g., direct I/O, change memory mappings).  
- Mode bit: CPU/status bit indicating current mode (0 = kernel, 1 = user).  
- Interrupt handler: Kernel routine that saves CPU state, services the interrupt/trap, and restores state.

---

## Formulas / Notation
- Mode bit: 0 → kernel mode, 1 → user mode  
- Context switch sequence (concise):  
  User process → system call → interrupt/trap → mode bit = 0 → save CPU state → execute kernel code → restore CPU state → mode bit = 1 → return to user process

---

## Key Concepts / Steps (quick bullets)
- #Boot: System starts in #kernel-mode at boot.  
- #Access: Kernel mode has direct access to all hardware & memory; user mode does not.  
- #SystemCall flow:
  - User calls API → kernel invoked via trap/interrupt → kernel executes request → returns result to user.  
- #ModeTransition:
  - Switch does NOT occur automatically; triggered by interrupt/trap (e.g., system call).  
- #SaveRestore:
  - Interrupt handler saves CPU registers/state before switching; restores before returning.  
- #PrivilegeEnforcement:
  - Only kernel mode can execute privileged instructions and access protected resources.

---

## Important Properties / Invariants
- User processes cannot execute privileged instructions nor access arbitrary physical memory.  
- Kernel must save full CPU state (registers, program counter, status/mode bit) before servicing and restore after.  
- Mode bit enforces protection barrier between user-space and kernel-space.  
- Context switching introduces overhead (must save/restore state and switch protection context).  
- Kernel is trusted authority for hardware access and resource management.

---

## Quick Reference (scannable)
- Mode bit mapping: 0 = kernel, 1 = user. #mode-bit  
- Boot mode: kernel mode. #boot #kernel-mode  
- Who can access hardware directly: Kernel only. #hardware #kernel-mode  
- How user accesses hardware: via system calls → kernel. #system-call  
- Trigger for mode switch: interrupt / trap generated (system call). #interrupt #trap  
- Interrupt handler duties: save CPU state → handle request → restore CPU state → set mode bit back. #interrupt-handler  
- Return to user: set mode bit = 1. #return  
- Common invariant: kernel must protect and isolate hardware/memory from user processes. #isolation

---

## Hashtag Index (for quick search)
#kernel-mode #user-mode #context-switch #system-call #interrupt #trap #mode-bit #interrupt-handler #privileged-instruction #CPU #process #kernel #user-space #memory #hardware

--- 
(Use this sheet to quickly locate mode mappings, transition steps, and the roles of kernel vs user modes during an exam.)

---

## Module 10 — Lecture 95: Process Creation & OS Services — Cheatsheet

#keywords: #process #processcreation #fork #systemcall #scheduling #memorymanagement #storagemanagement #security #protection #unix #linux #pid

## Key Definitions
- Process scheduling: selecting/removing processes on the CPU to manage execution order. #scheduling  
- Memory management: allocating & organizing main memory to maximize utilization and multiprogramming. #memorymanagement  
- Storage management: creating/deleting/formatting disk partitions and controlling user access. #storagemanagement  
- Protection & security: detecting/correcting resource errors and enforcing access/control. #security #protection  
- System call: privileged function request from a user process to the OS (interface between process & OS). #systemcall  
- Parent process: the process that calls fork to create a new process. #parent  
- Child process: the newly created process returned by fork and executed concurrently with the parent. #child

## Formulas / Syntax / Notation
- fork prototype: pid_t fork(void);  #fork #unix #linux  
- fork return semantics:
  - < 0 : error — child not created  
  - = 0 : running in child process  
  - > 0 : running in parent; value = child's PID (pid_t)

| fork() return | meaning |
|---------------|---------|
| < 0 | creation failed |
| 0  | in child process |
| > 0 | in parent; gives child's PID |

## Key Algorithms / Concepts
- Process Scheduling: OS selects another process to run when current process removed from CPU. #scheduling  
- Memory Management: supports multiprogramming by managing memory allocation and isolation. #memorymanagement  
- Storage Management: disk partition lifecycle and access control (create/delete/format). #storagemanagement  
- Protection & Security: OS responsibility to detect and correct resource errors and enforce safety. #security #protection  
- System Calls for processes: commonly used calls — fork, wait, exec, signal, kill, raise. #systemcall #fork #wait #exec #signal #kill #raise  
- fork behavior: creates child with separate memory space initialized with same content; parent & child execute concurrently. #fork #processcreation

## Important Properties / Invariants
- Concurrency: parent and child run concurrently after fork. #process  
- Memory separation: child and parent have different memory spaces; operations in one do not affect the other (initial contents same). #memorymanagement  
- fork is atomic with respect to process creation: returns differently in child vs parent. #fork  
- System calls are the controlled gateway to privileged OS operations. #systemcall

## Quick Reference (scannable)
- Common process-related syscalls: fork, wait, exec, signal, kill, raise. #fork #wait #exec #signal #kill #raise  
- fork usage pattern: parent forks → child (often) execs a new program → parent may wait for child. #fork #exec #wait  
- fork return check (C):
  - if (pid < 0) { /* error */ }  
  - else if (pid == 0) { /* child code */ }  
  - else { /* parent, pid = child PID */ }  
- Effects of fork:
  - CPU: both processes scheduled separately (#scheduling)  
  - Memory: separate address spaces (same initial content) (#memorymanagement)  
  - IPC/signaling needed for coordination between parent & child (#signal #kill)  
- OS responsibilities summary:
  - CPU scheduling — choose processes for CPU. #scheduling  
  - Memory management — allocation and isolation. #memorymanagement  
  - Storage management — partition & access control. #storagemanagement  
  - Protection & security — error handling & access enforcement. #security #protection

Keep this sheet handy for quick lookup of process creation semantics, core system calls, and the OS service responsibilities.

---

## Module 10 — Lecture 96: Fork (process creation) — Cheatsheet

#hashtags: #fork #systemcall #childprocess #parentprocess #PID #processcreation #processtree #multiprocessing #unix #linux

## Key Definitions
- fork(): Unix system call that creates a new process (one call returns twice). #fork #systemcall  
- Child process: The newly created process returned as 0 from fork(). #childprocess  
- Parent process: The original process which receives the child's PID (>0) from fork(). #parentprocess  
- PID (Process ID): Unique integer identifier for a process. #PID  
- Process tree: Hierarchy formed by parent/child relationships after forks. #processtree

## Formulas / Equations
- Number of processes after n unconditional forks: total = 2^n  (e.g., n=3 -> 8). #2^n #processcreation  
- If each process executes a single print, printed lines = 2^n.

## Key Algorithms / Concepts
- fork behavior:
  - fork() returns twice:
    - >0 in parent (value = child's PID)
    - 0 in child
    - -1 on error (no child created)
  - After fork both processes continue execution at the instruction after fork().
- Multiple fork calls: each fork in each existing process creates another child, causing exponential growth (doubling).
- Identifying processes: check fork() return value to distinguish parent vs child. #fork #childprocess #parentprocess

## Important Properties / Invariants
- fork() semantics:
  - Returns twice (parent & child). #fork
  - Parent receives child's PID (>0); child receives 0; negative means error.
  - Each fork doubles the number of processes if unconditional.
- Typical PID relationship: child has a different PID (often > parent PID), but ordering is OS-specific. #PID
- Without synchronization, order of output from parent/child is nondeterministic.
- Resource inheritance (common behavior):
  - Child inherits copies of parent's file descriptors, environment, and memory (copy-on-write in modern kernels). (Note: not detailed in lecture but typical Unix behavior.) #unix #linux

## Quick Reference
- fork() return values:
  - > 0 : parent — return value = child PID
  - 0   : child
  - -1  : error (fork failed)
- Process count:
  - n forks -> 2^n processes
  - Example: 3 forks -> 2^3 = 8 processes -> 8 prints if each prints once
- Typical usage pattern to distinguish:
  - if (fork() == 0) { /* child */ } else { /* parent */ }
- Common pitfalls:
  - Unconditional multiple forks -> exponential process explosion
  - No implicit wait -> children may become zombies if parent exits early (use wait()/waitpid() to avoid)
  - Output ordering is not deterministic between processes

## Example (summary from lecture)
- Single fork: prints "Hello world" twice (one from parent, one from child); cannot tell which printed without checking fork return.
- Three forks in sequence: yields 8 "Hello world" outputs (2^3).

Keep this sheet for quick lookup of fork return semantics, process count formula, and how to identify parent vs child.

---

## Module 10 — Lecture 97: Process coordination: parent/child, fork/wait/exec cheatsheet

#Keywords: #process #parent-child #fork #wait #waitpid #exec #execl #systemcall #orphan #ls

## Key Definitions (one-liners)
- Process: an executing program instance (address space + resources). #process  
- Parent process: the process that creates another via fork(). #parent-child  
- Child process: the new process created by fork(). #parent-child  
- fork(): system call that creates a child process (duplicate of parent). #fork  
- wait(): system call that makes a parent block until a child terminates. #wait  
- waitpid(): flexible wait allowing specific child selection and options. #waitpid  
- exec family: system calls that replace the current process image with a new program. #exec  
- execl(...): exec variant taking a path and a variable arg list (NULL-terminated). #execl  
- Orphan process: a child whose parent exited before it; adopted by init (or systemd). #orphan  
- System call: kernel-provided function invoked from user space. #systemcall

## Formulas / Signatures / Return semantics
- pid_t fork(void);
  - returns: >0 = child's PID (in parent), 0 = in child, -1 = error. #fork
- pid_t wait(int *status);
  - blocks until any child exits; returns child's PID, -1 on error. #wait
- pid_t waitpid(pid_t pid, int *status, int options);
  - can wait for specific child or use WNOHANG, etc. #waitpid
- int execl(const char *path, const char *arg0, ..., (char*)NULL);
  - on success: does not return; on error: returns -1 and sets errno. #execl #exec
- Exit status macros (from <sys/wait.h>):
  - WIFEXITED(status) — true if child exited normally.
  - WEXITSTATUS(status) — child's exit code (valid if WIFEXITED true).
  - WIFSIGNALED(status), WTERMSIG(status) — terminated by signal.

## Key Algorithms / Concepts (bulleted)
- Creating processes
  - Use fork() to create a child; both continue execution after fork. #fork
- Parent waiting for child
  - Use wait() to block until child finishes (prevents parent exiting early). #wait
  - Use waitpid() for non-blocking or targeting a PID (WNOHANG, WUNTRACED). #waitpid
- Running a different program in child
  - In child after fork, call an exec variant (execl, execv, execvp, etc.) to run a new program. #exec #execl
  - Example: child runs "ls -lh /home" via execl("/bin/ls", "ls", "-lh", "/home", (char*)NULL). #ls
- Parent/child lifecycle patterns
  - Parent waits -> child finishes -> parent continues.
  - Parent exits before child -> child becomes orphan (adopted by init). #orphan

## Important Properties / Invariants
- After fork:
  - Two processes exist with identical memory image (copy-on-write semantics usually). #fork
  - Distinguish by fork() return value: 0 in child, >0 in parent. #fork
- Exec semantics:
  - Exec replaces the calling process image; file descriptors may persist (unless O_CLOEXEC). #exec
  - On success exec() does not return; on failure returns -1 and sets errno. #execl
- Wait semantics:
  - wait() reaps terminated child and returns its PID and status; without wait, terminated child becomes a zombie until reaped. #wait
- Orphans:
  - Orphaned children are adopted by init (or equivalent), not automatically terminated. #orphan

## Quick Reference (scannable)
- Common fork/wait/execl pattern:
  - pid_t pid = fork();
    - if (pid < 0) -> error
    - if (pid == 0) { /* child */ execl("/bin/ls", "ls", "-lh", "/home", (char*)NULL); /* on error: exit */ }
    - else { /* parent */ wait(NULL); /* or waitpid(pid, &status, 0); */ }
- execl usage:
  - execl(path, argv0, arg1, ..., (char *)NULL);
  - argv0 conventionally set to program name (e.g., "ls"). #execl
- wait vs waitpid:
  - wait(NULL) -> block for any child.
  - waitpid(pid, &status, 0) -> block for specific child.
  - waitpid(pid, &status, WNOHANG) -> non-blocking.
- Exit/status handling:
  - if (WIFEXITED(status)) code = WEXITSTATUS(status);
  - if (WIFSIGNALED(status)) sig = WTERMSIG(status);
- Avoiding zombies:
  - Parent must call wait/waitpid (or set SIGCHLD handler with SIG_IGN on some systems).
- Common pitfalls:
  - Forgetting (char*)NULL terminator in execl -> undefined call behavior.
  - Calling exec in parent accidentally (do exec only in child).
  - Assuming exec returns; always check return for -1 (error).

## Short examples
- Run ls in child, parent waits:
  - pid = fork();
  - if (pid == 0) execl("/bin/ls","ls","-lh","/home",(char*)NULL);
  - else wait(NULL);

#Hashtags (all major items): #process #parent-child #fork #wait #waitpid #exec #execl #systemcall #orphan #ls

(Use this as a quick lookup during exam: signatures, return rules, common call patterns, and essential macros.)

---

## Module 10 — Lecture 98: Signals & Signal Handlers (Linux) — Cheatsheet

Keywords: #signal #signalhandler #linux #IPC #asynchronous #SIGINT #CtrlC #maskable #nonmaskable #raise #kill #signal_system_call #sleep

---

## Key Definitions
- Signal: A software interrupt used to announce asynchronous events to a process. #signal
- Signal handler: A user-provided function that executes when a process receives a signal. #signalhandler
- Maskable signal: A signal the process/user can catch, change, or ignore (e.g., Ctrl+C / SIGINT). #maskable
- Non-maskable signal: A signal that cannot be changed or ignored (usually hardware/non-recoverable errors). #nonmaskable
- Default action: The kernel's default behavior for a signal (e.g., terminate on SIGINT). #default_action

---

## Formulas / Function Signatures
- Register handler:
  - signal(int signum, void (*handler)(int));
  - or typedef: sighandler_t signal(int signum, sighandler_t handler);
- Handler prototype:
  - void sig_handler(int signum);
- Send signals:
  - int raise(int sig);           // send signal to calling process
  - int kill(pid_t pid, int sig); // send signal to specified process
- Sleep used to throttle loops:
  - unsigned sleep(unsigned seconds);

---

## Key Algorithms / Concepts
- Signal delivery: asynchronous — process execution is interrupted, handler runs, then control returns. #asynchronous
- Registering a handler: pass function pointer as second argument to signal() in main. #signal_system_call
- Common interactive signal: Ctrl+C → SIGINT → default action: terminate (can be caught). #SIGINT #CtrlC
- Programmatic signaling: use raise() for self, kill() to send to other processes. #raise #kill
- Use sleep(1) in loops to avoid CPU hogging when waiting for signals. #sleep

---

## Important Properties / Invariants
- Signals are asynchronous and can interrupt at almost any point of execution. #asynchronous
- Maskable vs Non-maskable:
  - Maskable: user can install handler or ignore. #maskable
  - Non-maskable: cannot be changed/ignored (OS/hardware-level). #nonmaskable
- Handler invocation:
  - Kernel invokes handler when signal delivered.
  - Handler runs immediately (preempts normal flow) and typically receives an int signum. #signalhandler
- Registration effect:
  - signal(signum, handler) sets handler for signum until changed or process exits. #signal_system_call
- Default behavior for SIGINT from terminal: terminate the process unless caught. #SIGINT

---

## Quick Reference (Scannable)
- Common signal constants: SIGINT (Ctrl+C), others exist (SIGTERM, SIGKILL*, SIGSTOP*). (*SIGKILL/SIGSTOP are non-catchable)
- Register handler:
  - Example: signal(SIGINT, sig_handler);
  - Handler signature: void sig_handler(int signum);
- Send signal:
  - From keyboard: Ctrl+C → kernel sends SIGINT to foreground process. #CtrlC
  - From code: raise(SIGINT); or kill(pid, SIGINT);
- System call prototypes:
  - signal(int signum, void (*handler)(int));
  - int raise(int sig);
  - int kill(pid_t pid, int sig);
  - unsigned sleep(unsigned seconds);
- Best practices (quick):
  - Keep handlers short and async-signal-safe.
  - Use sleep or blocking calls to avoid busy-wait loops consuming CPU. #sleep
- Observed behavior:
  - Handler output appears before control returns to main loop (handler runs immediately).

---

Tags (all major items): #signal #signalhandler #linux #IPC #SIGINT #CtrlC #maskable #nonmaskable #raise #kill #signal_system_call #sleep #asynchronous

--- 

(Use this sheet to quickly find signal registration, sending, and basic properties during an exam.)

---

## Module 10 — Lecture 99: Signals (raise / kill) — Cheatsheet

#hashtags: #signals #raise #kill #signal_handler #SIGUSR1 #SIGQUIT #signal_h #signal #process #pid #process_group #interprocess #intraprocess #signal()

---

## Key Definitions
- Signal: asynchronous notification sent to a process to notify it of an event. #signals
- raise(sig): send signal sig to the calling process (self). #raise
- kill(pid, sig): send signal sig to process identified by pid or to a process group. #kill
- signal(handler): register a signal handler for a given signal number. (#signal) #signal()
- Signal handler: function invoked when a process receives a signal, typically prototype void handler(int). #signal_handler
- SIGUSR1: user-defined signal with no predefined meaning. #SIGUSR1
- SIGQUIT: user-generated quit signal (default: terminate + core dump unless handled). #SIGQUIT
- pid (pid_t): process identifier used as target for kill. #pid #process

---

## Function Prototypes / Equations
- #signal_h
  - int raise(int sig);
  - int kill(pid_t pid, int sig);
  - typedef void (*sighandler_t)(int);
  - sighandler_t signal(int sig, sighandler_t handler);

- Return values:
  - raise(): returns 0 on success, non-zero on failure.
  - kill(): returns 0 on success, -1 on error (errno set).  

---

## Key Algorithms / Concepts
- raise (intra-process)
  - Usage: raise(SIGUSR1); — sends signal to calling process (self). #raise #intraprocess
- kill (inter-process / process-group)
  - Usage: kill(pid, SIGQUIT); — sends SIGQUIT to process pid. #kill #interprocess
  - Can target process groups using special pid values (see Quick Reference). #process_group
- signal registration
  - Register handler in process: signal(SIGQUIT, sig_handler); #signal()
  - Handler executed when signal delivered; handler can print and return or call _exit/exit. #signal_handler
- Parent-child signaling example
  - Parent calls kill(child_pid, SIGQUIT); child had registered handler and runs it on receipt. #SIGQUIT

---

## Important Properties / Invariants
- Delivery target:
  - raise() → calling process only. #raise
  - kill(pid>0) → process with id pid; kill(0) → all processes in sender’s process group; kill(<0) → send to process group |pid|; kill(-1) → all processes (subject to permission). #kill #process_group
- Signals are asynchronous and handled in process context.
- Some signals cannot be caught/ignored (e.g., SIGKILL, SIGSTOP). Handlers not invoked for those. #signals
- Handlers receive signal number as single int parameter: void handler(int sig). #signal_handler
- Default actions vary by signal (terminate, ignore, stop, core dump). #signals
- A signal sent to a process with a handler will cause handler execution; if unhandled, default action occurs. #signal_handler

---

## Quick Reference (scannable)
- Header: #include <signal.h> (#signal_h)
- raise:
  - Prototype: int raise(int sig);
  - Target: calling process
  - Return: 0 success, non-zero failure
  - Example: raise(SIGUSR1); #raise #SIGUSR1
- kill:
  - Prototype: int kill(pid_t pid, int sig);
  - Return: 0 success, -1 on error (errno)
  - Common pid values:
    - pid > 0 → that process only
    - pid == 0 → all processes in sender’s process group
    - pid < 0 → all processes in process group |pid|
    - pid == -1 → all processes (subject to permissions)
  - Example: kill(child_pid, SIGQUIT); #kill #SIGQUIT
- signal():
  - Prototype: void (*signal(int sig, void (*handler)(int)))(int);
  - Register: signal(SIGQUIT, sig_handler);
  - Handler prototype: void sig_handler(int sig);
- Signals mentioned:
  - SIGUSR1 — user-defined, no special kernel meaning. #SIGUSR1
  - SIGQUIT — user quit, default: terminate + core dump (catchable). #SIGQUIT
- When to use:
  - Use raise() for self-signaling within same process. #intraprocess
  - Use kill() for signaling other processes / process groups. #interprocess

---

Keep this sheet handy for quick lookup of function prototypes, return semantics, and common pid behaviors for raise() and kill().

---

## Module 10 — Lecture 100: System Call vs Function Call — Cheatsheet

#keywords: #systemcall #functioncall #kernel #user_mode #kernel_mode #contextswitch #IO #interprocesscommunication #privilege #syscall_instruction #software_interrupt #sysenter #blocking #nonblocking #syscall_examples #function_examples

---

## Key Definitions
- System call: A kernel-provided interface that lets a program request services from the OS (enters kernel mode). #systemcall #kernel  
- Function call: A user-mode invocation of a subroutine/procedure/method within the same program (no mode switch). #functioncall  
- Kernel mode: CPU privilege level where OS code can access protected resources/hardware. #kernel_mode #privilege  
- User mode: Lower privilege level where application code runs and cannot directly access hardware. #user_mode  
- Context switch (mode switch): Transition between user mode and kernel mode (or between processes/threads). #contextswitch

---

## Formulas / Notation
- Mode transition sequence: user code -> trap/syscall -> kernel handler -> return -> user code  
- Cost relation: T_function_call << T_system_call (function calls are much cheaper)  
- Rough decomposition for syscall latency:
  T_syscall ≈ T_user_call_overhead + T_trap + T_kernel_handler + T_return + (optional) T_scheduler
- Syscall invocation mechanisms: software interrupt (e.g. int 0x80), SYSENTER/SYSEXIT, SYSCALL/SYSRET. #software_interrupt #sysenter #syscall_instruction

---

## Key Algorithms / Concepts
- System call usage:
  - Services: file IO, device IO, process control, interprocess communication, memory management. #IO #interprocesscommunication  
  - Examples: open, read, write, close, fork, exec, wait, mmap, ioctl, kill. #syscall_examples
- Function call characteristics:
  - Local routines, library functions, user-defined functions (e.g., printf, strlen) executed in user mode. #function_examples
- Control flow:
  - Function call: call -> push args/regs/frame -> execute -> return  
  - System call: call user stub -> trap to kernel -> kernel executes -> return to user
- Privilege boundary:
  - Syscalls cross security/privilege boundary; arguments validated by kernel. #privilege #security

---

## Important Properties / Invariants
- Mode switch:
  - System call causes user->kernel->user transitions; function call does not. #contextswitch
- Resource access:
  - Only kernel (via system calls) can access protected resources/hardware. #kernel #IO
- Overhead:
  - System calls add significant latency and cannot be inlined/optimized away by compiler; function calls can be optimized (inline, tail-call). #performance
- Blocking behavior:
  - Many syscalls may block (sleep) and involve scheduler; function calls run until completion in same thread. #blocking #nonblocking
- Error reporting:
  - Syscalls return status/errno from kernel; function calls return per language convention. #syscall
- Safety:
  - Arguments to syscalls must be validated by kernel — user pointers cannot be trusted. #security

---

## Quick Reference (Scannable)
- When to use:
  - Use a system call to request OS services or access hardware. #systemcall  
  - Use a function call for algorithmic/subroutine work inside the process. #functioncall
- Examples:
  - System calls: open, read, write, fork, exec, mmap, ioctl. #syscall_examples  
  - Function calls: printf, sqrt, user_defined_func. #function_examples
- Performance checklist:
  - Need low latency? Prefer function call. #performance  
  - Need OS resource? Must use system call. #kernel
- Invocation methods (x86-ish):
  - Legacy: int 0x80 (software interrupt) #software_interrupt  
  - Fast: sysenter/sysexit or syscall/sysret #sysenter #syscall_instruction
- Security:
  - Syscall = privilege boundary -> kernel validation required. #privilege #security
- Typical flow (short):
  - Function call: push args -> call -> execute -> ret  
  - Syscall: user stub -> trap -> kernel handler -> return to user

---

## Comparison Table

| Aspect | System Call (#systemcall) | Function Call (#functioncall) |
|---|---:|---|
| Mode | Kernel mode (after trap) #kernel_mode | User mode only #user_mode |
| Purpose | Access OS services/hardware #IO | Execute user-defined routines |
| Context switch | Yes (user↔kernel) #contextswitch | No |
| Overhead | High (mode switch + kernel work) #performance | Low (stack/regs only) |
| Blocking | May block and invoke scheduler #blocking | Runs in-thread (no scheduler involvement) |
| Examples | open, read, write, fork #syscall_examples | printf, sum(), helper() #function_examples |
| Optimizable by compiler | No | Yes (inline, tail-call) |

---

Keep this sheet near your notes for quick lookup during an open-book exam.

---

## Module 10 — Lecture 101: Processes, Lifecycle, fork/exec, wait, and Signals — Cheatsheet

#hashtags: #process #process-lifecycle #PCB #fork #exec #wait #waitpid #signals #kill #raise #zombie #stack #heap #malloc #calloc #realloc #scheduling #ready-queue #interrupt #multitasking #multiprocessing #shell

---

## Key Definitions (one-line)
- Process: A program in execution (code + data + state + resources). #process  
- PCB (Process Control Block): Metadata for a process (PID, state, registers, memory map, etc.). #PCB  
- Program Counter: Pointer to next instruction to execute. #program-counter  
- Stack: LIFO memory region for function frames, return addresses, local variables. #stack  
- Heap: Dynamic memory region allocated at runtime (malloc/calloc/realloc). #heap #dynamic-memory  
- Process states: new, ready, running, waiting (blocked), terminated (exit). #process-lifecycle  
- Fork: System call to duplicate current process; creates child process (copy). #fork  
- Exec: Family of calls that replace current process image with a new program (PID unchanged). #exec  
- Wait / waitpid: Calls to block parent until child terminates (wait = any child, waitpid = specific PID). #wait #waitpid  
- Signal: Asynchronous notification of an event (interrupt/error) to a process. #signals  
- Signal handler: A function registered to handle a specific signal. #signal-handler  
- Kill: Send a signal to another process or process group (inter-process). #kill  
- Raise: Send a signal to the calling process itself (intra-process). #raise  
- Zombie: Child process that has exited but still has an entry in the process table because parent hasn't collected its exit status. #zombie  
- Daemon/background process: Runs without direct user interaction; foreground interacts with user. #daemon #background #foreground

---

## Formulas / Return-value rules (quick)
- fork():
  - returns 0 in child
  - returns child PID (>0) in parent
  - returns -1 on error
- exec*(): on success — does not return (replaces process image); on error — returns -1 and errno set.
- wait(&status): returns PID of terminated child or -1 on error; status contains termination info.
- waitpid(pid,...): waits for specific pid (or options); returns PID or -1.
- Common signal numbers (mentioned):
  - SIGINT = 2 (Ctrl+C) #SIGINT
  - SIGKILL = 9 (force kill, cannot be caught) #SIGKILL
  - SIGTERM = 15 (polite termination) #SIGTERM

---

## Key Algorithms / Concepts (bulleted)
- Process creation & PCB initialization:
  - OS allocates PCB, assigns unique PID, allocates resources, places process in ready queue. #PCB #scheduling
- Scheduling:
  - Scheduler chooses which ready process gets CPU time (ready queue). #scheduling #ready-queue
- fork-based concurrency:
  - Parent forks child; both run concurrently; commonly used by shells and servers. Example: shell uses fork + exec for background tasks (&). #fork #shell
- fork vs exec:
  - fork: duplicates process (new PID); exec: replaces process image (same PID). #fork #exec
- Server model with fork:
  - Parent listens; on client connect -> fork child to handle client; parent continues listening. #multiprocessing
- wait vs waitpid:
  - wait(): block until any child terminates.
  - waitpid(pid,...): block until specified child terminates (or use options). #wait #waitpid
- Zombie avoidance:
  - Parent must call wait/waitpid to collect child's exit status; otherwise child becomes zombie. #zombie
- Signals & handlers:
  - Register handler via signal()/sigaction(); when signal arrives, handler is invoked (unless signal is uncatchable, e.g., SIGKILL). #signals #signal-handler
- kill vs raise:
  - kill(pid, sig): send sig to other process/process group (inter-process).
  - raise(sig): send sig to calling process itself (intra-process). #kill #raise

---

## Important Properties / Invariants
- PID uniqueness: each active process has a unique PID. #PID  
- PCB always contains process state; switching updates PCB (context switch). #PCB  
- Stack frames obey LIFO; local variables are transient (valid only while frame active). #stack  
- Heap allocations occur at runtime; free them to avoid leaks. #heap #malloc #free  
- Process state transitions: new → ready → running → (waiting ↔ ready) → terminated. #process-lifecycle  
- A running process only goes to waiting when it needs I/O/event (interrupt); otherwise remains ready/running. #interrupt  
- exec never changes PID; fork always creates new PID. #fork #exec  
- SIGKILL cannot be caught/handled or ignored; SIGTERM can be handled for graceful shutdown. #signals #SIGKILL #SIGTERM

---

## Quick Reference (scannable)
- Process components: Text/code | Data (globals) | Heap (dynamic) | Stack (local/return addresses) | PCB. #stack #heap #PCB
- Process states: new, ready, running, waiting (blocked), terminated. #process-lifecycle
- fork() behavior:
  - child: return 0
  - parent: return child_PID > 0
  - error: -1
- exec*() behavior:
  - replaces image, keeps PID; on success never returns; on failure returns -1. #exec
- wait() vs waitpid():
  - wait(&status): waits for any child
  - waitpid(pid, &status, options): waits for specified child
- Zombie process:
  - cause: parent didn’t call wait/waitpid for exited child
  - cure: parent collects exit status (wait/waitpid) or parent exits (init adopts & reaps)
- Signals:
  - register handler: signal(sig, handler) or sigaction
  - common: SIGINT(2), SIGTERM(15), SIGKILL(9), SIGFPE (floating-point error)
- kill(pid, sig):
  - to gracefully ask process to terminate: kill(pid, SIGTERM)
  - to force: kill(pid, SIGKILL)
- raise(sig):
  - self-send: equivalent to kill(getpid(), sig) but restricted to same process
- Shell background (&):
  - shell forks child; child execs program; shell (parent) continues accepting commands. #shell
- Server fork model:
  - parent listens; fork on accept; child handles connection; parent continues listen. #multiprocessing

---

Keep this sheet for quick lookup of behavior, return values, and the differences: fork vs exec, wait vs waitpid, kill vs raise, and how to avoid zombies. Good luck on the exam.

---

## Module 11 — Lecture 102: Low-level File I/O (Linux) — Cheatsheet

#hashtags: #LowLevelIO #FileIO #Linux #open #close #read #write #filedescriptor #O_RDONLY #O_WRONLY #O_RDWR #O_CREAT #streamIO #HighLevelIO

---

## Key Definitions
- Low-level I/O: direct system-call I/O on file descriptors; faster, programmer-managed buffers. #LowLevelIO  
- High-level (stream) I/O: library-level buffered I/O (e.g., printf, fopen); more convenient, slower. #HighLevelIO #streamIO  
- File descriptor (fd): integer handle returned by open() identifying an open file. #filedescriptor  
- Flags: integer bitmask passed to open() to control access mode and behavior. #O_RDONLY #O_WRONLY #O_RDWR #O_CREAT  
- Mode: permission bits used when creating a file (third arg to open). #mode

---

## Formulas / Return values
- open signature (POSIX/C): int open(const char *pathname, int flags, mode_t mode); #open  
- close signature: int close(int fd); #close  
- Typical return semantics:
  - open: returns nonnegative file descriptor on success; returns -1 on error (and sets errno). #open  
  - close: returns 0 on success; returns -1 on error (and sets errno). #close  
  - (Transcript simplified errors as "1" for close-failure — POSIX uses -1.) Note: use errno for error details.  

---

## Key Concepts / Functions
- open
  - Purpose: open existing file or create new file; returns fd. #open
  - Args: filename (string), flags (int), mode (int, for creation). #mode
  - On success: file offset set to 0 (beginning).  
- close
  - Purpose: close an open file identified by fd; releases descriptor. #close
  - Arg: file descriptor (int).  
- read / write
  - Low-level I/O syscalls that operate on file descriptors to read/write byte buffers. #read #write
- Buffer management
  - Low-level I/O: programmer must manage buffers and I/O sizes; no automatic stdio buffering.  

---

## Common Flags (open)
| Flag | Meaning | #hashtag |
|---|---:|---|
| O_RDONLY | Open for read-only | #O_RDONLY |
| O_WRONLY | Open for write-only | #O_WRONLY |
| O_RDWR | Open for read & write | #O_RDWR |
| O_CREAT | Create file if it does not exist (requires mode) | #O_CREAT |

(Flags are bitwise combinable, e.g., O_WRONLY | O_CREAT)

---

## Important Properties / Invariants
- Linux treats devices and files uniformly: both accessed via file descriptors. #Linux  
- File descriptor uniquely identifies an open file table entry within a process. #filedescriptor  
- After open, file offset = 0 unless other flags/behaviors adjust it.  
- Must close every fd you open to avoid descriptor leaks. #close  
- Low-level I/O is typically faster than stdio but less convenient. #LowLevelIO #HighLevelIO

---

## Quick Reference
- Syntax:
  - open: int fd = open("path", flags, mode);
  - close: int r = close(fd);
  - read/write: ssize_t n = read(fd, buf, count); ssize_t m = write(fd, buf, count); #read #write
- Return values:
  - open: fd >= 0 → success; -1 → error (check errno).
  - close: 0 → success; -1 → error (check errno).
- Common errors: EACCES, ENOENT (open), EBADF (close/read/write with bad fd). (Check errno)  
- When using O_CREAT supply mode (e.g., 0644) for file permissions.  
- Combine flags with bitwise OR: open(path, O_WRONLY | O_CREAT, 0644);

---

## Minimal Example (reference)
- Open, do I/O, close:
  - int fd = open("file.bin", O_RDWR | O_CREAT, 0644);
  - if (fd < 0) /* handle error */;
  - ssize_t n = read(fd, buf, bufsize);
  - /* write(fd, buf2, len); */
  - close(fd);

---

Use this sheet to quickly locate syntax, flags, return conventions, and the differences between low-level and high-level file I/O in Linux.

---

## Module 11 — Lecture 103: File I/O: read, write, and random access (#fileio #read #write #lseek #filedescriptor #sequentialaccess #randomaccess #EOF #error #systemcall)

## Keywords
#fileio #read #write #lseek #filedescriptor #buffer #sequentialaccess #randomaccess #record #EOF #error #systemcall #SEEK_SET #SEEK_CUR #SEEK_END

---

## Key Definitions
- File descriptor: integer handle returned by open() used to identify an open file. #filedescriptor  
- read(): system call to read bytes from a file starting at current file position. #read  
- write(): system call to write bytes into a file starting at current file position. #write  
- lseek(): low-level call to change (seek) the current file position for random access. #lseek #randomaccess  
- Sequential access: reading/writing occurs in-file order (one after another). #sequentialaccess  
- Random access: non-sequential read/write of file contents (by records/offsets). #randomaccess  
- EOF: end-of-file indicator (read returns 0 bytes). #EOF  
- Error return: read/write return -1 on error. #error

---

## Function Signatures / Formulas
- read(fd, buf, count) -> returns number of bytes read (integer).  
- write(fd, buf, count) -> returns number of bytes written (integer).  
- lseek(fd, offset, whence) -> sets/returns file offset. #SEEK_SET #SEEK_CUR #SEEK_END

Canonical types (common POSIX):
- ssize_t read(int fd, void *buf, size_t count)  
- ssize_t write(int fd, const void *buf, size_t count)  
- off_t lseek(int fd, off_t offset, int whence)

Return semantics:
- read() returns >0: bytes read  
- read() returns 0: EOF reached (#EOF)  
- read() returns -1: error (#error)  
- write() returns >=0: bytes written  
- write() returns -1: error (#error)

---

## Key Concepts / Operations
- #SequentialAccess
  - read/write operate from the current file position and advance it.
- #RandomAccess
  - Use lseek() to change file position before read/write (record-based access).
- #Buffers
  - read fills a provided buffer; write consumes bytes from a provided buffer.
- #ReturnValues
  - Check returned byte counts to verify I/O success or detect EOF/errors.
- #SystemCalls
  - read/write/lseek are low-level system calls (unbuffered at user-level).

---

## Important Properties / Invariants
- File position is shared per file descriptor and moves forward by the number of bytes read/written. #fileposition  
- read/write require: (fd, buffer, byte-count). Order is consistent across both calls. #API  
- read returning 0 means no more data (EOF); -1 indicates an error. #EOF #error  
- write returns the actual bytes written; check for short writes (verify return). #write  
- lseek allows non-sequential access using offsets and whence constants. #lseek

---

## Quick Reference (scannable)
- Usage patterns:
  - Read: read(fd, buf, nbytes) → bytes_read
  - Write: write(fd, buf, nbytes) → bytes_written
  - Seek: lseek(fd, offset, SEEK_SET|SEEK_CUR|SEEK_END) → new_offset
- Return checks:
  - if (ret == 0) → EOF (for read)  
  - if (ret == -1) → error (check errno)  
  - if (ret < requested) → partial transfer (handle appropriately)
- Common whence values:
  - SEEK_SET = set offset to offset  
  - SEEK_CUR = set offset to current + offset  
  - SEEK_END = set offset to end + offset
- Typical param order: (fd, buffer, size) for both read/write.
- When to use:
  - Use sequential read/write for streaming/append operations. #sequentialaccess  
  - Use lseek for record-oriented or random-access reads/writes. #randomaccess

---

Tags summary: #fileio #read #write #lseek #filedescriptor #sequentialaccess #randomaccess #EOF #error #systemcall #buffer #record #SEEK_SET #SEEK_CUR #SEEK_END

---

## Module 11 — Lecture 104: Linux System Administration — Advanced Commands (cheatsheet)

Keywords: #linux #unix #root #administrator #privilege #sudo #su #useradd #userdel #passwd #wall #ulimit #cron #ssh #ftp #/etc/passwd #/etc/shadow #/etc/group #/etc/gshadow #systemadmin

## Key Definitions
- #root: Highest-privilege administrator account (UID = 0).  
- #sudo: "super user do" / "switch user do" — run a command with elevated (usually root) privileges without logging in as root.  
- #su: Switch user / become root by supplying the target account's password (often root password).  
- #useradd: Command to create a new user account (requires root/sudo).  
- #passwd: Set/change a user's login password (requires root/sudo to change another user).  
- #userdel: Delete a user account (requires root/sudo).  
- #wall: Broadcast a message to all logged-in users (root-only by default).  
- #ulimit: Per-user resource limits (max file size, processes, etc.).  
- #cron: Scheduler service for per-user/system jobs (access controllable by root).  
- /etc/passwd: User account info (username, UID, GID, home, shell).  
- /etc/shadow: Encrypted passwords and password policy data.  
- /etc/group: Group membership info.  
- /etc/gshadow: Secure group passwords/membership.

## Formulas / Notes
- Root UID = 0 (root is identified by UID 0).  
- Logging: #sudo and #su operations are typically logged (audit trail for privileged commands).  
- No algorithmic formulas in this lecture.

## Key Commands / Concepts (quick bullets)
- su
  - Become another user (commonly `su` or `su -`) — requires target user's password (#su).
- sudo
  - Run single command as root or another user, can use invoking user's password if configured (#sudo).
  - Safer than logging in as root; supports fine-grained permission via /etc/sudoers.
- wall
  - Broadcast text to all logged-in users (root-only usually).
  - Example: `sudo wall "Server will shut down at 17:00"`
- useradd
  - Create a user; adds entries to `/etc/passwd`, `/etc/shadow`, `/etc/group`, `/etc/gshadow`.
  - Requires root/sudo (#useradd).
- passwd
  - Set or change a user's password. Example: `sudo passwd username` (#passwd).
- userdel
  - Delete a user account. Example: `sudo userdel username` (#userdel).
  - Common options: `-r` remove home and mail spool, `-f` force delete, `-h` help.
- ulimit
  - Set maximum resource usage for user processes (file size, number of processes, stack size) (#ulimit).
- cron
  - Root controls which users can use cron; system and per-user scheduled tasks (#cron).
- Networking services
  - Root controls access/config of network services (e.g., #ssh, #ftp).

## Important Properties / Invariants
- Any operation that installs, removes, modifies system software or protected system files requires root privileges.  
- Root can:
  - Change file attributes and contents regardless of file-level protections.  
  - Delete files inside protected directories.  
  - Change any user's password without knowing the old one.  
  - Set system clock/date.  
  - Control access to scheduling, resource limits, and network services.
- sudo vs su:
  - su requires target account password (usually root).  
  - sudo can be configured to use the invoking user's password and can limit allowed commands; useful for auditing and least privilege.
- Auditing:
  - Use sudo (and proper syslog/audit) to keep a record of privileged actions.

## Quick Reference (scannable)
- File locations:
  - `/etc/passwd` — user account fields  
  - `/etc/shadow` — encrypted passwords  
  - `/etc/group` — group memberships  
  - `/etc/gshadow` — group secure info
- Common commands (syntax)
  - Create user: `sudo useradd <username>`  (#useradd)  
  - Set password: `sudo passwd <username>`  (#passwd)  
  - Delete user: `sudo userdel <username>` or `sudo userdel -r <username>`  (#userdel)  
  - Become root: `su -` (needs root password)  (#su)  
  - Run single command as root: `sudo <command>`  (#sudo)  
  - Broadcast message: `sudo wall "message"`  (#wall)  
  - Set/check ulimit: `ulimit -a` / `ulimit -n <value>`  (#ulimit)
- userdel options:
  - `-r` remove home and mail, `-f` force, `-h` help
- Best practices:
  - Prefer `sudo` over direct root login.  
  - Restrict sudoers to necessary commands.  
  - Ensure auditing/logging of privileged commands.
- Tasks requiring root (quick list):
  - Install/update software, modify system dirs, change other users' passwords, set system time, control cron, change networking service configs, broadcast using wall.

Tags: #linux #root #sudo #su #useradd #userdel #passwd #wall #ulimit #cron #ssh #ftp #/etc/passwd #/etc/shadow #/etc/group #/etc/gshadow

(End of cheatsheet)

---

## Module 11 — Lecture 105: Linux Group Management — Cheatsheet

#hashtags: #Linux #groups #groupmanagement #/etc/group #GID #groupadd #groupdel #gpasswd #usermod #getent #id #groups #permissions

---

## Key Definitions
- Group: collection of users used to manage permissions collectively. #groups
- /etc/group: default config file that stores group records. #/etc/group
- GID: Group ID, numeric identifier for a group. #GID
- Group member list: comma-separated usernames in field 4 of /etc/group. #groupmembership
- Orphan files: files whose group no longer exists after a group is deleted. #orphan

---

## /etc/group — Record format
Each line:  
group_name:password:GID:user_list  
- Example: wheel:x:10:root,alice,bob  
- Field 1 = name, Field 2 = (encrypted) password, Field 3 = GID, Field 4 = comma-separated members. #/etc/group

---

## GID ranges / notes
- System GIDs (reserved): historically 0–499; many modern distros use 0–999 (check distro). #GID  
- Use a GID ≥ 500 (or ≥1000 depending on distro) for normal groups. #GID

---

## Common commands (quick reference)
| Action | Command (synopsis) | Notes |
|---|---:|---|
| Create group | groupadd [-g GID] groupname | -g sets GID (lowercase). #groupadd |
| Delete group | groupdel groupname | Removing group may orphan files. #groupdel |
| Change group name/GID | groupmod [-n newname] [-g newGID] groupname | #groupmod |
| Add user to group (append) | usermod -aG group username | -a (append) + -G (supplementary groups). #usermod |
| Add/remove member (group-managed) | gpasswd -a username group / gpasswd -d username group | Useful for managing /etc/group membership. #gpasswd |
| Show group entry | getent group groupname || grep '^groupname:' /etc/group | Portable lookup. #getent |
| Show user's groups | id username  OR  groups username | id shows uid/gid and supplementary groups. #id #groups |

(Use root or sudo for administration commands.)

---

## Key Concepts / Short Tips
- Primary vs supplementary groups:
  - A user's primary group is stored in /etc/passwd (not /etc/group) — supplementary groups appear in /etc/group. #groups
- When deleting a group, files with that GID remain but the group name is gone (become orphans); system may reassign or require manual fix. #orphan
- Prefer gpasswd or usermod -aG to add users — avoid usermod -G without -a (it replaces supplementary groups). #usermod #gpasswd
- Verify GID assignment after group creation via getent group or /etc/group. #groupadd #getent

---

## Important Properties / Invariants
- /etc/group is authoritative for supplementary group membership.
- Membership list is comma-separated; empty list = no supplementary members.
- GIDs must be unique for distinct groups (OS enforces uniqueness). #GID
- System account GIDs should not be reused for regular user groups. #GID

---

## Quick Reference (one-liners)
- Create group with specific GID: sudo groupadd -g 1500 AWS1  #groupadd
- Add existing user to group (append): sudo usermod -aG AWS1 BITS1  #usermod
- Add user to group (alternate): sudo gpasswd -a BITS1 AWS1  #gpasswd
- Remove user from group: sudo gpasswd -d BITS1 AWS1  #gpasswd
- Delete group: sudo groupdel AWS1  #groupdel
- View group record: getent group AWS1  OR  grep '^AWS1:' /etc/group  #getent
- Show user groups: id BITS1  OR  groups BITS1  #id #groups

---

Keep this sheet for quick lookup of formats, flags, and common pitfalls when managing Linux groups.

---

## Module 11 — Lecture 106: Low-level I/O & Admin Commands — Cheatsheet

#hashtags: #low-level-functions #system-calls #file-io #file-descriptors #open #read #write #close #creat #lseek #O_RDONLY #O_WRONLY #O_RDWR #O_CREAT #O_EXCL #buffer #size_t #mode_t #unix #sudo #su #wall #user-management #group-management #gpasswd #ulimit

---

## Key Definitions (one-line)
- Low-level function: OS-level routine that interacts directly with hardware/memory (often via system calls).  
- System call: Kernel-provided API for user programs to request OS services (e.g., file I/O).  
- File descriptor (fd): small integer handle that identifies an open file within a process.  
- Buffer: temporary memory area used to read/write chunks of data.  
- mode_t: data type used for file permission bits (e.g., 0644).  
- size_t / ssize_t: unsigned (size_t) and signed (ssize_t) types for representing byte counts or return sizes.  
- whence: reference position for lseek (SEEK_SET/SEEK_CUR/SEEK_END).  
- Superuser / root: account with administrative privileges (can run privileged commands).  

---

## Formulas / Signatures (quick reference)
- open: int open(const char *pathname, int flags, mode_t mode /*optional*/);
- creat: int creat(const char *pathname, mode_t mode);
- read: ssize_t read(int fd, void *buf, size_t count);
- write: ssize_t write(int fd, const void *buf, size_t count);
- close: int close(int fd);
- lseek: off_t lseek(int fd, off_t offset, int whence);

Return values:
- open/creat: file descriptor >=0 on success, -1 on error (errno set).  
- read/write: number of bytes read/written (ssize_t), 0 = EOF for read, -1 on error.  
- close: 0 on success, -1 on error.  
- lseek: resulting offset (off_t) or -1 on error.

---

## Key Algorithms / Concepts (bulleted)
- #FileOpen: use open() with flags to obtain an fd; use mode only when creating.  
- #FileCreate: creat() creates a new file and returns fd (equivalent to open with O_CREAT|O_WRONLY|O_TRUNC).  
- #ReadWrite: read(fd, buf, n) / write(fd, buf, n) operate on buffers and return bytes actually transferred.  
- #FileClose: close(fd) releases the descriptor; other processes unaffected unless shared fd.  
- #SeekNavigation: lseek moves file offset; use SEEK_SET / SEEK_CUR / SEEK_END.  
- #Flags: control access mode and behavior (read-only, write-only, create, exclusive).  
- #Permissions: file permissions expressed as octal bits (owner/group/other: r=4,w=2,x=1).  
- #Concurrency: multiple processes can open and read same file concurrently; writes may require synchronization.  
- #LowLevelProps: typically implemented in C/assembly; direct memory/hardware access; can be non-portable but fast.  

---

## Important Properties / Invariants
- File descriptors are unique per process (small int).  
- Multiple fds (same or different processes) can reference the same underlying file description (shared offset unless reopened).  
- read() returning 0 => EOF. read()/write() may transfer fewer bytes than requested — always check return value.  
- O_CREAT creates when absent; O_EXCL combined with O_CREAT causes open to fail if file exists.  
- lseek offset can be positive (forward) or negative (back) relative to whence.  
- Always close fds to free kernel resources and allow others to use files.  
- Administrative commands require superuser (sudo / root).  

---

## Open Flags (common)
- O_RDONLY — open for read only (#O_RDONLY)  
- O_WRONLY — open for write only (#O_WRONLY)  
- O_RDWR   — open for read & write (#O_RDWR)  
- O_CREAT  — create file if it does not exist (#O_CREAT)  
- O_EXCL   — with O_CREAT: fail if file exists (#O_EXCL)  
- (others: O_TRUNC, O_APPEND, etc.)

---

## lseek whence values (quick)
- SEEK_SET: offset relative to file start (offset can be positive/negative).  
- SEEK_CUR: offset relative to current file position.  
- SEEK_END: offset relative to file end (commonly negative to go backwards).

Example: lseek(fd, +5, SEEK_SET) -> move to byte 5 from start.

---

## File permission octal quick reference
- Owner / Group / Others bits: r=4, w=2, x=1.  
- Examples: 0644 => owner rw-, group r--, other r--.  
- mode_t used when creating files (open/creat).

---

## Quick Reference: System-call table (scannable)
- open(path, flags[, mode]) — get fd; use flags (O_RDONLY/O_WRONLY/O_RDWR); mode used if creating.  
- creat(path, mode) — create new file, return fd.  
- read(fd, buf, cnt) — read up to cnt bytes into buf; returns bytes read or 0 (EOF).  
- write(fd, buf, cnt) — write up to cnt bytes from buf; returns bytes written.  
- lseek(fd, offset, whence) — set/get file offset; returns resulting offset.  
- close(fd) — close descriptor; returns 0 on success.

---

## Quick Reference: Admin commands & usage
- sudo <cmd> — run command as superuser (Super User DO) (#sudo)  
- su - <user> — switch user / become root (#su)  
- wall "message" — broadcast message to all logged-in users (#wall)  
- adduser <username> — add a new user (#adduser)  
- deluser <username> — remove a user (#deluser)  
- groupadd <groupname> — create group (#groupadd)  
- groupdel <groupname> — delete group (fails if it is a primary group of existing users) (#groupdel)  
- gpasswd — administer group membership/password; add/remove users, lock/unlock group (#gpasswd)  
- ulimit — view/set resource limits for shell/processes (#ulimit)

Notes:
- Many admin commands require sudo/root.  
- Deleting a group that is a user's primary group requires changing that user's primary group or deleting the user first.

---

## Quick Tips (for exam lookups)
- Always check read/write return value — partial transfers are possible.  
- Use O_EXCL with O_CREAT to prevent race-condition creates.  
- Use mode_t octal to set permissions at create time (e.g., 0644).  
- Use lseek to implement random-access reads/writes.  
- Close fds when done to avoid leaks and lock/file access issues.  
- Use wall to announce maintenance to all logged-in users.

---

Keep this sheet handy for file I/O syscalls and basic Unix admin commands. Good luck on the exam!

---
