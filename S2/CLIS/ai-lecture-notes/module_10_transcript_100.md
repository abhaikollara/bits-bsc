# System Call vs Function Call — Cheatsheet
#keywords: #systemcall #functioncall #kernel #user_mode #kernel_mode #contextswitch #IO #interprocesscommunication #privilege #syscall_instruction #software_interrupt #sysenter #blocking #nonblocking #syscall_examples #function_examples

---

## Key Definitions
- System call: A kernel-provided interface that lets a program request services from the OS (enters kernel mode). #systemcall #kernel  
- Function call: A user-mode invocation of a subroutine/procedure/method within the same program (no mode switch). #functioncall  
- Kernel mode: CPU privilege level where OS code can access protected resources/hardware. #kernel_mode #privilege  
- User mode: Lower privilege level where application code runs and cannot directly access hardware. #user_mode  
- Context switch (mode switch): Transition between user mode and kernel mode (or between processes/threads). #contextswitch

---

## Formulas / Notation
- Mode transition sequence: user code -> trap/syscall -> kernel handler -> return -> user code  
- Cost relation: T_function_call << T_system_call (function calls are much cheaper)  
- Rough decomposition for syscall latency:
  T_syscall ≈ T_user_call_overhead + T_trap + T_kernel_handler + T_return + (optional) T_scheduler
- Syscall invocation mechanisms: software interrupt (e.g. int 0x80), SYSENTER/SYSEXIT, SYSCALL/SYSRET. #software_interrupt #sysenter #syscall_instruction

---

## Key Algorithms / Concepts
- System call usage:
  - Services: file IO, device IO, process control, interprocess communication, memory management. #IO #interprocesscommunication  
  - Examples: open, read, write, close, fork, exec, wait, mmap, ioctl, kill. #syscall_examples
- Function call characteristics:
  - Local routines, library functions, user-defined functions (e.g., printf, strlen) executed in user mode. #function_examples
- Control flow:
  - Function call: call -> push args/regs/frame -> execute -> return  
  - System call: call user stub -> trap to kernel -> kernel executes -> return to user
- Privilege boundary:
  - Syscalls cross security/privilege boundary; arguments validated by kernel. #privilege #security

---

## Important Properties / Invariants
- Mode switch:
  - System call causes user->kernel->user transitions; function call does not. #contextswitch
- Resource access:
  - Only kernel (via system calls) can access protected resources/hardware. #kernel #IO
- Overhead:
  - System calls add significant latency and cannot be inlined/optimized away by compiler; function calls can be optimized (inline, tail-call). #performance
- Blocking behavior:
  - Many syscalls may block (sleep) and involve scheduler; function calls run until completion in same thread. #blocking #nonblocking
- Error reporting:
  - Syscalls return status/errno from kernel; function calls return per language convention. #syscall
- Safety:
  - Arguments to syscalls must be validated by kernel — user pointers cannot be trusted. #security

---

## Quick Reference (Scannable)
- When to use:
  - Use a system call to request OS services or access hardware. #systemcall  
  - Use a function call for algorithmic/subroutine work inside the process. #functioncall
- Examples:
  - System calls: open, read, write, fork, exec, mmap, ioctl. #syscall_examples  
  - Function calls: printf, sqrt, user_defined_func. #function_examples
- Performance checklist:
  - Need low latency? Prefer function call. #performance  
  - Need OS resource? Must use system call. #kernel
- Invocation methods (x86-ish):
  - Legacy: int 0x80 (software interrupt) #software_interrupt  
  - Fast: sysenter/sysexit or syscall/sysret #sysenter #syscall_instruction
- Security:
  - Syscall = privilege boundary -> kernel validation required. #privilege #security
- Typical flow (short):
  - Function call: push args -> call -> execute -> ret  
  - Syscall: user stub -> trap -> kernel handler -> return to user

---

## Comparison Table

| Aspect | System Call (#systemcall) | Function Call (#functioncall) |
|---|---:|---|
| Mode | Kernel mode (after trap) #kernel_mode | User mode only #user_mode |
| Purpose | Access OS services/hardware #IO | Execute user-defined routines |
| Context switch | Yes (user↔kernel) #contextswitch | No |
| Overhead | High (mode switch + kernel work) #performance | Low (stack/regs only) |
| Blocking | May block and invoke scheduler #blocking | Runs in-thread (no scheduler involvement) |
| Examples | open, read, write, fork #syscall_examples | printf, sum(), helper() #function_examples |
| Optimizable by compiler | No | Yes (inline, tail-call) |

---

Keep this sheet near your notes for quick lookup during an open-book exam.