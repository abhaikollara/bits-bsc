# File & Directory Permissions (Unix/Linux) — Cheatsheet

#keywords
#permissions #ownership #file #directory #rwx #octal #chmod #chown #chgrp #setuid #setgid #stickybit #user #group #others #superuser

---

## Key Definitions (one-line)
- Owner: user who owns a file/directory.  
- Group: group associated with a file; group members get group permissions.  
- Others: all users not owner or in group.  
- Permission bits: read (r), write (w), execute (x).  
- Symbolic notation: e.g., rwx r-x r-- (owner / group / others).  
- Octal notation: 3-digit mode like 755 (owner/group/others) or 4-digit with special bits.  
- setuid: special bit causing executable to run with file-owner privileges.  
- setgid: special bit causing executable to run with file-group privileges (or directories inherit group).  
- sticky bit: on a directory, restricts deletion to file owner, directory owner, or superuser.  
- Superuser (root): has overriding privileges.

---

## Formulas / Mappings
- Permission bit values: r = 4, w = 2, x = 1  
- Octal digit = sum of bits present (e.g., rw- = 4+2 = 6)  
- Standard mode: OWNER (hundreds) | GROUP (tens) | OTHERS (ones)  
  - Example: 755 -> owner=7 (rwx), group=5 (r-x), others=5 (r-x)  
- Special (leading) octal bits: setuid = 4, setgid = 2, sticky = 1  
  - Example: 4755 -> setuid + 755

---

## Key Commands & Concepts
- chmod (change mode / permissions)
  - Symbolic: chmod u+r file.txt (add read to owner)  
  - Symbolic multi: chmod g-w,o-w file.txt (remove write from group & others)  
  - Octal: chmod 644 file.txt
  - Special bits: chmod u+s file (setuid symbolically), chmod g+s dir (setgid)
- chown (change owner and/or group)
  - Usage: chown new_owner file; chown new_owner:new_group file
- chgrp (change group only)
  - Usage: chgrp new_group file
- Permission sets: three groups — owner / group / others (#rwx)
- Special bits:
  - #setuid: executable runs with file-owner privileges
  - #setgid: executable runs with file-group privileges; on directories causes group inheritance
  - #stickybit: on directories, controls who can delete/rename files inside

---

## Important Properties & Invariants
- Permission order always: owner, group, others.  
- Symbolic operators: + (add), - (remove), = (set exactly).  
- Octal → symbolic mapping is deterministic via r=4, w=2, x=1.  
- setuid/setgid affect effective privileges during execution, not file contents.  
- Sticky bit only meaningful on directories for deletion control.  
- Owner (or root) can change a file's permissions with chmod; changing ownership (chown) typically requires appropriate privileges (often root).  
- File execute + setuid/setgid: display as 's' (if execute bit set) or 'S' (if execute not set) in ls -l; sticky shown as 't' or 'T'.

---

## Quick Reference (scannable)
- Permission letters: r = read, w = write, x = execute
- Bit values: r=4, w=2, x=1 → octal digit = sum
- Common modes:
  - 755 -> rwx r-x r-x (owner full, others/read+exec)
  - 644 -> rw- r-- r-- (owner read/write, others read)
  - 700 -> rwx --- --- (owner only)
  - 600 -> rw- --- --- (owner read/write only)
- Special bits (leading digit):
  - 4--- : setuid
  - 2--- : setgid
  - 1--- : sticky
  - Example: 2755 -> setgid + 755 (directory inherits group)
- ls -l symbols:
  - owner exec position: 's' (setuid+exec), 'S' (setuid only)  
  - group exec position: 's' (setgid+exec), 'S' (setgid only)  
  - others exec position on dir: 't' (sticky+exec), 'T' (sticky only)
- Examples:
  - chmod u+r file.txt — add read for owner (#chmod #symbolic)  
  - chmod 644 file.txt — set rw- r-- r-- (#chmod #octal)  
  - chown alice file.txt — change owner to alice (#chown)  
  - chown alice:devs file.txt — owner alice, group devs (#chown #chgrp)  
  - chgrp devs file.txt — change group to devs (#chgrp)
- Deletion rules in sticky directory:
  - Only file owner, directory owner, or superuser can remove files (#stickybit)

---

Tags for quick search: #permissions #ownership #rwx #octal #chmod #chown #chgrp #setuid #setgid #stickybit #owner #group #others

--- 

Keep this sheet nearby during open-book exams for quick lookup of commands, octal-symbolic mappings, and special-bit behavior.