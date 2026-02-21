# Signals (raise / kill) — Cheatsheet
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