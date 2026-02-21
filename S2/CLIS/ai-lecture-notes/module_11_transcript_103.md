# File I/O: read, write, and random access (#fileio #read #write #lseek #filedescriptor #sequentialaccess #randomaccess #EOF #error #systemcall)

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