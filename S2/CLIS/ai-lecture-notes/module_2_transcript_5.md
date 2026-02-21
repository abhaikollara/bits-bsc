# File commands cheatsheet — Sort, Tail, cmp, diff
#hashtags: #linux #shell #file-commands #sort #tail #cmp #diff #text-processing #files

## Key Definitions
- sort: Sort lines of text (default: ascending, lexicographic).  
- tail: Show last part of a file (commonly last lines).  
- cmp: Compare two files byte-by-byte; reports first difference (byte & line).  
- diff: Show line-by-line differences between text files (various output formats).

## Syntax / quick examples
- sort: `sort filename`  
- tail: `tail -n <lines> filename` , `tail -f filename`  
- cmp: `cmp file1 file2`  
- diff: `diff file1 file2`

## Flags / Options (concise)
- sort
  - `-r` : reverse order (#reverse)  
  - `-n` : numeric sort (#numeric)  
  - `-u` : unique — output each line once (#unique)  
  - `-k <n>` : sort by field/column number (#field-sort)  
  - `-t <sep>` : set field separator for column-based sort (#separator)
- tail
  - `-n <N>` : show last N lines (#lines)  
  - `-f` : follow file as it grows (realtime) (#follow)
- cmp
  - `-l` : list byte differences with decimal values (#bytes)  
  - `-b` : show differing bytes in octal (#octal)  
  - `-i <N>` : skip first N bytes in both files before comparing (#skip)
  - Behavior: no output → files identical (per transcript)
- diff
  - `-c` : context format (#context)  
  - `-u` : unified format (#unified)  
  - `-r` : recursively compare directories (#recursive)

## Important properties / invariants
- sort does not modify the original file by default; it prints sorted output to stdout (transcript demo).  
- tail shows the last lines; `-f` streams updates without re-reading full file.  
- cmp reports the first differing byte and line number; useful for exact (byte) equality checks.  
- diff reports textual (line-level) differences and supports multiple output formats for patches/reads.  
- Skipping bytes in cmp (`-i`) shifts the comparison offset; first difference reported is after skip.

## Quick reference table
| Command | Purpose | Common flags | Typical use |
|---|---:|---|---|
| sort | Sort lines of a file | `-r`, `-n`, `-u`, `-k <n>`, `-t <sep>` | Sort by column, remove dupes |
| tail | Show last lines / follow file | `-n <N>`, `-f` | View recent log entries |
| cmp | Byte-by-byte file compare | `-l`, `-b`, `-i <N>` | Detect first byte difference |
| diff | Line-by-line differences | `-c`, `-u`, `-r` | Produce patches / compare directories |

## Quick patterns / rules to remember
- To view sorted output but keep file unchanged: `sort file` (redirect to overwrite if wanted). #sort  
- To view last 10 lines (default 10): `tail file` or specific: `tail -n 2 file`. #tail  
- Follow logs in realtime: `tail -f /var/log/syslog`. #tail #follow  
- Exact binary check: `cmp a b` — no output = identical (per lecture). #cmp  
- Skip first N bytes in cmp: `cmp -i N a b` (comparison starts at byte N+1). #cmp #skip  
- Human-friendly diff: `diff -u a b` (unified) — common for patches. #diff #unified

## Searchable hashtags (for exam lookup)
#linux #shell #file-commands #sort #tail #cmp #diff #text-processing #sorting #reverse #numeric #unique #field-sort #separator #lines #follow #bytes #octal #skip #context #unified #recursive

(Concise reference derived from lecture demo: sort, tail, cmp, diff — flags and behaviors above.)