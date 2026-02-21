# Processes & Process States (Linux) — Cheatsheet
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