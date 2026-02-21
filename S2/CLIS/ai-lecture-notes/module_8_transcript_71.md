# Shell Scripting — Cheatsheet
#hashtags: #shell #scripting #bash #sh #ksh #csh #tcsh #zsh #shebang #automation #backup #datacenter #ERP #GNUplot #bootscript #systemadmin

---

## Key Definitions
- Shell: command-line interpreter that runs user commands on Unix/Linux. #shell
- Shell script: a text file of shell commands treated as a single executable recipe. #scripting
- Shebang (hashbang): first-line marker that tells OS which interpreter to use (#!/path/to/shell). #shebang
- Interpreter: program that reads and executes script lines at runtime (not compiled). #interpreter
- Automation: using scripts to repeat, schedule, or compose system tasks without manual intervention. #automation

---

## Formulas / Syntax / Notation
- Shebang format:
  - #! /path/to/interpreter
  - Example: #!/bin/bash
- Execution model:
  - script-file -> shell-interpreter -> interpreted commands (no compile step)
- Simple repetition pattern (conceptual): run command N times (e.g., create users)
  - for user in userlist; do adduser $user; done

---

## Key Algorithms / Concepts
- Automation of repetitive tasks (backups, user creation, batch updates). #automation #backup
- Command composition: combine existing utilities into new commands/pipelines. #pipeline
- Scripts as single-entity commands: encapsulate lengthy command sequences. #encapsulation
- Use of functions in scripts to operate on datasets (cleaning, align fields). #function
- Data visualization by script-driven tools (e.g., gnuplot). #GNUplot
- Interpreted vs compiled: scripts are interpreted (easier to write/debug; no type declarations). #interpreter

---

## Common Shells (quick reference)
| Shell | Common path | Notes |
|---|---:|---|
| sh (Bourne) | /bin/sh | original Unix shell. #sh |
| bash (Bourne-Again) | /bin/bash | widely used on Linux (used in module). #bash |
| ksh (Korn) | /bin/ksh | Korn shell. #ksh |
| csh | /bin/csh | C-style shell. #csh |
| tcsh | /bin/tcsh | enhanced csh. #tcsh |
| zsh | /bin/zsh | feature-rich interactive shell. #zsh |

---

## Important Properties / Invariants
- Scripts are interpreted by the specified shell (via shebang). #shebang
- Scripts allow grouping many commands into one executable unit. #encapsulation
- Shells (traditional) have limited programming features compared to full languages:
  - limited single-command focus; only special combos otherwise. #limitations
  - limited/primitive support for strings and arrays (depends on shell). #limitations
- Easier to write and debug than many compiled programs due to no data-type declarations. #debugging
- Ideal for system admin tasks, repetitive workflows, startup/boot scripts, and batch maintenance. #systemadmin #bootscript

---

## Use Cases (scannable)
- Backup automation for high-frequency transactions (banks). #backup
- Bulk user creation and environment setup (ERP, LMS deployments). #ERP #LMS
- Server/service health monitoring, resource collection, capacity planning (data centers). #datacenter
- Boot scripts, application install/uninstall automation, batch updates. #bootscript
- Data preprocessing pipelines and plotting via external tools (gnuplot). #GNUplot

---

## Quick Reference (rules & patterns)
- When to use shell scripts:
  - repetitive OS-level tasks, orchestration of command-line utilities, simple text/file manipulation. #automation
- When NOT to rely solely on shell scripts:
  - heavy data-structure manipulation, complex string/array logic, performance-critical code (prefer higher-level language). #limitations
- Shebang must be first line to select interpreter; otherwise default interactive shell used. #shebang
- Scripts are executed by invoking interpreter or setting executable + invoking file:
  - chmod +x script.sh; ./script.sh
  - or: bash script.sh
- Create new commands by composing utilities (pipe |, redirect > >>). #pipeline
- Debugging tips:
  - run with -x for trace: bash -x script.sh
  - add set -e to exit on error (shell support permitting)

---

Keep this sheet handy during open-book exams for quick lookup of shell types, shebang usage, when to use shell scripts, and typical system-administration use cases.