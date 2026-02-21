# Signals & Signal Handlers (Linux) — Cheatsheet

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