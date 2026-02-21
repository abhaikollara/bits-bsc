# Linux commands: touch, tr, pr — Cheatsheet
#hashtags: #linux #shell #command #touch #tr #pr #file #timestamp #textstream #formatting #man

## Key Definitions
- touch: create an empty file or update file access/modify timestamps without changing content. #touch
- tr: translate, delete, or squeeze characters from a text stream (stdin → stdout). #tr #textstream
- pr: paginate/format text files for printing or screen display (adds headers, page breaks). #pr #formatting
- man: view manual page for a command (e.g., man touch). #man

## Syntax / Quick Reference Forms
- touch: touch [OPTION]... FILE...
  - example: touch newfile.txt
  - set timestamp: touch -d "YYYY-MM-DD HH:MM:SS" file
- tr: tr [OPTION] SET1 [SET2]
  - example: tr 'A-Z' 'a-z' < infile > outfile
- pr: pr [OPTION]... [FILE]...
  - example: pr -l 60 file.txt       (set 60 lines/page)
  - merge files: pr -m file1 file2

## Important Options (concise)
- touch
  - -c : do not create file if it does not exist (no error). #touch
  - -d STRING : use STRING as the new access and modification time. #touch
  - -t [[CC]YY]MMDDhhmm[.ss] : use specified timestamp (alternate format). #touch
- tr
  - -d : delete characters in SET1 (no translation). #tr
  - -s : squeeze repeated characters in SET1 to a single occurrence. #tr
  - -c : complement SET1 (operate on characters not in SET1). #tr
- pr
  - -l N : set page length to N lines (lines per page). #pr
  - -m : merge multiple files side-by-side into one page. #pr
  - -h STRING : use STRING as the page header. #pr
  - -t : omit headers and trailers (print only file contents). #pr

## Key Algorithms / Concepts (bullet)
- #touch
  - Create placeholder files quickly.
  - Update file timestamps for build systems / dependency tracking.
- #tr
  - Simple byte/character-wise transformations; works with stdin/stdout—use with redirection or pipes.
  - Typical uses: case conversion, removing characters, normalizing whitespace.
- #pr
  - Paginate for printing or readable screen output; useful to view files in page-sized chunks and to prepare multi-file printouts.

## Important Properties / Invariants
- touch does not change file contents; only timestamps (unless file is created empty). #touch
- tr operates on byte/character streams — it does not accept filenames directly (use redirection or pipes). #tr
- tr is single-character-set oriented; to transform ranges use ranges like 'A-Z' 'a-z' or POSIX classes like '[:digit:]'. #tr
- pr formats output into pages (headers, footers, page breaks) — it is not an editor. #pr

## Quick Reference (scannable)
- Create file: touch file.txt    #touch
- Update timestamp to now: touch file.txt    #touch
- Do not create if missing: touch -c file.txt    #touch
- Set specific time: touch -d "2023-08-01 12:34:56" file.txt    #touch
- Lowercase stream: tr 'A-Z' 'a-z' < in > out    #tr
- Delete digits: tr -d '[:digit:]' < in > out    #tr
- Squeeze spaces: tr -s ' ' < in > out    #tr
- Complement and delete: tr -cd '[:alnum:]\n' < in > out    (keep only alnum + newline)    #tr
- Paginate with 50 lines/page: pr -l 50 file.txt    #pr
- Merge files side-by-side: pr -m file1.txt file2.txt    #pr
- No headers/trailers: pr -t file.txt    #pr
- View help: man touch | man tr | man pr    #man

## Examples (one-liners)
- touch placeholder: touch .placeholder    #touch
- touch specific date: touch -d "2024-02-21 09:00:00" report.txt    #touch
- convert file to lowercase: cat file | tr 'A-Z' 'a-z' > file.lc    #tr
- remove all non-printing: tr -cd '\11\12\15\40-\176' < in > out    #tr
- print two files merged per page: pr -m chapter1.txt chapter2.txt | lp    #pr

Remember: use man <command> for full option lists and platform-specific details. #man #linux