# Arrays in Bash — Declaration, Initialization, Access, and Operations

Keywords: #array #bash #declare #declare-a #indexing #slicing #iteration #keys #assignment #compound-assignment #heterogeneous #no-multidim #access

## Key Definitions
- Array: ordered collection of elements addressed by numeric indices. #array  
- Bash array: an array in Bash (can be heterogeneous; no built-in multidimensional arrays). #bash #heterogeneous #no-multidim  
- Index / key: integer position of an element (first index = 0). #indexing  
- Element: a single value stored at an index.  
- declare -a: explicitly declares a variable as an array. #declare  
- Compound assignment: assigning multiple elements at once using parentheses and optional explicit indices. #compound-assignment

## Formulas / Notation
- Indexing base: first element index = 0  
- Slice syntax (start,length): ${array[@]:start:length} — e.g., to get indices 2–4 use ${array[@]:2:3}  
- Time (common): access O(1), iterate O(n) (informational, not from transcript)

## Key Syntax & Examples (quick)
- Declare empty array:
  - declare -a arr
- Indexed assignment:
  - arr[0]=val
  - arr[3]=x
- Compound / list initialization:
  - arr=(a b c d)         # indexes 0..3
  - arr=( [0]=a [2]=c )   # explicit indices
- No spaces around assignment:
  - WRONG: arr = (a b)
  - RIGHT: arr=(a b)
- Access single element:
  - ${arr[2]}              # element at index 2
- First element shortcuts:
  - ${arr[0]} or ${arr}    # both yield first element
- All elements:
  - ${arr[@]} or ${arr[*]} # expand all elements
- Slice / range:
  - ${arr[@]:start:length} # e.g., ${arr[@]:2:3} -> indexes 2,3,4
- Keys / indices:
  - ${!arr[@]} or ${!arr[*]}  # list of indices (0-based)
- Iteration:
  - for v in "${arr[@]}"; do ...; done

## Key Algorithms / Concepts (bulleted)
- Declaration: use declare -a name to explicitly declare an array. #declare  
- Initialization methods:
  - Indexed assignment (arr[index]=value). #assignment  
  - Compound/list assignment (arr=(elem1 elem2 ...)). #compound-assignment  
- Access patterns:
  - Single element by index. #access  
  - All elements via @ or *. #access #slicing  
  - Range/slice via ${arr[@]:start:length}. #slicing  
  - Keys via ${!arr[@]}. #keys  
- Iteration: use for-loops over ${arr[@]}. #iteration  
- Variable index: use a variable as an index (e.g., i=2; echo ${arr[$i]}). #indexing

## Important Properties / Invariants
- Indexing starts at 0 (first element stored at index 0). #indexing  
- Bash arrays may contain mixed-type elements — no homogeneous-type requirement. #heterogeneous  
- Bash does not natively support multidimensional arrays. #no-multidim  
- Use declare -a to make intention explicit (not required but recommended). #declare  
- No spaces around the = when assigning arrays.  
- ${arr} (unindexed) is equivalent to ${arr[0]} in many contexts (first element). #access  
- ${arr[@]} vs ${arr[*]}: both expand all elements; behavior differs when quoted ( informational ). #access

## Quick Reference (scannable)
- declare array:
  - declare -a myarr
- init (list):
  - myarr=(1 2 3 4)
- init (indexed):
  - myarr[0]=1
  - myarr[4]=9
- print element i:
  - echo "${myarr[i]}"
- print first element:
  - echo "${myarr[0]}" or echo "${myarr}"
- print all elements:
  - echo "${myarr[@]}"    # or "${myarr[*]}"
- slice indices 2–4:
  - echo "${myarr[@]:2:3}"
- print all keys/indices:
  - echo "${!myarr[@]}"
- iterate:
  - for v in "${myarr[@]}"; do echo "$v"; done
- common mistakes:
  - Do not put spaces around = in assignments.
  - Expectation of multidimensional arrays — Bash does not support them natively.

Hashtags (major): #array #bash #declare #indexing #slicing #iteration #keys #assignment #compound-assignment #heterogeneous #no-multidim

(Use this sheet as a quick lookup for Bash array operations and common syntaxes.)