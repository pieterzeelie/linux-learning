## Find Command in Linux – Summary

The find command in Linux is used to search for files and directories based on various criteria such as name, type, size, permissions, and modification time. Unlike locate, which relies on a prebuilt database, find performs real-time searches directly in the filesystem.

## Syntax

`find [path] [options] [expression]`

- Path: Starting directory for the search (e.g., `~/Documents`).\
- Options: Refine search (e.g., `-type` for files/directories).
- Expression: Criteria like filenames, sizes, or permissions.

## Common Use Cases

### 1. Find a Specific File
`find ./GFG -name sample.txt`
(Searches for sample `.txt` in the `GFG` directory.)

### 2. Search Files by Pattern
`find ./GFG -name "*.txt"` (Finds all `.txt` files in the directory.)

### 3. Find and Delete with Confirmation
`find ./GFG -name sample.txt -exec rm -i {} ;` (Prompts before deleting the file.)

### 4. Find Empty Files/Directories
`find ./GFG -empty` (Lists empty files and folders.)

### 5. Search by Permissions
`find ./GFG -perm 664` (Finds files with permission `664`.)

### 6. Display Directory Hierarchy
`find . -type d` (Shows all directories and subdirectories.)
`
### 7. Search Text Within Files
`find ./ -type f -name "*.txt" -exec grep 'Geek' {} ;` (Finds `.txt` files containing the word `Geek`.)

### 8. Find Files by Modification Time
`find /path/to/search -mtime -7` (Lists files modified in the last 7 days.)

### 9. Find Large Files (>100MB)
`find / -type f -size +100M` (Searches for files larger than 100MB.)

### 10. Find Files Modified in Last 24 Hours
`find ~ -type f -mtime -1` (Lists files modified in the last day.)

### 11. Find and Delete Temporary Files
`sudo find /tmp -type f -name "*.tmp" -exec rm {} ;` (Deletes `.tmp` files in `/tmp`.)

### 12. Limit Search Depth
`find . -maxdepth 2 -name "*.txt"` (Restricts search to two levels deep.)

### 13. Combine with Grep for Content Search
`find . -type f -exec grep -l "pattern" {} ;` (Finds files containing the word `pattern`.)
