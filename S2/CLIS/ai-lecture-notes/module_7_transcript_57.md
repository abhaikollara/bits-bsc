# Vi/vim: Undelete & Buffer Recovery — Cheatsheet
#keywords: #vi #vim #editor #undelete #undo #recover #registers #buffer #paste #yank #commands

## Key Definitions
- Undo (`u`): revert the last change.  
- Redo (`Ctrl-R`): reapply an undone change (vim).  
- Register: named temporary storage for deleted/yanked text (`"a`..`"z`, `"0`..`"9`).  
- Numbered registers (`"0`–`"9`): hold recent deletes/yanks in rotation.  
- Named registers (`"a`–`"z`): user-controlled storage for yanks/deletes.  
- Unnamed register (`""`): default register used by most delete/yank/paste commands.  
- Buffer: generic temporary area (in vi/vim, registers implement buffer storage for paste).

## Formulas / Syntax (quick patterns)
- Specify a register: `"x` where x ∈ {0-9, a-z}  
- Paste from register x: `"xp` (paste after cursor) or `"xP` (paste before cursor)  
- Yank (copy) into register x: `"x{yank-command}` (e.g., `"ayy` to yank a line into register a)  
- Undo: `u` (repeat `u` to undo multiple changes)  
- Redo (vim): `Ctrl-R`  
- Paste default: `p` (after), `P` (before)

## Key Commands / Concepts
- Undo last change:
  - `u` — undo last change (press repeatedly to step back through changes). #undo
  - (Lecture: `U` mentioned — historically restores whole line in original vi; behavior differs in modern vim). #U
- Paste last deleted/yanked text:
  - `p` — paste contents of unnamed/default register after cursor. #paste
  - `P` — paste before cursor. #paste
- Use registers to recover specific deleted text:
  - `"0p` or `"0P` — paste contents of register 0. #registers #numbered-registers
  - `"1p` — paste from register 1 (older deleted text). #registers
  - `"ap` — paste from named register a. #named-registers
- Yank (copy) to a named register:
  - `"xy{motion}` or `"xY` / `"x y` pattern — place selection into register x (e.g., `"ayy` to yank current line into `a`). #yank #registers
- Delete behavior and registers:
  - Deletes and yanks are stored in registers so you can paste them later. #recover

## Important Properties / Invariants
- Paste position:
  - `p` → after the cursor/selection.  
  - `P` → before the cursor/selection. #paste
- Register precedence (canonical behavior):
  - `"0` — most recent yank (only updated by yank commands). #numbered-registers
  - `"1` — most recent delete; `"2`..`"9` hold successively older deletes. #numbered-registers
  - Named registers (`"a`..`"z`) persist until overwritten by explicit use. #named-registers
  - Unnamed register receives the most recent delete/yank used by default commands. #unnamed-register
- Undo is sequential (stack-like): repeated `u` steps backward through change history. #undo

## Quick Reference (scannable)
- Undo last: `u` (#undo)
- Undo multiple: press `u` repeatedly (#undo)
- Redo (vim): `Ctrl-R` (#undo #redo)
- Paste default: `p` (after), `P` (before) (#paste)
- Paste from register: `"<register>p` or `"<register>P` (e.g., `"0p`, `"1p`, `"ap`) (#registers)
- Yank into register: `"<register>y{motion}` or `"<register>yy` (e.g., `"ayy`) (#yank #registers)
- Delete (stores into delete register): `d{motion}` — deleted text goes to numbered registers (#delete #registers)
- Inspect registers (vim): `:registers` or `:reg` — show register contents (#registers)
- Named registers are explicit; numbered rotate for deletes; `"0` reserved for last yank (#named-registers #numbered-registers)

## Examples (one-line)
- Undo last deletion: press `u`. #undo  
- Paste most recent delete (default): press `p`. #paste  
- Paste from register 0: `"0p`. #registers  
- Yank current line into register a, then paste it: `"ayy` then move cursor and `"ap`. #yank #named-registers

#tags: #vi #vim #undelete #undo #registers #buffer #paste #yank #commands

(Keep this sheet near your editor during the exam: quick commands above allow recovering deleted text and using registers to manage paste/recovery.)