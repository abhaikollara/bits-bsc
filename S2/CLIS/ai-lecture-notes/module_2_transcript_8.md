# Linux Manual & Basic Commands — Cheatsheet
#hashtags: #linux #man #manual #passwd #date #who #whoami #write #adduser #sudo #su #users #timezones #format

---

## Key Definitions
- man: The manual-page viewer for commands/programs (#man #manual)  
- passwd: Change a user's password (#passwd #password)  
- date: Display or set system date/time; supports format specifiers (#date #time #format)  
- who: Show currently logged-in users and related info (#who)  
- whoami: Print current effective username (alias: who am i) (#whoami)  
- write: Send a message to another logged-in user/TTY (#write)  
- adduser: Create a new user account (usually via sudo) (#adduser)  
- sudo: Run a command with administrative privileges (#sudo)  
- su: Switch user / start a login shell for another user (#su)

---

## Formulas / Notation
- man syntax: man [options] <command>
- passwd syntax: passwd [options] [user]
- date syntax (display custom): date +"%<specifier> %<specifier> ..."  (enclose format in quotes)
- who syntax: who [options]
- write syntax: write <username> [tty]
- adduser: sudo adduser <username>
- su-login: su - <username>

---

## Man pages (manual) — Key Options & Behavior (#man)
- man <command> : open manual page for command  
- man -k <keyword> : search keyword in man descriptions (apropos)  
- man -f <command> : short description (whatis)  
- man -a <command> : show all manual pages for command (from all sections/packages)  
- man -w <command> : print path(s) to manual page file(s)  
- man -h / man --help : show help for man itself (also common for most commands)  
- man <section> <name> : show man page in specific section (see sections table)

Man sections (commonly used)
- Section 1 — User commands (#man-section-1)  
- Section 2 — System calls (#man-section-2)  
- Section 3 — Library functions (#man-section-3)

Example: man 1 wc -> command wc; man 3 cw -> library function (may be not present)

---

## passwd (change password) — Quick facts (#passwd)
- passwd : change current user's password (prompts: current, new, confirm)  
- sudo passwd <user> : change another user's password (requires sudo)  
- Options:  
  - -l : lock account password  
  - -u : unlock account password  
  - -d : delete password (disable password)  
  - -e : set password to expire

Notes: password input is not echoed; policy/length enforced by PAM.

---

## date (display / set date & time) — Format tokens (#date #time #format)
- Default: date -> prints current date/time in default format  
- Custom: date +"%A %d %B %Y"  -> e.g., Monday 07 August 2023  
- Common specifiers:
  - %a : abbreviated weekday name (Sun)  
  - %A : full weekday name (Sunday)  
  - %b / %h : abbreviated month name (Aug)  
  - %B : full month name (August)  
  - %d : day of month (01..31)  
  - %H : hour (00..23) — 24-hour  
  - %I : hour (01..12) — 12-hour (transcript used lowercase l for 12h; common is %I)  
  - %M : minute (00..59)  
  - %S : second (00..60)  
  - %Y : year with century (2023)  
  - %y : year without century (23)  
  - %Z : time zone name (UTC, etc.)  
- Setting system date: date requires appropriate privileges (sudo/root)

---

## who / whoami — Usage & Options (#who #whoami)
- who : list logged-in users (username, tty, login time, host)  
- who -a : show all available information (inclusive output)  
- who -b : show last system boot time  
- who -d : show dead processes / abandoned sessions  
- who -l : (transcript) omit hostname/terminal (note: behavior may vary)  
- who -q : quick list + count of logged-in users  
- who -T : display time of last system activity (transcript)  
- who -u : show users and process status (including processes still running)  
- who -H : show header line  
- who -w : display without terminal information (transcript)  
- whoami / who am i : print the current user name (effective user)

---

## write — Send message to logged-in user (#write)
- Syntax: write <username> [tty]  
- Requirements: recipient must be logged in and message writing allowed on their TTY  
- Example: write student pts/1  (then type message; Ctrl-D to end)  
- Use-case: quick terminal-to-terminal messaging on multi-user systems

---

## adduser / sudo / su — Creating & switching users (#adduser #sudo #su)
- sudo adduser <username> : create a new user (prompts for password & details)  
  - creates home directory, group, prompts for user info  
- sudo : run command as root (prompts for caller password)  
- su - <username> : switch to user account with login shell (use to test login / open user session)

---

## Important Properties & Invariants
- man shows per-section documentation; same name can have multiple manual pages (use man -a)  
- man -k is keyword search (useful if you don't know exact command)  
- passwd requires current password for non-root users; sudo allows root to change others' passwords  
- date format specifiers must be prefixed by % and enclosed in quotes to avoid shell expansion  
- who only reports currently logged-in terminal sessions; remote users and background processes appear per options  
- write only works if recipient's terminal allows messages (mesg toggle) and the user is logged in on specified tty

---

## Quick Reference (one-liners & examples)
- Open manual: man ls  
- Search manual pages for keyword "disk": man -k disk  
- Short description: man -f ls  
- Show all man pages for a name: man -a man  
- Print man page path: man -w passwd

- Change own password: passwd  
- Change another's password: sudo passwd alice  
- Lock account: sudo passwd -l username

- Show date: date  
- Custom date: date +"%A %d %B %Y"  -> Monday 07 August 2023  
- Set date (requires sudo/root): sudo date -s "2023-08-07 14:00:00"

- List logged-in users: who  
- Quick user count: who -q  
- Show boot time: who -b  
- Current user: whoami   (or who am i)

- Send message: write <username> [pts/X]  (Ctrl-D to end message)  
- Create user: sudo adduser student  
- Switch to user: su - student

---

Keep this sheet by your terminal for fast lookup: search tags like #man, #passwd, #date, #who, #write, #adduser.