# Linux Shell Cheatsheet

#hashtags
#LinuxShell #terminal #terminal_emulator #GNOMEterminal #KDEconsole #xterm #Bash #Zsh #Fish #prompt #root #user #absolute_path #relative_path #paths #slash #tab_completion #command_history

## Title
Linux Shell — terminals, shell types, prompts, paths, tab completion (quick exam reference)

## Key Definitions
- Linux Shell: Command-line interface to execute commands and manage system resources. #LinuxShell  
- Terminal emulator: GUI program that provides an interface to a shell (e.g., GNOME Terminal). #terminal_emulator  
- Shell types: Implementations of the shell command interpreter (Bourne Again Shell/Bash, Z shell/Zsh, Fish). #Bash #Zsh #Fish  
- Prompt: Visible shell cue; indicates user type and readiness for input. #prompt  
- Root (superuser): System administrator account (prompt ends with #). #root  
- Regular user: Normal account (prompt typically ends with $). #user  
- Absolute path: Full path from root (starts at /). #absolute_path  
- Relative path: Path relative to current directory (does not start with /). #relative_path  
- Tab completion: Press Tab to auto-complete commands, options, filenames, or list possible matches. #tab_completion  
- Command history: Previously run commands accessible via up/down arrow keys. #command_history

## Formulas / Notation
- Path separator: /  (UNIX-style) #slash  
- Absolute path example: /home/user/documents/fite.dxt  (#absolute_path)  
- Relative path example (from /home/user): documents/fite.dxt  (#relative_path)  
- Prompt symbols: Regular user -> ends with $ ; Root -> ends with #  (#prompt #root #user)

## Key Algorithms / Concepts
- Terminal ↔ Shell: Terminal emulator (GNOME Terminal, KDE Console, xterm) hosts the shell. #terminal_emulator #GNOMEterminal #KDEconsole #xterm  
- Shell types:
  - Bash (Bourne Again Shell): common default shell. #Bash  
  - Zsh: extended features over Bash. #Zsh  
  - Fish: interactive-friendly, syntax highlighting & autocompletion. #Fish  
- Prompt detection: Use trailing symbol to infer user type ($ = regular, # = root). #prompt #root #user  
- Path addressing:
  - Absolute path: start with / (root) and list full directories to file. #absolute_path  
  - Relative path: from current working directory; shorter and context-sensitive. #relative_path  
- Tab completion behavior:
  - Single match -> completes text.  
  - Multiple matches -> lists possible options for selection. #tab_completion  
- Command history navigation: Up/Down arrow to scroll previous commands; re-run or edit. #command_history

## Important Properties / Invariants
- / is the directory separator in Linux paths. #slash  
- Absolute paths start with /; relative paths do not. #absolute_path #relative_path  
- Prompt trailing character indicates privilege: $ (regular), # (root). #prompt  
- Tab completion speeds typing and reduces errors; ambiguous prefixes show choices. #tab_completion  
- Terminal emulator only provides UI; the shell actually interprets commands. #terminal_emulator

## Quick Reference (scannable)
- Terminals: GNOME Terminal | KDE Console | xterm  (#GNOMEterminal #KDEconsole #xterm)  
- Shells: Bash | Zsh | Fish  (#Bash #Zsh #Fish)  
- Prompt symbols:
  - user: ...$  (#user)  
  - root: ...#  (#root)  
- Path rules:
  - Absolute: starts with / → /path/to/file  (#absolute_path)  
  - Relative: from current dir → path/to/file  (#relative_path)  
  - Separator: /  (#slash)  
- Tab completion:
  - Hit Tab while typing command/filename/options  
  - Single completion → auto-fill  
  - Multiple → list choices  (#tab_completion)  
- Command history: Up-arrow = previous command, Down-arrow = next command  (#command_history)

Keep this sheet for quick lookup of shell types, prompt conventions, and path/addressing basics during open-book exams.