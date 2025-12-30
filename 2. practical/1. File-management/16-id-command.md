## Real-life Exercises

### 1. Check Your Own Identity
See your UID, GID, and groups.
`id`

### 2. Create a New User and Inspect Their IDs
```bash
sudo useradd testuser
id testuser
```

### 3. Compare Real vs Effective IDs
Run a command with sudo and compare:
```bash
id -u
sudo id -u
```

### 4. Check Group Membership for Permission Troubleshooting
Useful when debugging file access issues.  
`id -G pieter`

### 5. Display Only Names (Human‑Readable)
```bash
id -nu
id -ng
id -nG
```

###  6. Create a Group and Add a User — Then Verify
```bash
sudo groupadd devteam
sudo usermod -aG devteam testuser
id testuser
```

### 7. Inspect SELinux Context (If on RHEL/CentOS)
`id -Z`

### 8. Script‑Friendly Output
Use only numeric IDs for automation:
```bash
id -u
id -g
id -G
```



