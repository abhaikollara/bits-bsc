# Copying & Moving Files and Directories — Cheatsheet
#cp #mv #copy #move #recursive #-r #file #directory #rename #filesystem #Unix #Linux #command #shell #resource-intensive

## Key Definitions
- cp: copy command — copies files or directories (creates new file(s)).  
- mv: move command — moves or renames files/directories (does not create a duplicate).  
- source: path/name of file/dir to copy or move.  
- destination: path/name where the item will be copied/moved to.  
- recursive (-r): option to process directories and their contents recursively (required for directory copy).  
- rename: changing a file/dir name using mv (same directory).

## Syntax / Formulas
- cp [options] source... destination
- cp -r source_directory destination_directory
- mv source... destination
- mv old_name new_name  (rename)
- mv file target_directory  (move into target dir)

## Key Algorithms / Concepts
- #cp: copies single or multiple files; leaves original(s) intact.
- #cp -r: required to copy directories and their contents recursively.
- #mv: renames if destination is a name in same directory; moves if destination is a different directory.
- #rename: use mv old_name new_name (no duplicate created).
- Moving a directory into another: mv dir target_dir (result: dir becomes a child of target_dir).
- Conflict behavior (transcript): cannot rename/overwrite a file with a directory of the same name (operation will not be allowed).

## Important Properties / Invariants
- cp creates a separate copy; original remains.
- mv does not create a second copy when renaming within same filesystem/location — the item is moved/renamed.
- To copy directories, always use -r (cp without -r cannot copy directories).
- Moving into an existing directory places the item under that directory (not overwrite a file with a directory).
- Recursive copy/move of large data can be time-consuming and resource-intensive — use with caution.

## Quick Reference (scannable)
- Copy file to new filename (same directory)
  - cp 1.txt 2.txt  → creates 2.txt as a copy of 1.txt
- Copy file into directory (as same name)
  - cp 1.txt dir/1.txt  → copy 1.txt into dir (dir should exist)
- Copy directory recursively
  - cp -r dir1 dir2  → copies dir1 and its contents into dir2 (creates dir2/dir1 or copies into dir2 depending on usage)
- Rename file
  - mv old_name.txt new_name.txt  → old_name removed, new_name appears
- Move file into directory
  - mv 1.txt dir/  → 1.txt moved into dir
- Rename/move directory
  - mv dir2 dir3  → renames dir2 to dir3 (within same parent) or moves dir2 under dir3 if dir3 exists as directory
- Move directory into another directory
  - mv 3 1  → moves directory 3 as a child of directory 1

## Short Tips
- Use cp -r for directories (#recursive).  
- Use mv to rename without duplication (#rename).  
- Check destination path carefully: moves/renames are destructive to source (mv removes source).  
- Avoid recursive operations on very large directories unless necessary (resource/time cost).

