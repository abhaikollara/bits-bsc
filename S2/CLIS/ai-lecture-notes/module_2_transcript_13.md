# Linux Fundamentals Cheatsheet
#hashtags: #linux #kernel #shell #filesystem #processes #systemlibraries #bootloader #init #systemd #systemctl #ps #ls #commands #grub #runlevels #targets #permissions

---

## Key Definitions (one-line)
- Kernel: Core OS component managing hardware, drivers, memory, and processes. #kernel  
- Shell: User interface (command interpreter) for running commands and scripts. #shell  
- Filesystem: Hierarchical namespace of files/directories rooted at `/`. #filesystem  
- Process: An executing program instance (has PID, state, parent). #processes  
- System libraries: Shared libraries (.so) used by programs at runtime. #systemlibraries  
- Bootloader: Program that loads the kernel (e.g., GRUB) during boot. #bootloader #grub  
- Init (PID 1): First user-space process that starts and manages services (systemd or SysV). #init #systemd  
- Unit/Service (systemd): Config file describing how to start/manage a service. #systemctl

---

## Boot & Login Sequence (scannable steps)
1. Firmware (BIOS/UEFI) POST → reads boot device.  
2. Bootloader (GRUB) loads kernel + initramfs. #grub #bootloader  
3. Kernel initialization (drivers, mounts initramfs). #kernel  
4. Root filesystem mounted → kernel execs init (PID 1). #init  
5. Init/systemd reads units → starts services/targets. #systemd #targets  
6. getty/login prompt → user login → user shell session. #login #shell

Important files: `/boot/vmlinuz`, `/boot/initrd.img`, `/etc/fstab`, `/etc/default/grub`.

---

## Formulas / Notation / Quick mappings
- Permission bits: r=4, w=2, x=1 → numeric mode (e.g., 755 = rwx r-x r-x). #permissions  
- Exit code: 0 = success, nonzero = error.  
- Common PID facts: PID 1 = init/systemd; orphaned processes adopted by PID 1. #processes  
- Process listing formats: `ps aux` (BSD) vs `ps -ef` (UNIX). #ps

---

## Key Commands & Flags (quick reference)
- File listing: `ls -l` (long), `ls -a` (hidden), `ls -la`. #ls  
- Process view: `ps aux`, `ps -ef`, `top`, `htop`. #ps  
- Start/stop services (systemd): `systemctl status|start|stop|restart|enable|disable <unit>`. #systemctl #systemd  
- Logs: `journalctl -u <unit>`, `journalctl -b`, `dmesg`. #journalctl #dmesg  
- File ops: `cp`, `mv`, `rm`, `mkdir`, `rmdir`. #commands  
- Disk/FS: `df -h`, `du -sh <path>`, `mount`, `umount`. #filesystem  
- Permissions: `chmod 755 file`, `chown user:group file`, `umask`. #permissions  
- Process control: `kill <PID>`, `kill -9 <PID>`, `pkill -f <pattern>`. #processes  
- Identity: `whoami`, `id`, `su -`, `sudo <cmd>`.  
- Search/text: `grep`, `find`, `cat`, `less`, `tail -f`. #commands

---

## Key Concepts / Components (bulleted)
- Kernel vs User-space: Kernel handles hardware; shells/apps run in user-space. #kernel #shell  
- Single filesystem tree: Everything mounted under `/`. #filesystem  
- Systemd units: service, socket, target, mount, timer, path, etc. #systemd #targets  
- Initramfs purpose: early userspace to mount real root filesystem. #init  
- Service management: `systemctl` controls units, `journalctl` reads logs. #systemctl #journalctl  
- Process lifecycle: create (fork/exec), running, sleeping, stopped, zombie, exit. #processes

---

## Important Properties & Invariants
- PID 1 is special: reaps zombies, adopts orphans. #init  
- Root user UID = 0 has full privileges.  
- Filesystem mount order affects availability (use `/etc/fstab` or systemd mount units). #filesystem  
- Systemd enforces dependencies via unit ordering and targets. #systemd  
- Binary/library locations: `/bin /sbin /usr/bin /usr/sbin /lib /usr/lib`. #systemlibraries

---

## Quick Reference Table (commands → common flags)
| Task | Command (examples) |
|---|---|
| List files | ls -l, ls -la |
| View processes | ps aux, top, htop |
| Manage services | systemctl status/start/stop/restart/enable/disable <unit> |
| Read logs | journalctl -u <unit>, journalctl -b, dmesg |
| Disk usage | df -h, du -sh /path |
| File permissions | chmod 755 file; chown user:group file |
| Kill process | kill PID; kill -9 PID; pkill -f pattern |
| Boot config | update-grub (Debian), edit /etc/default/grub |

---

## Exam Quick Tips (one-liners)
- To check kernel & arch: `uname -a`. #kernel  
- To see PID 1 and tree: `ps -fp 1` and `pstree -p`. #processes  
- To debug boot: check `journalctl -b -1` (previous boot) & `dmesg`. #journalctl #dmesg  
- To persist mounts: add to `/etc/fstab`. #filesystem  
- Use `systemctl is-enabled <unit>` to check boot enablement. #systemctl

---

End — concise reference for Linux components, boot flow, core commands, and quick facts.