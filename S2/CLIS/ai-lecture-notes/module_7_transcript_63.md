# Sort (Linux sort filter) — Cheatsheet
#hashtags: #sort #Linux #command-line #sorting #text-processing #options #r_option #n_option #k_option #u_option #f_option #o_option #case-insensitive #numeric-sort #field-sort #remove-duplicates

## Title
Sort filter (Linux) — reorder lines of text (ascending/descending), field/key-based, remove duplicates, case handling, save output

## Quick Syntax
- Basic: sort [options] [file...]
- Pipe: some-command | sort [options]
- Write to file: sort [options] input.txt
- Using -o: sort [options] input.txt -o sorted.txt
- Equivalent redirection: sort input.txt > sorted.txt

## Key Definitions (one-line)
- sort: command that rearranges lines of text in a file or stream.
- ascending order: default lexical order from smallest to largest.
- descending order: reverse of ascending (use -r).
- lexical (character) sort: compares characters (ASCII/locale).
- numeric sort: compares numeric values (use -n).
- key/field: a specified column/field within a line used as the sort key (use -k).
- case-sensitive: uppercase/lowercase considered different.
- case-insensitive: case ignored when comparing (use -f).
- duplicate line: identical entire lines; can be removed with -u.
- output file (-o): store sorted result into a file instead of stdout.

## Options (quick reference)
- -r : reverse sort order (descending) — #r_option #reverse
- -n : numeric sort (compare numbers, not strings) — #n_option #numeric-sort
- -k POS : sort by key/field POS (e.g., -k2 for second field) — #k_option #field-sort
- -u : unique — remove duplicate lines in output — #u_option #remove-duplicates
- -f : fold lower to upper — case-insensitive sort — #f_option #case-insensitive
- -o FILE : write result to FILE (like redirection) — #o_option #output
- (note) default field separator: whitespace (use -t to set a different delimiter)

## Examples (compact)
- sort file.txt
- sort -r file.txt
- sort -n numbers.txt
- sort -k2 data.txt              (sort by 2nd field)
- sort -t, -k3 file.csv         (specify delimiter , and sort by 3rd field)
- sort -f names.txt             (case-insensitive)
- sort -u duplicates.txt        (remove duplicate lines)
- sort input.txt -o sorted.txt

## Important Properties / Invariants
- Default sort is lexical/character-based (not numeric).
- -n changes comparison to numeric; without -n "10" < "2" (character order).
- -k causes the entire line to move with its key — lines remain intact.
- -u removes duplicate lines from the final sorted output.
- -f treats 'A' and 'a' as equal for sorting purposes.
- Options can be combined (e.g., sort -n -r -k2 file).

## Quick Reference Table

| Option | Meaning | Short example |
|--------|---------|----------------|
| (none) | Lexical ascending | sort file.txt |
| -r | Reverse (descending) | sort -r file.txt |
| -n | Numeric sort | sort -n nums.txt |
| -k pos | Sort by field/key pos | sort -k2 data.txt |
| -f | Case-insensitive | sort -f names.txt |
| -u | Remove duplicate lines | sort -u list.txt |
| -o FILE | Write output to FILE | sort input.txt -o out.txt |

## Common Patterns
- Sort and save: sort input.txt -o sorted.txt
- Sort numerically by 2nd field: sort -t ' ' -k2,2 -n file
- Remove duplicates after sorting: sort file | uniq  (or sort -u file)
- Pipeline usage: cmd | sort -k3 -n | head -n 10

## Tips (exam quick-facts)
- If numbers are treated oddly, add -n.
- If different cases mix order, use -f.
- To sort by a specific column, use -k and possibly -t for delimiter.
- To persist output use -o or shell redirection (>).
- Use combinations: sort -k2 -n -r -u (sort by field 2, numeric, reverse, unique).

End of cheatsheet.