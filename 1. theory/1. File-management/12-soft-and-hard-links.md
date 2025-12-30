# Soft and Hard Links in Linux/Unix

Links in Linux are pointers to files or directories, allowing multiple names to reference the same data.  
There are two types: **Hard Links** and **Soft (Symbolic) Links**.

---

## 🔗 Hard Links
- Share the **same inode** as the original file → point directly to the data on disk.
- File content remains accessible even if the original filename is deleted.
- Changes in one hard link are reflected in all linked files.
- **Limitations:**
  - Cannot span across different file systems.
  - Cannot be created for directories (to avoid recursive loops).
- **Command:**
  ```bash
  ln original.txt hardlink.txt
  ```
  Example:
  ```bash
  ls -l
  -rw-r--r-- 2 pieter devops 120 Dec  3 20:00 original.txt
  -rw-r--r-- 2 pieter devops 120 Dec  3 20:00 hardlink.txt
  ```

## 🪢 Soft (Symbolic) Links
- Work like shortcuts (contain a pathname to the target).
- Have a different inode from the original file.
- Can span across different file systems.
- If the original file is deleted or renamed, the symlink becomes dangling.
- Can link to directories.
- Command:

  ```bash
  ln -s /path/to/original.txt symlink.txt
  ```

## 📊 Soft vs Hard Links Comparison

| Feature             | Hard Link                  | Soft Link (Symlink)              |
|---------------------|----------------------------|----------------------------------|
| Inode               | Same as original           | Different inode                  |
| File system scope   | Same file system only      | Can cross file systems           |
| Directory linking   | Not allowed                | Allowed                          |
| If original deleted | Still accessible           | Becomes dangling                 |
| Size                | Same as original           | Size = length of target path     |
| Command             | `ln file linkname`         | `ln -s file linkname`            |                                                   






