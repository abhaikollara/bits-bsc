# Linux head — Quick Cheatsheet
#keywords: #head #linux #command #text-processing #filter #pipe #stdin #stdout #cat #glob #log #lines #bytes #options

## Key Definitions
- head: display the first part of files or stdin (default: first 10 lines). #head
- stdin / stdout: standard input / output streams. #stdin #stdout
- pipe (|): send stdout of one command as stdin to another. #pipe
- glob: wildcard filename expansion (e.g., *.log). #glob

## Syntax & Options (quick)
- Basic: head [OPTIONS] [FILE...]
- When no FILE given → reads from stdin (use with pipe). #stdin
- Options:
  - -n N, --lines=N : show first N lines (default N = 10). #lines #-n
  - -c K, --bytes=K : show first K bytes. #bytes #-c

## Key Algorithms / Concepts
- Preview file start: head file.txt (shows first 10 lines). #preview
- Specific lines: head -n 5 file.txt (first 5 lines). #-n
- Specific bytes: head -c 20 file.txt (first 20 bytes). #-c
- From pipeline: cat data.txt | head (head reads piped input). #pipe #cat
- Multiple files / globbing: head *.log → prints head of each file in turn, usually with filename headers between outputs. #glob #log

## Important Properties / Invariants
- Default output = first 10 lines if neither -n nor -c supplied. #default10
- -n and -c are mutually exclusive behaviors (choose lines or bytes). #mutual
- When reading multiple files, head outputs each file’s beginning sequentially (identifies files). #multifile
- head does not load entire file into memory — good for large files/logs. #scalable

## Quick Reference (scannable)
- Default: head file.txt → first 10 lines. #default10
- First N lines: head -n N file.txt or head --lines=N #-n
- First K bytes: head -c K file.txt or head --bytes=K #-c
- From pipe: somecmd | head → first 10 lines of somecmd output. #pipe
- Multiple files: head file1 file2 or head *.log → shows head for each file. #glob
- Use to: preview large files, inspect log headers, check file format/structure. #log #preview

## Examples
- head myfile.txt                → first 10 lines
- head -n 5 myfile.txt           → first 5 lines
- head -c 20 myfile.txt          → first 20 bytes
- cat data.txt | head -n 3       → first 3 lines of piped content
- head *.log                     → head of every .log file in directory

## Quick Tips
- Combine with other filters (grep, awk, tail) for targeted inspection. #grep #awk #tail
- Use head before processing large files to confirm format/headers. #safety
- Remember difference: head = start-of-file, tail = end-of-file. #tail

(Concise reference for open-book exams — quick lookup of syntax, options, and common usage.)