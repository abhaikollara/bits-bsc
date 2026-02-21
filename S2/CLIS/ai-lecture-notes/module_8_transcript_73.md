# Bash Wildcards (Globbing) Cheatsheet
#keywords: #wildcards #glob #bash #shell #filematching #star #questionmark #brackets #negation #ranges #ls #quoting #escaping #dotfiles

## Key Definitions
- Wildcard (globbing): pattern characters the shell expands to matching filenames/pathnames. #wildcards #glob
- * (star): matches zero or more characters. #star
- ? (question mark): matches exactly one character. #questionmark
- [chars] (character class): matches exactly one character listed (e.g., [aeiou]). #brackets
- [!chars] or [^chars] (negation inside brackets): matches exactly one character not listed. #negation
- Range in brackets: [a-z] matches any single character in that range. #ranges
- Quoting/escaping: prevents shell expansion (e.g., '\*' or "*" or 'pattern'). #quoting #escaping
- Globbing vs Regex: glob patterns are simpler than regular expressions. #glob

## Formulas / Pattern Equivalents
- '*'  => matches 0..n characters (glob) — roughly equivalent to regex '.*'. #star
- '?'  => matches exactly 1 character — roughly regex '.'. #questionmark
- '[abc]' => matches exactly one of 'a' or 'b' or 'c' — regex '[abc]'. #brackets
- '[a-z]' => matches one character in inclusive range a..z. #ranges
- '[!abc]' or '[^abc]' => matches one character not in set — regex '[^abc]'. #negation

## Key Concepts / Usage
- Basic usage examples:
  - ls *.html -> list files ending with ".html". #ls #star
  - ls A*.html -> files starting with 'A' and ending with ".html". #star
  - ls project.?? -> files named "project." plus exactly two-character extension. #questionmark
  - ls [aeiou]* -> files starting with a vowel (a,e,i,o,u). #brackets
  - ls [!aeiou]* -> files starting with any character except listed vowels. #negation
  - ls [0-9]* -> files starting with a digit (range). #ranges
- Patterns match filenames, not arbitrary text — used by shell commands (ls, rm, cp, mv, etc.). #filematching
- Use quoting/escaping to treat wildcard characters literally (prevent expansion). #quoting #escaping

## Important Properties / Invariants
- '*' can match an empty string (zero characters). #star
- '?' always matches exactly one character. #questionmark
- Bracket expressions match exactly one character from the set or range. #brackets #ranges
- Negation ([!...] or [^...]) inside brackets matches any single character not in the set. #negation
- Globbing happens before the command runs (shell expands patterns to filenames). #glob
- If a pattern matches no files, behavior depends on shell options:
  - Bash default: pattern remains unchanged (or can be removed with nullglob). (Note: exam check: shell settings affect behavior.) #bash
- Leading dotfiles: patterns normally do NOT match filenames starting with '.' unless explicitly included (e.g., .*) or shell option shopt -s dotglob is set. #dotfiles

## Quick Reference (scannable)
- Pattern -> Meaning -> Example
  - * -> zero or more chars -> *.txt (all .txt files) #star
  - ? -> exactly one char -> file?.txt (file1.txt, fileA.txt) #questionmark
  - [abc] -> one of a,b,c -> [aeiou]* (starts with a vowel) #brackets
  - [!abc] -> not a,b,c -> [!aeiou]* (starts with non-vowel) #negation
  - [a-z] -> any lowercase letter a..z -> [A-Za-z]* (starts with any letter) #ranges
- Tips / Pitfalls
  - To list files literally named '*' or '?' use quoting: ls '*' or ls '\*'. #quoting #escaping
  - Use quotes to pass patterns to commands that should interpret them (e.g., find) without shell expanding. #quoting
  - Combine patterns: ls proj?.[ch] -> matches proj1.c, projA.h, etc. (#combine)
  - Ranges are inclusive and depend on locale for ordering. #ranges
  - For recursive matching, combine with find or use shell options (globstar ** in bash with shopt -s globstar). #globstar (note: advanced)

## Examples (compact)
- ls *.html -> all .html files #star
- ls A*.html -> files starting 'A' and ending '.html' #star
- ls project.?? -> two-character extension #questionmark
- ls [aeiou]* -> starts with vowel #brackets
- ls [!aeiou]* -> starts with non-vowel #negation
- ls [a-c]* -> starts with a, b, or c (range) #ranges

Keep this sheet nearby for quick pattern-to-behavior lookup during open-book exams.