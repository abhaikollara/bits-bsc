# Linux User Session Lifecycle — Cheatsheet
#keywords: #Linux #login #session #authentication #SSH #TTY #GDM #LightDM #PAM #MFA #shell #Bash #startup-scripts #/etc/passwd #/etc/shadow #logout #processes

---

## Key Definitions
- User initiation: user starts a login via GUI, TTY, or remote client (SSH). #UserInitiation
- Authentication: verifying credentials by comparing entered password to stored (hashed) password. #Authentication
- Multi-factor Authentication (MFA): additional factor(s) beyond password (e.g., mobile OTP, biometrics). #MFA
- Session initialization: system sets up user environment and runs startup scripts. #SessionInitialization
- Shell assignment: shell specified for the user (e.g., /bin/bash) used as the command interpreter. #ShellAssignment
- Login shell vs interactive/non-login shell: different startup script order and behavior. #LoginShell
- Logout / cleanup: termination of session, signaling/killing user processes and freeing resources. #Logout

---

## Lifecycle (compact flow)
user initiation -> authentication -> session initialization -> shell assignment -> user session (use) -> logout -> cleanup
- Notation: Initiation (GUI/TTY/SSH) → Auth (PAM + /etc/shadow) → Init (env + startup scripts) → Shell (/etc/passwd shell) → Active → Logout (SIGHUP, kill user processes)

---

## Formulas / Notation / Fields
- /etc/passwd entry format:
  username:password:UID:GID:GECOS:home:shell
  - Note: password field usually "x" and hashed password stored in /etc/shadow. #/etc_passwd #/etc_shadow
- Common env vars: USER, UID, HOME, SHELL, PATH, LOGNAME. #Environment
- SSH command: ssh user@host  (secure remote login). #SSH

---

## Key Algorithms / Concepts (bulleted)
- User initiation methods:
  - Graphical: GDM, LightDM (display managers). #GDM #LightDM #DisplayManager
  - Local text: TTY virtual consoles (Ctrl+Alt+F1..F7). #TTY
  - Remote: SSH (secure shell). #SSH
- Authentication pipeline:
  - Password verification against hashed entry in /etc/shadow via PAM. #PAM #/etc_shadow
  - Optional MFA step integrated via PAM modules. #MFA
- Session initialization:
  - System loads global and user configs, sets env vars, mounts home (if networked), creates session leader. #SessionInitialization
- Shell assignment and startup scripts:
  - Login shell sequence (common for Bash): /etc/profile → ~/.bash_profile → ~/.bash_login → ~/.profile
  - Interactive non-login shells: ~/.bashrc
  - ~/.bash_profile often sources ~/.bashrc for consistency. #Bash #StartupScripts
- Logout & cleanup:
  - Session termination sends SIGHUP to session processes; system may forcibly kill remaining processes (pkill -u USER). #SIGHUP #Cleanup
  - Session management tools: systemd-logind (loginctl), display manager teardown. #systemd #loginctl

---

## Important Properties / Invariants
- Passwords are stored hashed (never plaintext) — compare hashes during auth. #Hashing
- User processes run with user UID/GID and limited privileges. #UID #GID
- Shell assigned in /etc/passwd determines interpreter for user sessions. #ShellAssignment
- PAM + modules control authentication, account, session, password management. #PAM
- GUI logins start display/session managers (X/Wayland); TTY sessions have a controlling terminal. #X #Wayland #TTY
- On logout, session leader termination usually causes child processes to receive SIGHUP. #SIGHUP

---

## Quick Reference (commands, files, checks)
Files:
- /etc/passwd — account records (shell field). #/etc_passwd
- /etc/shadow — hashed passwords. #/etc_shadow
- /etc/pam.d/ — PAM configuration. #PAM
- /etc/profile, ~/.profile, ~/.bash_profile, ~/.bashrc — startup scripts. #StartupScripts

Commands:
- ssh user@host — remote login. #SSH
- whoami / id — show current user / UID/GID. #whoami #id
- who / w / last — who is logged in / recent logins. #who #w #last
- loginctl list-sessions — systemd session list. #loginctl
- ps -u username / pkill -u username — list/kill user processes. #ps #pkill
- logout / exit / Ctrl-D — end a shell session. #logout
- getent passwd username — view passwd entry via NSS. #getent

Checks / quick facts:
- Where is the hashed password? /etc/shadow (requires root). #/etc_shadow
- How is shell set? 7th field in /etc/passwd. #/etc_passwd
- Which scripts run for login shell? /etc/profile then user's login scripts. #LoginShell
- How are GUI sessions started? Display manager (GDM/LightDM) spawns user session (X/Wayland). #GDM #LightDM
- How to force-logoff user processes? pkill -u username or killall -u username. #pkill

---

## Short Troubleshooting Tips
- Can't login remotely: test network + sshd status (systemctl status sshd). #sshd
- Wrong shell: check /etc/passwd entry; change with chsh. #chsh
- Env vars missing on GUI login: ensure display manager sources correct profile scripts. #Environment
- Persisting background processes after logout: check nohup, screen/tmux sessions, or systemd user services. #nohup #screen #tmux #systemd

---

Tags included for quick search: #Linux #login #session #authentication #SSH #TTY #GDM #LightDM #PAM #MFA #shell #Bash #startup-scripts #/etc_passwd #/etc_shadow #logout #processes #systemd #loginctl

