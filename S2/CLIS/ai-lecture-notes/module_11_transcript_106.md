# Low-level I/O & Admin Commands — Cheatsheet
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