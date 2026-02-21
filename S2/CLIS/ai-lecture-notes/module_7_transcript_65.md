# Linux tail command — Cheatsheet
#keywords: #tail #linux #logfiles #monitoring #streaming #commandline #grep #textutils

## Key Definitions
- tail: displays the last part (end) of a file or stream.  
- follow (-f): keep reading and display new data appended to a file in real time.  
- line count (-n): show the last N lines of input.  
- byte count (-c): show the last N bytes of input.  
- log file: frequently-updated file where recent events/errors are appended to the end.

## Syntax / Short formulas
- Basic: tail [options] [file]  
- Common options: -n N (lines), -c N (bytes), -f (follow)  
- Default behavior: tail file → last 10 lines

## Key Commands & Examples
- tail file.txt
  - Output: last 10 lines (default)
- tail -n 2 file.txt
  - Output: last 2 lines
- tail -c 20 file.txt
  - Output: last 20 bytes
- tail -f logfile.log
  - Output: show end of file and continuously show new lines as they are added
- Combining with grep (filter + recent matches)
  - grep "error" logfile.log | tail -n 10
  - Output: last 10 lines that match "error"

## Key Concepts / Use Cases
- #monitoring: Observe real-time updates to logs (use -f).  
- #troubleshooting: Quickly view recent errors or events at file end.  
- #efficiency: View end of large files without reading entire file.  
- #composition: Pipe/chain with other commands (grep, awk, sed) for focused output.

## Important Properties / Invariants
- Default last-lines = 10.  
- -n and -c accept numeric arguments specifying what to return from file end.  
- -f causes tail to continue running and print appended data as it arrives.  
- tail is useful when recent updates are appended to file ends (typical for logs).

## Quick Reference (scannable)
- tail file                → last 10 lines  
- tail -n N file           → last N lines  
- tail -c N file           → last N bytes  
- tail -f file             → follow (show appended lines in real time)  
- grep "pattern" file | tail -n N  → last N matching lines  
- Use tail to: monitor logs, inspect recent entries, stream appended output

#tags: #tail #linux #logfiles #monitoring #grep #follow #lines #bytes #commandline