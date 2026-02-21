# Processes, Lifecycle, fork/exec, wait, and Signals — Cheatsheet
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