# Advanced File Permissions in Linux

Linux provides three **special permissions** beyond the standard `rwx`: **SUID**, **SGID**, and **Sticky Bit**. These enhance control over file execution and directory access.

---

## 1. Set-User-ID (SUID)
- **Effect on files:** Executables run with the **file owner’s privileges** instead of the user executing them.
- **Common use case:** `passwd` command (needs elevated privileges).
- **Set SUID:**
  - Symbolic: `chmod u+s filename`
  - Octal: `chmod 4755 filename`
- **Indicator:** `s` replaces `x` in the owner’s execute field.
- **Remove SUID:** `chmod u-s filename`

---

## 2. Set-Group-ID (SGID)

### On Files
- Executables run with the **file’s group privileges**.
- **Set SGID:**
  - Symbolic: `chmod g+s filename`
  - Octal: `chmod 2755 filename`
- **Indicator:** `s` replaces `x` in the group’s execute field.
- **Remove SGID:** `chmod g-s filename`

### On Directories
- **New files inherit the directory’s group ownership** instead of the creator’s default group.
- Useful for **collaborative environments**.
- Example:
  ```bash
  sudo mkdir /shared
  chmod g+s /shared

---

## 3. Sticky bit

- Effect on directories: Only the file owner, directory owner, or root can delete/rename files, even if others have write permissions.
- Common use case: /tmp directory.
- Set Sticky Bit:
- Symbolic: `chmod +t directoryname`
- Octal: `chmod 1777 directoryname`
- Indicator: `t` replaces `x` in the others’ execute field.
- Remove Sticky Bit: `chmod -t directoryname`

## Permission Summary Table

| Permission | Symbolic | Effect on files | Effect on directories |
|---|---|---|---|
| SUID | chmod u+s | Executables run with file owner’s privileges | Not applicable |
| SGID | chmod g+s | Executables run with file group’s privileges | New files inherit the directory’s group |
| Sticky | chmod +t | Not applicable | Only owner/root can delete or rename within the directory |

Got it 👍 — you want the summary formatted in Markdown markup style so it’s copy‑paste ready for your GitHub notes. Here’s the cleaned version:


3. Sticky Bit
- 	Effect on directories: Only the file owner, directory owner, or root can delete/rename files, even if others have write permissions.
- 	Common use case:  directory.
- 	Set Sticky Bit:
- 	Symbolic: 
- 	Octal: 
- 	Indicator:  replaces  in the others’ execute field.
- 	Remove Sticky Bit: 


### Visual Indicators
- 	`s` (lowercase): Special permission set and execute permission present.
- 	`S` (uppercase): Special permission set but no execute permission.
- 	`t` (lowercase): Sticky bit set and execute permission present.
- 	`T` (uppercase): Sticky bit set but no execute permission.

### Key Takeaway
SUID, SGID, and Sticky Bit provide powerful access control beyond .
- 	SUID → Run executables with owner’s privileges.
- 	SGID → Ensure consistent group ownership in collaborative directories.
- 	Sticky Bit → Protect files in shared spaces.
Understanding and configuring these correctly is essential for secure system administration and multi-user environments.

Source: GeeksforGeeks – Advance File Permissions in Linux






