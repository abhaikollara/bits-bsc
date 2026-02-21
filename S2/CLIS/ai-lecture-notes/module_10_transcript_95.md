# Process Creation & OS Services — Cheatsheet
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