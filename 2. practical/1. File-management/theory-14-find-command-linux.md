## Practical Applications

### Backup Important Files
```bash
find ~/Documents -name "*.docx" -mtime -30 -exec cp {} ~/Backup/ \;
```
Copies all .docx files modified in the last 30 days from Documents to a Backup folder.

### Clean Up Log Files Older Than 90 Days
```bash
find /var/log -type f -name "*.log" -mtime +90 -exec rm {} \;
```
Deletes log files older than 90 days to free up disk space.

### Find Large Media Files
```bash
find ~/Media -type f \( -iname "*.mp4" -o -iname "*.mkv" \) -size +500M 
```
Lists all video files larger than 500MB in the Media directory.

### Find and Compress Old Files
```bash
find ~/Projects -type f -mtime +365 -exec gzip {} \;
```
Compresses files not modified in over a year to save space.

### Find Broken Symbolic Links
```bash
find /usr/local/bin -xtype l
```
Lists broken symbolic links in `/usr/local/bin`

### Find Files Owned by a Specific Use
```bash
find /home -user pieter
```
Finds all files owned by user `pieter` in the home directory.


### Find Files with Specific Permissions and Change Them
```bash
find ~/Scripts -type f -perm 777 -exec chmod 755 {} \;
```
Finds files with overly permissive permissions and tightens them.

### Generate a List of Recently Modified Files for Review
```bash
find ~/Work -type f -mtime -7 -printf "%TY-%Tm-%Td %TT %p\n" > recent_changes.txt
```
Creates a timestamped list of files modified in the last week.


