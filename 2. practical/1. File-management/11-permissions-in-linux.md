## 🖥️ Practical Permission Examples (Project Files)

### 1. Protecting Configuration Files
```bash
# Set config.env so only I can read/write
chmod 600 config.env
ls -l config.env
```
Output:
```bash
-rw------- 1 pieter devops  120 Dec  3 19:30 config.env
```

### 2. Securing Deployemnt Script
```bash
# Make deploy.sh executable only by me
chmod 700 deploy.sh
ls -l deploy.sh
```
Output: 
```bash
-rwx------ 1 pieter devops  512 Dec  3 19:31 deploy.sh
```

### 3. Shared Project Directory
```bash
# Allow group members to collaborate
chmod 775 project_dir
ls -ld project_dir
```
Output:
```bash
drwxrwxr-x 2 pieter devops 4096 Dec  3 19:32 project_dir
```

### 4. Web server files
```bash
# Public HTML file: editable by me, readable by all
chmod 644 index.html
ls -l index.html
```
Output:
```bash
-rw-r--r-- 1 pieter devops  980 Dec  3 19:33 index.html
```

### 5. Logs and Temporary Files
```bash
# Logs readable by admins, hidden from others
chmod 640 app.log
ls -l app.log
```
Output:
```bash
-rw-r----- 1 pieter devops 2048 Dec  3 19:34 app.log
```

### 6. Sticky bit for shared Directory
```bash
# Prevent others from deleting my files in /tmp
chmod +t /tmp
ls -ld /tmp
```
Output:
```bash
drwxrwxrwt 10 root root 4096 Dec  3 19:35 /tmp
```

### 7. Setgid for Team Projects
```bash
# Ensure new files inherit group ownership
chmod g+s project_dir
ls -ld project_dir
```
Output:
```bash
drwxrwsr-x 2 pieter devops 4096 Dec  3 19:36 project_dir
```
