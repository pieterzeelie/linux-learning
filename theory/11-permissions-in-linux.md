# Linux File Permissions

Linux permissions form the foundation of system security, controlling **who can read, write, or execute files and directories**.

---

## 🔑 Basic Permissions
- **Read (r):** View file contents / list directory files  
- **Write (w):** Modify file / add or delete files in a directory  
- **Execute (x):** Run a file as a program or enter a directory  

---

## 👥 Permission Groups
- **User (u):** Owner of the file  
- **Group (g):** Users in the assigned group  
- **Others (o):** All other users  
- **All (a):** Applies to user, group, and others  

---

## 🛠 Checking Permissions
- `ls -l filename` → shows permissions, owner, group, size, date  
- `namei -l /path/to/file` → breakdown of path permissions  
- `stat filename` → detailed file metadata  

---

## ✏️ Changing Permissions (`chmod`)
### Symbolic Notation
- `chmod u+x file` → add execute for user  
- `chmod g-w file` → remove write for group  
- `chmod o=r file` → set read-only for others  
- `chmod ug+rw,o-x file` → multiple changes at once  

### Octal Notation
- **r = 4, w = 2, x = 1**  
- Combine values per group (user/group/others):  
  - `chmod 755 file` → user: rwx (7), group: r-x (5), others: r-x (5)  
  - `chmod 644 file` → user: rw- (6), group: r-- (4), others: r-- (4)  

---

## 🔒 Special Permissions
- **Setuid (`chmod u+s file`)** → run with owner’s privileges  
- **Setgid (`chmod g+s dir`)** → files inherit group of directory  
- **Sticky bit (`chmod +t dir`)** → only owner can delete/rename inside directory  

---

## 👤 Ownership
- `chown user:group file` → change file owner/group  
- `chmod 755 file` → adjust permissions  

---

## 📌 Quick Reference
| Symbol | Meaning | Example |
|--------|---------|---------|
| `+`    | Add permission | `chmod g+x file` |
| `-`    | Remove permission | `chmod o-w file` |
| `=`    | Set exact permission | `chmod u=rwx file` |

---

## 🧮 Common Octal Values
| Value | User | Group | Others | Meaning |
|-------|------|-------|--------|---------|
| 777   | rwx  | rwx   | rwx    | Full access for everyone |
| 755   | rwx  | r-x   | r-x    | User full, group/others read+execute |
| 700   | rwx  | ---   | ---    | User full, no access for others |
| 644   | rw-  | r--   | r--    | User read+write, group/others read-only |
| 600   | rw-  | ---   | ---    | User read+write only |
| 400   | r--  | ---   | ---    | User read-only |

---

**Tip:** Always assign the minimum required permissions to reduce security risks.  

---

Source: [GeeksforGeeks – Linux Permissions](https://www.geeksforgeeks.org/linux-unix/set-file-permissions-linux/)