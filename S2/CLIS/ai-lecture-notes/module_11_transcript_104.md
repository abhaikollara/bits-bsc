# Linux System Administration — Advanced Commands (cheatsheet)

Keywords: #linux #unix #root #administrator #privilege #sudo #su #useradd #userdel #passwd #wall #ulimit #cron #ssh #ftp #/etc/passwd #/etc/shadow #/etc/group #/etc/gshadow #systemadmin

## Key Definitions
- #root: Highest-privilege administrator account (UID = 0).  
- #sudo: "super user do" / "switch user do" — run a command with elevated (usually root) privileges without logging in as root.  
- #su: Switch user / become root by supplying the target account's password (often root password).  
- #useradd: Command to create a new user account (requires root/sudo).  
- #passwd: Set/change a user's login password (requires root/sudo to change another user).  
- #userdel: Delete a user account (requires root/sudo).  
- #wall: Broadcast a message to all logged-in users (root-only by default).  
- #ulimit: Per-user resource limits (max file size, processes, etc.).  
- #cron: Scheduler service for per-user/system jobs (access controllable by root).  
- /etc/passwd: User account info (username, UID, GID, home, shell).  
- /etc/shadow: Encrypted passwords and password policy data.  
- /etc/group: Group membership info.  
- /etc/gshadow: Secure group passwords/membership.

## Formulas / Notes
- Root UID = 0 (root is identified by UID 0).  
- Logging: #sudo and #su operations are typically logged (audit trail for privileged commands).  
- No algorithmic formulas in this lecture.

## Key Commands / Concepts (quick bullets)
- su
  - Become another user (commonly `su` or `su -`) — requires target user's password (#su).
- sudo
  - Run single command as root or another user, can use invoking user's password if configured (#sudo).
  - Safer than logging in as root; supports fine-grained permission via /etc/sudoers.
- wall
  - Broadcast text to all logged-in users (root-only usually).
  - Example: `sudo wall "Server will shut down at 17:00"`
- useradd
  - Create a user; adds entries to `/etc/passwd`, `/etc/shadow`, `/etc/group`, `/etc/gshadow`.
  - Requires root/sudo (#useradd).
- passwd
  - Set or change a user's password. Example: `sudo passwd username` (#passwd).
- userdel
  - Delete a user account. Example: `sudo userdel username` (#userdel).
  - Common options: `-r` remove home and mail spool, `-f` force delete, `-h` help.
- ulimit
  - Set maximum resource usage for user processes (file size, number of processes, stack size) (#ulimit).
- cron
  - Root controls which users can use cron; system and per-user scheduled tasks (#cron).
- Networking services
  - Root controls access/config of network services (e.g., #ssh, #ftp).

## Important Properties / Invariants
- Any operation that installs, removes, modifies system software or protected system files requires root privileges.  
- Root can:
  - Change file attributes and contents regardless of file-level protections.  
  - Delete files inside protected directories.  
  - Change any user's password without knowing the old one.  
  - Set system clock/date.  
  - Control access to scheduling, resource limits, and network services.
- sudo vs su:
  - su requires target account password (usually root).  
  - sudo can be configured to use the invoking user's password and can limit allowed commands; useful for auditing and least privilege.
- Auditing:
  - Use sudo (and proper syslog/audit) to keep a record of privileged actions.

## Quick Reference (scannable)
- File locations:
  - `/etc/passwd` — user account fields  
  - `/etc/shadow` — encrypted passwords  
  - `/etc/group` — group memberships  
  - `/etc/gshadow` — group secure info
- Common commands (syntax)
  - Create user: `sudo useradd <username>`  (#useradd)  
  - Set password: `sudo passwd <username>`  (#passwd)  
  - Delete user: `sudo userdel <username>` or `sudo userdel -r <username>`  (#userdel)  
  - Become root: `su -` (needs root password)  (#su)  
  - Run single command as root: `sudo <command>`  (#sudo)  
  - Broadcast message: `sudo wall "message"`  (#wall)  
  - Set/check ulimit: `ulimit -a` / `ulimit -n <value>`  (#ulimit)
- userdel options:
  - `-r` remove home and mail, `-f` force, `-h` help
- Best practices:
  - Prefer `sudo` over direct root login.  
  - Restrict sudoers to necessary commands.  
  - Ensure auditing/logging of privileged commands.
- Tasks requiring root (quick list):
  - Install/update software, modify system dirs, change other users' passwords, set system time, control cron, change networking service configs, broadcast using wall.

Tags: #linux #root #sudo #su #useradd #userdel #passwd #wall #ulimit #cron #ssh #ftp #/etc/passwd #/etc/shadow #/etc/group #/etc/gshadow

(End of cheatsheet)