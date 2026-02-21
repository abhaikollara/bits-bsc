# Open files & File Descriptor Management — Cheatsheet
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