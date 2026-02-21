# Linux Device Drivers — Cheatsheet
#keywords: #deviceDrivers #Linux #kernelSpace #userSpace #kernelModule #deviceFiles #systemCalls #kernelInterfaces #lsmod #modinfo #insmod #rmmod #ls_dev #characterDevice #blockDevice

## Key Definitions
- Device driver: Software that intermediates between hardware and the OS, enabling control and communication. #deviceDrivers
- Kernel-space driver: Driver integrated into the kernel with direct access to kernel resources and hardware. #kernelSpace
- User-space driver: Driver running outside the kernel, using system calls / kernel interfaces to access hardware. #userSpace
- Kernel module: Loadable piece of kernel code that implements a driver or kernel feature. #kernelModule
- Device file (/dev): Special filesystem entries representing devices (block/character). #deviceFiles #blockDevice #characterDevice
- System call: Kernel-provided API for user-space programs to request kernel services. #systemCalls
- Kernel interface: Set of APIs and mechanisms the kernel exposes for drivers. #kernelInterfaces

## Formulas / Equations
- None in transcript (N/A)

## Key Algorithms / Concepts
- Role of drivers:
  - Mediates OS ↔ hardware communication and control. #deviceDrivers
  - Manages peripherals (graphics, network, USB, storage). #deviceFiles
- Types of drivers:
  - Kernel-space: low-level, high-performance, direct hardware access. #kernelSpace
  - User-space: runs in userland, flexible, load/unload dynamically, incurs user↔kernel transition overhead. #userSpace
- Writing drivers:
  - Requires understanding kernel interfaces + target hardware. #kernelInterfaces
  - Correct implementation improves system performance & stability. #deviceDrivers #kernelModule

## Important Properties / Invariants
- Kernel-space drivers:
  - Direct access to kernel resources; preferred for critical/performance-sensitive tasks. #kernelSpace
- User-space drivers:
  - Safer to develop/iterate; can be dynamically loaded/unloaded; performance overhead due to boundary crossing. #userSpace
- Device files:
  - Provide userland access to devices (listed in /dev). #deviceFiles
- Kernel modules:
  - Can be loaded/unloaded at runtime (dynamic). #kernelModule
- Security & stability:
  - Buggy kernel drivers can crash the system; correctness is critical. #kernelSpace #kernelModule

## Commands Quick Reference (scannable)
| Command | Purpose | Typical usage |
|---|---:|---|
| lsmod | List currently loaded kernel modules | lsmod #lsmod |
| modinfo | Display information about a specific module | modinfo <module> #modinfo |
| insmod | Load a kernel module into the running kernel | insmod <module.ko> #insmod |
| rmmod | Unload a kernel module from the running kernel | rmmod <module> #rmmod |
| ls /dev | Show device files (character & block devices) | ls /dev #ls_dev #deviceFiles |

- Notes:
  - insmod/rmmod operate on kernel modules (.ko) and names; modinfo prints metadata (ver, deps, params). #kernelModule
  - ls /dev lists entries representing physical/virtual devices; differentiate block vs character devices. #blockDevice #characterDevice

## Quick Reference — Scannable Facts
- Device drivers = required for OS to control hardware. #deviceDrivers
- Kernel-space: faster, privileged, riskier. #kernelSpace
- User-space: safer/flexible, slower due to system calls. #userSpace
- Kernel modules can be dynamically loaded/unloaded (insmod/rmmod). #kernelModule #insmod #rmmod
- Use lsmod to see loaded modules; use modinfo to inspect a module. #lsmod #modinfo
- Device files live under /dev; used to access hardware from userland. #ls_dev #deviceFiles
- Writing drivers needs kernel API + hardware docs; correct drivers improve performance/stability. #kernelInterfaces

(End of cheatsheet)