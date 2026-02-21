# Low-level File I/O (Linux) — Cheatsheet
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