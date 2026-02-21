# VA Editor / vi: Mark (Bookmark) Command — Cheatsheet
#hashtags: #vi #VAEditor #mark #marks #bookmark #bookmarks #navigation #cursor #delmarks #backtick #apostrophe #commands

## Key Definitions
- Mark / Bookmark: a named pointer set at a specific cursor location in a file.  
- Cursor position: exact character location where the cursor sits.  
- Mark name: single lowercase letter used to identify a mark (e.g., a, b, c).

## Command Syntax (Formulas / Equations)
- Set mark: m{letter}  (e.g., ma)
- Jump to mark: '{letter}  (apostrophe + letter)
- Jump to beginning of line of mark: `{letter}  (backtick + letter)
- Delete mark(s): :delmarks {name(s)}  (e.g., :delmarks a)

## Key Algorithms / Concepts
- Setting a mark:
  - Place cursor at desired location → press m then a lowercase letter (ma sets mark 'a').  
- Navigating to a mark:
  - Use apostrophe + letter to move cursor to the mark (e.g., 'a).  
- Jumping to the marked line start:
  - Use backtick + letter to jump to the beginning of the line where the mark is set (e.g., `a).  
- Deleting marks:
  - Use :delmarks followed by the mark name(s) to remove bookmarks.

## Important Properties / Invariants
- Marks are pointers created at the current cursor position when set.
- Mark names are single lowercase letters (per transcript example).
- Marks speed up navigation between different parts of a file.
- :delmarks removes specified mark(s).

## Quick Reference (Scannable)
| Action | Command | Example |
|---|---:|---|
| Set mark at cursor | m{letter} | ma  (set mark "a") |
| Move cursor to mark | '{letter} | 'a  (go to mark "a") |
| Jump to start of marked line | `{letter} | `a  (go to line start of mark "a") |
| Delete mark | :delmarks {name} | :delmarks a |

## Example Quick Workflow
- Move to line 10 → press ma (sets mark a).  
- Move elsewhere → press `a to jump back to beginning of the marked line (or 'a per navigation need).  
- Remove mark → :delmarks a

(Concise reference based on lecture transcript.)