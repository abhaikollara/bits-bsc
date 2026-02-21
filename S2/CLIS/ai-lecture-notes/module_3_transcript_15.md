# File Permissions (Linux) — Cheatsheet
#hashtags: #filepermissions #linux #chmod #umask #ls #octal #symbolic #permissions #read #write #execute #filetypes #symlink #blockdevice #chardevice #pipe #socket #security

## Key Definitions (one-line)
- File permission: access rights (read/write/execute) controlling who can do what to a file/dir.  
- Owner (u): user who owns the file.  
- Group (g): group the owner belongs to.  
- Others (o): all other users.  
- Symbolic mode: chmod syntax using letters (u/g/o/a, +/−/=) and r/w/x.  
- Numeric (octal) mode: chmod using 3 octal digits (owner/group/others), each 0–7.  
- umask: mask subtracted from maximum permissions to get default new-file/dir perms.  
- Permission string: 10 chars: [type][owner(3)][group(3)][others(3)] (e.g., -rwxr-xr--).  
- File types chars: - regular, d directory, l symlink, b block device, c character device, p named pipe, s socket.

## Formulas / Notation
- Bit values: read = 4, write = 2, execute = 1.  
- Octal digit = sum(bits): 7=4+2+1 (rwx), 6=4+2 (rw-), 5=4+1 (r-x), 4=r--, 3=-wx, 2=-w-, 1=--x, 0=---.  
- Permission string length: 10 chars (1 type + 3x3 permission triads).  
- Default permissions = (max) − umask  
  - max for directories = 777; max for files = 666 (no execute by default).  
  - Example: umask 022 → dir default = 777−022 = 755; file default = 666−022 = 644.

## Key Commands / Syntax
- View permissions:  
  - ls -l  (long listing, shows permissions & ownership)  
  - ls -a  (include hidden files)  
  - ls -lah (long, human-readable sizes, show hidden)  
- Change permissions: chmod [MODE] FILE(S)  
  - Numeric: chmod 755 script.sh  → owner=rwx (7), group=r-x (5), others=r-x (5)  
  - Symbolic: chmod u+rwx,g-w,o=r file.txt  
    - u/g/o/a (user/group/others/all), + to add, - to remove, = to set exactly  
- umask: umask [MASK]  (set default mask; show with umask without args)

## Key Algorithms / Concepts (bulleted)
- #octal-encoding: encode each triad (u/g/o) to a digit 0–7 using 4/2/1 bits.  
- #symbolic-mode: modify specific classes without touching others (u/g/o/a with +/−/=).  
- #permission-string-interpretation: parse e.g. -rwxr-xr-- → owner=rwx (7), group=r-x (5), others=r-- (4) → 754.  
- #default-permissions: new files/dirs get (max − umask).  
- #execute-meaning: for files, allow running; for dirs, execute = traverse/search (required to enter/access contents).

## Important Properties / Invariants
- The three classes (u,g,o) are independent — changing one does not auto-change others unless using 'a' or explicit commands.  
- Numeric chmod sets all three classes at once (3-digit).  
- Symbolic chmod can be applied incrementally and combined (e.g., u+x,g-w).  
- umask only affects newly created files/directories, not existing ones.  
- For files, default max excludes execute (666); for directories include execute (777).  
- Incorrect permissions can cause security or availability issues — be cautious with 777 on dirs/files.

## Quick Reference (scan)
- Octal → perms:
  - 0 = ---  
  - 1 = --x  
  - 2 = -w-  
  - 3 = -wx  
  - 4 = r--  
  - 5 = r-x  
  - 6 = rw-  
  - 7 = rwx
- Common chmod shortcuts:
  - chmod 644 file.txt → rw- r-- r-- (owner rw, group read, others read)  
  - chmod 600 file.txt → rw- --- --- (private file)  
  - chmod 755 script.sh → rwx r-x r-x (owner can execute; others can read & execute)  
  - chmod 700 dir/ → rwx --- --- (private dir)
- Interpret permissions string:
  - Example: -rw-r--r-- → regular file, owner=rw(6), group=r(4), others=r(4) → chmod 644
  - Example: drwxr-xr-x → directory, owner=7, group=5, others=5 → chmod 755
- umask examples:
  - umask 022 → new file = 666−022 = 644; new dir = 777−022 = 755  
  - umask 077 → new file = 600; new dir = 700 (private)
- File type chars:
  - - regular file, d directory, l symlink, b block dev, c char dev, p named pipe (FIFO), s socket

## Example quick commands
- Show detailed, human sizes: ls -lah  
- Set file private: chmod 600 secret.txt  
- Make script executable: chmod +x run.sh  OR chmod 755 run.sh  
- Add execute for owner only: chmod u+x file  
- Remove read for group: chmod g-r file

Keep this sheet for quick lookup of bit mappings, command forms, and common presets.