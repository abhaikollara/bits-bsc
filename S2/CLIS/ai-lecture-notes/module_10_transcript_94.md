# Kernel vs User Mode — Cheatsheet
#kernel-mode #user-mode #context-switch #system-call #interrupt #trap #privileged-instruction #mode-bit #interrupt-handler #CPU #process #operating-system #kernel #user-space #memory #hardware

---

## Key Definitions
- Kernel mode: CPU mode with full access to hardware and all memory addresses; used by the OS/kernel.  
- User mode: Restricted CPU mode for user processes; no direct access to hardware or all RAM.  
- System call: Controlled request by a user process to the OS to access hardware or privileged services.  
- Context switch (mode switch): Transition of CPU execution between user mode and kernel mode.  
- Interrupt: Signal (hardware/software) that causes the CPU to stop current execution and transfer control to an interrupt handler.  
- Trap: Entering a special handler/state (often triggered by a system call) to switch to kernel mode.  
- Privileged instruction: CPU instructions only executable in kernel mode (e.g., direct I/O, change memory mappings).  
- Mode bit: CPU/status bit indicating current mode (0 = kernel, 1 = user).  
- Interrupt handler: Kernel routine that saves CPU state, services the interrupt/trap, and restores state.

---

## Formulas / Notation
- Mode bit: 0 → kernel mode, 1 → user mode  
- Context switch sequence (concise):  
  User process → system call → interrupt/trap → mode bit = 0 → save CPU state → execute kernel code → restore CPU state → mode bit = 1 → return to user process

---

## Key Concepts / Steps (quick bullets)
- #Boot: System starts in #kernel-mode at boot.  
- #Access: Kernel mode has direct access to all hardware & memory; user mode does not.  
- #SystemCall flow:
  - User calls API → kernel invoked via trap/interrupt → kernel executes request → returns result to user.  
- #ModeTransition:
  - Switch does NOT occur automatically; triggered by interrupt/trap (e.g., system call).  
- #SaveRestore:
  - Interrupt handler saves CPU registers/state before switching; restores before returning.  
- #PrivilegeEnforcement:
  - Only kernel mode can execute privileged instructions and access protected resources.

---

## Important Properties / Invariants
- User processes cannot execute privileged instructions nor access arbitrary physical memory.  
- Kernel must save full CPU state (registers, program counter, status/mode bit) before servicing and restore after.  
- Mode bit enforces protection barrier between user-space and kernel-space.  
- Context switching introduces overhead (must save/restore state and switch protection context).  
- Kernel is trusted authority for hardware access and resource management.

---

## Quick Reference (scannable)
- Mode bit mapping: 0 = kernel, 1 = user. #mode-bit  
- Boot mode: kernel mode. #boot #kernel-mode  
- Who can access hardware directly: Kernel only. #hardware #kernel-mode  
- How user accesses hardware: via system calls → kernel. #system-call  
- Trigger for mode switch: interrupt / trap generated (system call). #interrupt #trap  
- Interrupt handler duties: save CPU state → handle request → restore CPU state → set mode bit back. #interrupt-handler  
- Return to user: set mode bit = 1. #return  
- Common invariant: kernel must protect and isolate hardware/memory from user processes. #isolation

---

## Hashtag Index (for quick search)
#kernel-mode #user-mode #context-switch #system-call #interrupt #trap #mode-bit #interrupt-handler #privileged-instruction #CPU #process #kernel #user-space #memory #hardware

--- 
(Use this sheet to quickly locate mode mappings, transition steps, and the roles of kernel vs user modes during an exam.)