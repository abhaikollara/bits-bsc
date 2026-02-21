# Linux CLI Basics — Day-to-day Commands (Cheatsheet)

#keywords
#Linux #CLI #commandline #terminal #stty #who #whoami #date #pwd #man #mail #write #tabs #tabcompletion #history #logout #CtrlC #CtrlU #CtrlD

---

## Key Definitions
- Command: a text instruction given to the OS to perform a task.  
- Terminal / CLI: text-based interface to enter commands.  
- Prompt: the shell marker (e.g., $) — do not type it.  
- Echo: terminal setting that shows typed characters; turned off for passwords.  
- Tab completion: pressing Tab to auto-complete file/command names.  
- Manual (man): built-in documentation for commands and options.  

---

## Formulas / Notation
- RETURN = Enter key (execute command)
- Control notation: Ctrl-X shown as Ctrl+X (e.g., Ctrl+D)  
- stty syntax examples:
  - stty -echo        (turn echo off)
  - stty echo         (turn echo on)
  - stty sane         (restore defaults)
  - stty intr ^C      (set interrupt char to Ctrl+C)  
  (Options and arguments are case-sensitive.)

---

## Key Commands & Concepts
- who
  - Purpose: list currently logged-in users and their login times/sessions.  
  - Syntax: who
- whoami (or who am I)
  - Purpose: show current user identity.  
  - Syntax: whoami  or  who am i
- date
  - Purpose: display current date & time.  
  - Syntax: date
- pwd
  - Purpose: print current working directory.  
  - Syntax: pwd
- man
  - Purpose: display manual pages and options for a command.  
  - Syntax: man <command>  (e.g., man who)
- mail
  - Purpose: read/send system mail (simple client).  
  - Syntax: mail                 (read)  
           mail <user@host>     (send; Ctrl+D to finish body)
- write
  - Purpose: send a message to another logged-in user.  
  - Syntax: write <username> <tty?>  (user must be logged in)
- stty
  - Purpose: view/modify terminal settings (echo, control chars, tabs).  
  - Syntax: stty             (view)  
           stty -echo        (disable echo)  
           stty echo         (enable echo)  
           stty sane         (reset to sane defaults)  
           stty intr ^C      (set interrupt char)
- tabs
  - Purpose: set/reset terminal tab stops.  
  - Syntax: tabs -0   (reset)  tabs -8  (set standard 8-col tabs)
- Tab completion
  - Behavior: press Tab to complete filenames/commands or list matches.
- history
  - Purpose: list previously-entered commands.  
  - Syntax: history
- Logout
  - Ctrl+D (EOF) to log out, or type exit / logout

---

## Important Properties / Invariants
- Commands and stty options are case-sensitive.  
- Do not type the shell prompt symbol ($) when entering commands.  
- Password input: echo is off (characters not displayed).  
- Ctrl+D sends EOF — commonly logs out of shell or ends input (e.g., mail).  
- Ctrl+U kills the entire current input line (before Enter).  
- Backspace removes last character; arrow keys move cursor for editing.  
- Tab completion and history speed up command entry.  
- Use man pages to discover options; commands often have many flags.

---

## Quick Reference (scannable)

Commands:
- who        — list logged-in users
- whoami     — current username
- date       — show date/time
- pwd        — show present working directory
- man <cmd>  — manual for <cmd> (e.g., man who)
- mail       — read system mail
- mail addr  — send mail to addr (end body with Ctrl+D)
- write user — send message to logged-in user
- history    — show past commands
- exit/logout / Ctrl+D — log out

stty (common):
- stty              — show terminal settings
- stty -echo        — turn off echo (useful for passwords)
- stty echo         — turn on echo
- stty sane         — restore defaults
- stty intr ^C      — set interrupt to Ctrl+C (case-sensitive)

Tabs & completion:
- tabs -0           — reset tab stops
- tabs -8           — set 8-column tabs
- Tab               — auto-complete filenames/commands

Line editing / control keys:
- Ctrl+U            — kill whole input line
- Ctrl+D            — send EOF / logout
- Ctrl+C            — interrupt current process (if configured)
- Backspace         — delete previous character
- ← / →             — move cursor within line

Manual options (example: who):
- who -a            — all
- who -b            — boot time
- who -d            — dead processes
- who -H            — show headings

Notes:
- If terminal behaves oddly, inspect stty and use stty sane to recover.  
- Use Coursera Labs / terminal emulator to practice commands interactively.

---

#hashtags (summary)  
#Linux #CLI #terminal #stty #tabcompletion #history #man #mail #write #pwd #who #whoami #date #logout #lineediting #controlchars

