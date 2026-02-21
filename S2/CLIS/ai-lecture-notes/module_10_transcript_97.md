# Process coordination: parent/child, fork/wait/exec cheatsheet
#Keywords: #process #parent-child #fork #wait #waitpid #exec #execl #systemcall #orphan #ls

## Key Definitions (one-liners)
- Process: an executing program instance (address space + resources). #process  
- Parent process: the process that creates another via fork(). #parent-child  
- Child process: the new process created by fork(). #parent-child  
- fork(): system call that creates a child process (duplicate of parent). #fork  
- wait(): system call that makes a parent block until a child terminates. #wait  
- waitpid(): flexible wait allowing specific child selection and options. #waitpid  
- exec family: system calls that replace the current process image with a new program. #exec  
- execl(...): exec variant taking a path and a variable arg list (NULL-terminated). #execl  
- Orphan process: a child whose parent exited before it; adopted by init (or systemd). #orphan  
- System call: kernel-provided function invoked from user space. #systemcall

## Formulas / Signatures / Return semantics
- pid_t fork(void);
  - returns: >0 = child's PID (in parent), 0 = in child, -1 = error. #fork
- pid_t wait(int *status);
  - blocks until any child exits; returns child's PID, -1 on error. #wait
- pid_t waitpid(pid_t pid, int *status, int options);
  - can wait for specific child or use WNOHANG, etc. #waitpid
- int execl(const char *path, const char *arg0, ..., (char*)NULL);
  - on success: does not return; on error: returns -1 and sets errno. #execl #exec
- Exit status macros (from <sys/wait.h>):
  - WIFEXITED(status) — true if child exited normally.
  - WEXITSTATUS(status) — child's exit code (valid if WIFEXITED true).
  - WIFSIGNALED(status), WTERMSIG(status) — terminated by signal.

## Key Algorithms / Concepts (bulleted)
- Creating processes
  - Use fork() to create a child; both continue execution after fork. #fork
- Parent waiting for child
  - Use wait() to block until child finishes (prevents parent exiting early). #wait
  - Use waitpid() for non-blocking or targeting a PID (WNOHANG, WUNTRACED). #waitpid
- Running a different program in child
  - In child after fork, call an exec variant (execl, execv, execvp, etc.) to run a new program. #exec #execl
  - Example: child runs "ls -lh /home" via execl("/bin/ls", "ls", "-lh", "/home", (char*)NULL). #ls
- Parent/child lifecycle patterns
  - Parent waits -> child finishes -> parent continues.
  - Parent exits before child -> child becomes orphan (adopted by init). #orphan

## Important Properties / Invariants
- After fork:
  - Two processes exist with identical memory image (copy-on-write semantics usually). #fork
  - Distinguish by fork() return value: 0 in child, >0 in parent. #fork
- Exec semantics:
  - Exec replaces the calling process image; file descriptors may persist (unless O_CLOEXEC). #exec
  - On success exec() does not return; on failure returns -1 and sets errno. #execl
- Wait semantics:
  - wait() reaps terminated child and returns its PID and status; without wait, terminated child becomes a zombie until reaped. #wait
- Orphans:
  - Orphaned children are adopted by init (or equivalent), not automatically terminated. #orphan

## Quick Reference (scannable)
- Common fork/wait/execl pattern:
  - pid_t pid = fork();
    - if (pid < 0) -> error
    - if (pid == 0) { /* child */ execl("/bin/ls", "ls", "-lh", "/home", (char*)NULL); /* on error: exit */ }
    - else { /* parent */ wait(NULL); /* or waitpid(pid, &status, 0); */ }
- execl usage:
  - execl(path, argv0, arg1, ..., (char *)NULL);
  - argv0 conventionally set to program name (e.g., "ls"). #execl
- wait vs waitpid:
  - wait(NULL) -> block for any child.
  - waitpid(pid, &status, 0) -> block for specific child.
  - waitpid(pid, &status, WNOHANG) -> non-blocking.
- Exit/status handling:
  - if (WIFEXITED(status)) code = WEXITSTATUS(status);
  - if (WIFSIGNALED(status)) sig = WTERMSIG(status);
- Avoiding zombies:
  - Parent must call wait/waitpid (or set SIGCHLD handler with SIG_IGN on some systems).
- Common pitfalls:
  - Forgetting (char*)NULL terminator in execl -> undefined call behavior.
  - Calling exec in parent accidentally (do exec only in child).
  - Assuming exec returns; always check return for -1 (error).

## Short examples
- Run ls in child, parent waits:
  - pid = fork();
  - if (pid == 0) execl("/bin/ls","ls","-lh","/home",(char*)NULL);
  - else wait(NULL);

#Hashtags (all major items): #process #parent-child #fork #wait #waitpid #exec #execl #systemcall #orphan #ls

(Use this as a quick lookup during exam: signatures, return rules, common call patterns, and essential macros.)