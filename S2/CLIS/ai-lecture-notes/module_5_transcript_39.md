# I/O Queuing, I/O Scheduling & Interrupt Handling — Linux (Cheatsheet)

Keywords
- #IO #I/O #IOQueuing #IOScheduling #Interrupts #ISR #irqreturn_t #CFQ #Deadline #NOOP #/sys #/proc #proc_interrupts #blockdevice #SSD #HDD #LinuxKernel

Key Definitions
- I/O queuing: Kernel mechanism that buffers and orders pending I/O requests from CPUs/devices to improve throughput and latency.
- I/O scheduler: Kernel component deciding service order of pending block I/O requests.
- Interrupt: Hardware signal to CPU indicating device needs immediate attention.
- Interrupt handler / ISR: Kernel routine registered to process a specific hardware interrupt.
- irqreturn_t: Return type used by Linux interrupt handlers (indicates handled/not handled).
- Block device: Device that supports buffered block I/O (e.g., /dev/sda).
- /sys filesystem: Kernel interface to view/change device and kernel settings (e.g., schedulers).
- /proc/interrupts: Procfs file showing counts of interrupts handled per CPU/device.

Formulas / Notation
- No explicit mathematical formulas in lecture.
- Common performance terms:
  - Latency: time for single I/O to complete
  - Throughput: I/O per second or MB/s
  - Fairness / deadline = qualitative metrics (no formula provided)

Key Algorithms / Concepts
- #CFQ (Completely Fair Queuing)
  - Fair distribution of I/O bandwidth across processes; good for desktop/interactive workloads.
- #Deadline
  - Ensures time-bounded servicing of requests to improve responsiveness for real-time/latency-sensitive tasks.
- #NOOP
  - Simple FIFO/merge-based scheduler with minimal overhead; good for low-latency devices (e.g., #SSD) or hardware that does its own scheduling.
- Changing scheduler per block device
  - Use /sys/block/<device>/queue/scheduler to view/change scheduler.
- Interrupt Handling
  - Devices raise interrupts -> CPU invokes registered ISR -> ISR services device (quick) and may schedule deferred work.
- Viewing interrupt stats
  - /proc/interrupts shows interrupt counts by CPU and device.

Important Properties / Invariants
- Scheduler choice affects latency vs throughput vs fairness; choose according to workload (interactive vs batch vs realtime) and device (HDD vs SSD).
- NOOP minimizes CPU-side reordering; better when device-level controller optimizes ordering (SSD/NVMe).
- Deadline provides upper bounds on request wait time (improves predictability).
- CFQ provides per-process fairness; may add overhead.
- Interrupt handlers should be short (do minimal work) to avoid blocking CPU; defer long work to bottom halves/tasklets/workqueues.
- Changing scheduler is per-block-device and immediate (takes effect at kernel level).
- Many operations require root privileges (use sudo).

Quick Reference (Commands, Paths, Examples)
- Show current scheduler for /dev/sda:
  - cat /sys/block/sda/queue/scheduler
  - Output format example: "[cfq] noop deadline" (brackets = current)
- Set scheduler for /dev/sda (requires root):
  - echo cfq  > /sys/block/sda/queue/scheduler
  - echo deadline > /sys/block/sda/queue/scheduler
  - echo noop > /sys/block/sda/queue/scheduler
  - Use sudo if needed: sudo sh -c 'echo deadline > /sys/block/sda/queue/scheduler'
- View interrupt statistics:
  - cat /proc/interrupts
- Register / implement ISR (kernel module typical pattern):
  - Prototype: irqreturn_t handler(int irq, void *dev_id)
  - Register: request_irq(irq, handler, flags, name, dev_id)
  - Unregister: free_irq(irq, dev_id)
  - (Use sparingly and with correct flags; requires kernel/module programming)
- Permissions:
  - Many /sys and /proc writes require root. Use sudo and be cautious.

Scheduler Quick Comparison (scannable)
- CFQ (#CFQ)
  - Pros: fairness, good for interactive
  - Cons: overhead, may not suit SSDs
- Deadline (#Deadline)
  - Pros: bounded latency, predictable
  - Cons: less fairness for throughput
- NOOP (#NOOP)
  - Pros: minimal overhead, good for SSD/NVMe or stacked schedulers
  - Cons: no fairness / time guarantees

Gotchas / Tips
- Default scheduler may vary by kernel/version and device (check /sys/block/<dev>/queue/scheduler).
- Writing incorrect values or interfering with drivers can destabilize system—use caution.
- Interrupts can be balanced across CPUs by kernel settings (not covered in depth in this lecture).
- Prefer NOOP for hardware that handles its own queuing (NVMe controllers); prefer Deadline or CFQ when predictability or fairness is required.

One-line summary
- Use /sys/block/<dev>/queue/scheduler to view/change I/O scheduler (#CFQ, #Deadline, #NOOP) based on workload and device; use /proc/interrupts and irqreturn_t/ISRs to monitor and handle hardware interrupts.