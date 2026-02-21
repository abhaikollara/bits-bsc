# Path-name to Inode (Linux) — Cheat Sheet
#hashtags: #inode #filesystem #path-resolution #directory #directory-entry #tokenization #traversal #metadata #root #inode-number #file-data

## Key Definitions
- inode: Index node; filesystem data structure holding file metadata and pointers to data blocks. #inode
- inode number: Unique identifier for each file/directory in the filesystem. #inode-number
- directory entry: Mapping from a name (string) → inode number stored in a directory. #directory-entry
- path tokenization: Splitting a path into components (tokens) e.g., /home/user/file -> ["home","user","file"]. #tokenization
- path resolution / traversal: Sequentially following directory entries from a start inode to reach the target inode. #path-resolution
- root inode: Starting inode for absolute paths (commonly inode 1). #root

## Formulas / Notation
- Let k = number of path components (tokens).
  - Path resolution time ∝ k (linear in path depth): T = O(k) (ignoring per-directory lookup cost). #complexity
- Directory lookup per component: cost depends on directory implementation (linear/hashed/B-tree) — overall resolution cost = Σ lookup_cost(component_i).

## Key Algorithms / Concepts
- Tokenize path
  - Remove leading “/”, split on “/” → sequence of name tokens. #tokenization
- Start at root inode (absolute path) or CWD inode (relative path). #root
- For each token in order:
  - Read current directory’s entries, find name → get inode number. #directory-entry #traversal
  - Set current inode = found inode; continue to next token.
- Stop when final token resolved → final inode represents file/dir. #inode
- Use final inode to:
  - Read metadata (permissions, ownership, timestamps). #metadata
  - Follow block pointers to access file data blocks. #file-data

## Important Properties / Invariants
- Each file/directory has exactly one inode number (unique). #inode-number
- Directories store name → inode mappings (directory entries). #directory-entry
- Absolute paths: traversal always starts at root inode. #root
- Resolution proceeds component-by-component; failure to find any component = path not found.
- After resolution, inode provides both metadata and pointers to data blocks (content access). #metadata #file-data

## Example (walkthrough)
- Path: /home/user/documents/file1.txt
- Tokenize → ["home", "user", "documents", "file1.txt"]
- Traverse:
  - start inode 1 (/)
  - lookup "home" in inode 1 → inode 10
  - lookup "user" in inode 10 → inode 20
  - lookup "documents" in inode 20 → inode 30
  - lookup "file1.txt" in inode 30 → inode 40 (final)
- Final: inode 40 → metadata + data blocks. #inode

## Quick Reference (scannable)
- Steps:
  1. Tokenize path → tokens[]
  2. Set current = root inode (absolute) or CWD inode (relative)
  3. For each token t:
     - lookup t in current directory → next_inode
     - if not found → error (ENOENT)
     - current = next_inode
  4. Result = current (final inode) → use for metadata/data access
- Common failures: missing component, permission denied while reading a directory, broken symlink (not covered here). #traversal
- Useful reminders:
  - inode contains metadata + block pointers. #inode #metadata
  - directories = special files that map names → inode numbers. #directory
  - resolution cost grows with path depth (k). #complexity

Keep this sheet near your notes for quick lookup during path-resolution problems.