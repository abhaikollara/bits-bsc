# Bash Arrays — Advanced Operations (cheatsheet)

Keywords: #bash #array #arrays #indexing #length #slice #slicing #unset #append #+= #iteration #for-loop #indices #sparse

## Key Definitions
- Array: ordered collection of string values indexed by integers (in Bash). #array
- Index: integer position of element; first element is index 0. #indexing
- Length: number of elements currently present (not max index). #length
- Slice: contiguous subarray copied from an array. #slice
- Append: add element(s) to end of array using +=. #append
- Unset: remove a single element or entire array (using unset). #unset
- Sparse array: array with missing indices (after unset of elements). #sparse
- Indices list: list of present keys/indices (useful for iteration). #indices

## Formulas / Notation (Bash)
- Get number of elements: ${#arr[@]}  — returns length. #length
- Get all values: ${arr[@]}  — expands to all elements. #array
- Get all indices: ${!arr[@]}  — expands to present indices. #indices
- Access element i: ${arr[i]}  — value at index i. #indexing
- Slice (copy): new=( "${arr[@]:start:length}" )  
  - start = starting index (0-based).  
  - length = number of elements to copy. #slice
- Append elements: arr+=(val1 val2 ...)  #append
- Assign element: arr[index]=value  #indexing
- Remove element: unset arr[index]  — removes single element (creates hole). #unset
- Remove entire array: unset arr  — deletes array completely. #unset

## Key Algorithms / Concepts (quick bullets)
- Iteration over indices:
  - for i in "${!arr[@]}"; do echo "$i ${arr[$i]}"; done  — index + value. #for-loop #indices
- Iteration over values:
  - for v in "${arr[@]}"; do echo "$v"; done  — values only. #for-loop
- Append multiple items:
  - arr+=( "csh" "ksh" "zsh" )  — adds items to end. #+=
- Delete element vs delete array:
  - unset arr[3]  — delete element at index 3 (sparse result).  
  - unset arr     — delete whole array. #unset
- Slice semantics:
  - Slicing produces a new array copy; original array remains unchanged. #slice
- Zero-based indexing reminder:
  - First element = index 0. #indexing

## Important Properties / Invariants
- ${#arr[@]} counts present elements, not the largest index.
- unset arr[i] removes the element but does not reindex remaining elements (creates sparse indices).
- ${!arr[@]} only lists present indices (skip holes).
- Slicing uses start + length; order preserved; result is a separate copy.
- arr+=(...) appends at next numeric index (if numeric indices used).
- Assigning arr[index]=value can create non-contiguous indices.

## Quick Reference (syntax & examples)
- Declare/initialize:
  - arr=( "bash" "sh" "csh" "ksh" "zsh" )  #init
- Get length:
  - ${#arr[@]}  → e.g., 5
- Access:
  - ${arr[0]}  → first element ("bash")
- Iterate indices & values:
  - for i in "${!arr[@]}"; do echo "$i : ${arr[$i]}"; done
- Iterate values:
  - for v in "${arr[@]}"; do echo "$v"; done
- Append elements:
  - arr+=( "csh" "ksh" "zsh" )
- Delete element:
  - unset arr[3]  # removes index 3
- Delete whole array:
  - unset arr
- Slice (copy elements 0..1):
  - high_level=( "${arr[@]:0:2}" )  # copies arr[0] and arr[1]
- List indices present:
  - echo "${!arr[@]}"  # e.g., 0 1 2 4 7

Keep this sheet for quick lookup of common bash array operations and syntax.