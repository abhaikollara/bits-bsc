# Fork (process creation) — Cheatsheet
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