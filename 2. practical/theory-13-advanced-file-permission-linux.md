# Practical Applications of Advanced File Permissions

## 1. SUID (Set-User-ID)

### Scenario
Allow normal users to run a program with **root privileges** (without giving them full root access).

### Example: `passwd` command
```bash
ls -l /usr/bin/passwd
```
Output:
```bash
-rwsr-xr-x 1 root root 54256 Dec  4 20:58 /usr/bin/passwd
```

## Custom Demo
```bash
# Create a simple script that shows current user
echo -e '#!/bin/bash\necho "Running as: $(whoami)"' > demo.sh
chmod 755 demo.sh

# Set SUID
sudo chown root demo.sh
sudo chmod u+s demo.sh

# Run as normal user
./demo.sh
```

Output:
```bash
Running as: root
```

## 2. SGID (Set-Group-ID)

### Scenario

Ensure files created in a shared directory inherit the group ownership of the directory.
Example: Shared project folder
```bash
# Create group and directory
sudo groupadd projectteam
sudo mkdir /shared_project
sudo chown :projectteam /shared_project
sudo chmod 2775 /shared_project   # SGID set

# Add users to group
sudo usermod -aG projectteam user1
sudo usermod -aG projectteam user2
```

Test : 

```bash
# As user1
cd /shared_project
touch file_by_user1.txt
ls -l
```

Output :
```bash
-rw-r--r-- 1 user1 projectteam 0 Dec  4 20:58 file_by_user1.txt
```

## 3. Sticky Bit
### Scenario

Prevent users from deleting each other’s files in a shared writable directory.

Example : `/tmp` directory
```bash
ls -ld /tmp
```

Output :
```bash
ls -ld /tmp
```

### Custom Demo

```bash
# Create shared directory
sudo mkdir /shared_tmp
sudo chmod 1777 /shared_tmp   # Sticky bit set

# User1 creates a file
su user1 -c "echo 'hello' > /shared_tmp/u1.txt"

# User2 tries to delete it
su user2 -c "rm /shared_tmp/u1.txt"
```

Output :
```bash
rm: cannot remove '/shared_tmp/u1.txt': Operation not permitted
```