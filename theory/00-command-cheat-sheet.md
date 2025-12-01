# 📝 Linux command cheat sheet: Basic

<details>
<summary> 📂 list (ls) command</summary>
  
# Linux Cheat Sheet: 'ls' Command

| Command        | Description                                                                 | Example Output/Use Case                          |
|----------------|-----------------------------------------------------------------------------|--------------------------------------------------|
| `ls`           | List files and directories in current folder                                | `ls` → shows names only                          |
| `ls -1`        | Display one file per line                                                   | Easier to read when many files                   |
| `ls -l`        | Long listing: permissions, owner, size, date, filename                      | `-rw-r--r-- 1 user group 1234 Dec 1 file.txt`    |
| `ls -lh`       | Long listing with human‑readable sizes (KB, MB, GB)                         | `1.2K` instead of `1234`                         |
| `ls -ld`       | Show info about directory itself, not contents                              | `ls -ld /etc`                                    |
| `ls -t`        | Sort by modification time (newest first)                                    | `ls -t | head -1` → most recent file             |
| `ls -lt`       | Long listing sorted by modification time                                    | Shows details with newest files first            |
| `ls -ltr`      | Long listing sorted by modification time (oldest first)                     | Handy for logs/history                           |
| `ls -a`        | Show all files including hidden (`.` and `..`)                              | Reveals `.bashrc`, `.git`, etc.                  |
| `ls -A`        | Show hidden files but exclude `.` and `..`                                  | Cleaner hidden file view                         |
| `ls -R`        | Recursive listing (includes subdirectories)                                 | `ls -R /etc/apt` → lists all contents            |
| `ls -i`        | Show inode numbers                                                          | Useful for file system debugging                 |
| `ls -q`        | Hide control/non‑printable characters in names                              | Displays `?` instead of confusing characters     |
| `ls -n`        | Show numeric UID and GID instead of names                                   | `1000 1000` instead of `user group`              |
| `ls -F`        | Append symbols to classify files (`/` dir, `*` exec, `@` link)              | `script.sh*` → executable file                   |
| `ls --color=auto` | Color‑coded output (dirs in blue, links in green, files default color)   | Easier visual classification                     |
| `ls -l --time-style=long-iso` | Customize time format (YYYY-MM-DD HH:MM)                     | Useful for scripts and logs                      |
</details>

<details>
<summary> 📂 print working directory (pwd) command</summary>

# Linux Cheat Sheet: 'pwd' Command

| Command     | Description                          | Example Output        |
|-------------|--------------------------------------|-----------------------|
| `pwd`       | Prints current directory (logical).  | `/home/user/docs`     |
| `/bin/pwd`  | Prints physical path (no symlinks).  | `/var/logs`           |
| `pwd -L`    | Logical path (resolves symlinks).    | `/home/user/tmp_link` |
| `pwd -P`    | Physical path (actual directory).    | `/tmp`                |
| `echo $PWD` | Environment variable for directory.  | `/home/user/tmp_link` |

</details>

<details>  
<summary> 📂 make directory (mkdir) command</summary>

# Linux Cheat Sheet: 'mkdir' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `mkdir dir_name`         | Create a single directory in the current location.                         | `mkdir jayesh_gfg`                      | Creates `jayesh_gfg` in current path.          |
| `mkdir -v dir_name`      | Create directory with verbose output (shows confirmation message).          | `mkdir -v geeksforgeeks`                | "mkdir: created directory 'geeksforgeeks'"     |
| `mkdir dir1 dir2 dir3`   | Create multiple directories at once.                                        | `mkdir jayesh_gfg_1 jayesh_gfg_2`       | Creates all listed directories.                |
| `sudo mkdir dir_name`    | Create directory with root privileges (resolves permission denied errors).  | `sudo mkdir geeksforgeek`               | Prompts for root password if needed.           |
| `mkdir /path/to/dir`     | Create directory using absolute path.                                       | `mkdir /home/user/newdir`               | Creates `newdir` at specified path.            |
| `mkdir parent/child`     | Create directory using relative path (nested).                             | `mkdir my_folder/sub_folder`            | Creates `sub_folder` inside `my_folder`.       |
| `mkdir --help`           | Display help information for `mkdir`.                                      | `mkdir --help`                          | Shows usage guide.                             |
| `mkdir --version`        | Display version and license info.                                          | `mkdir --version`                       | Prints version details.                        |
| `mkdir -p path`          | Create parent directories as needed (no error if they already exist).       | `mkdir -p first/second/third`           | Creates full nested structure.                 |
| `mkdir -m mode dir_name` | Set permissions while creating directory (like `chmod`).                    | `mkdir -m 755 secure_dir`               | Creates `secure_dir` with `rwxr-xr-x` perms.   |
</details>

<details>
  
<summary> 📂 change directory (cd) command</summary>

# Linux Cheat Sheet: 'cd' Command

| Command / Option     | Description                                                   | Example Usage              | Example Output / Notes                          |
|-----------------------|---------------------------------------------------------------|----------------------------|------------------------------------------------|
| `cd dir_name`         | Change to a specific directory.                              | `cd Documents`             | Moves into `Documents` directory.              |
| `cd ..`               | Move up one directory level (parent directory).              | `cd ..`                    | From `/home/user/docs` → `/home/user`.         |
| `cd ../..`            | Move up two directory levels.                                | `cd ../..`                 | From `/home/user/docs` → `/home`.              |
| `cd /path/to/dir`     | Change using absolute path.                                  | `cd /var/log`              | Moves directly to `/var/log`.                  |
| `cd ~`                | Change to the home directory of the current user.            | `cd ~`                     | Goes to `/home/user`.                          |
| `cd`                  | Without arguments, defaults to home directory.               | `cd`                       | Equivalent to `cd ~`.                          |
| `cd -`                | Switch to the previous working directory.                    | `cd -`                     | Toggles between last two directories.          |
| `cd ~/dir_name`       | Change to a subdirectory inside home.                        | `cd ~/Downloads`           | Goes to `/home/user/Downloads`.                |
| `cd /`                | Change to the root directory.                                | `cd /`                     | Moves to `/`.                                  |
| `cd ./dir_name`       | Change to a subdirectory relative to current directory.      | `cd ./scripts`             | Goes to `scripts` inside current directory.    |
</details>

<details>
  
<summary> 📂 remove directory (rmdir) command</summary>

# Linux Cheat Sheet: 'rmdir' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `rmdir dir_name`         | Remove an empty directory.                                                  | `rmdir test_dir`                        | Deletes `test_dir` if empty.                   |
| `rmdir -v dir_name`      | Remove directory with verbose output (shows confirmation message).          | `rmdir -v sample_dir`                   | "rmdir: removing directory, 'sample_dir'"      |
| `rmdir dir1 dir2 dir3`   | Remove multiple empty directories at once.                                  | `rmdir dirA dirB dirC`                  | Deletes all listed empty directories.          |
| `rmdir -p path`          | Remove nested parent directories if they become empty.                      | `rmdir -p parent/child/grandchild`      | Removes `grandchild`, then `child`, then `parent` if empty. |
| `rmdir --ignore-fail-on-non-empty dir_name` | Ignore errors for non-empty directories (skips them silently). | `rmdir --ignore-fail-on-non-empty dirX` | Skips `dirX` if not empty, continues with others. |
| `rmdir --help`           | Display help information for `rmdir`.                                      | `rmdir --help`                          | Shows usage guide.                             |
| `rmdir --version`        | Display version and license info.                                          | `rmdir --version`                       | Prints version details.                        |
  
</details>

<details>
  
<summary> 📂 copy-paste (cp) command</summary>

# Linux Cheat Sheet: 'cp' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `cp source dest`         | Copy one file to another. Creates dest if not exists, overwrites if exists. | `cp a.txt b.txt`                        | Copies `a.txt` → `b.txt`.                      |
| `cp file1 file2 dir/`    | Copy multiple files into a directory.                                       | `cp a.txt b.txt c.txt new/`             | Files copied into `new/` directory.            |
| `cp -R src_dir dest_dir` | Copy directories recursively.                                               | `cp -R docs backup/`                    | Copies all files from `docs` into `backup/`.   |
| `cp -i src dest`         | Interactive mode. Prompts before overwriting.                              | `cp -i a.txt b.txt`                     | Asks confirmation before replacing `b.txt`.    |
| `cp -f src dest`         | Force copy. Deletes destination if needed, then copies.                     | `cp -f a.txt b.txt`                     | Overwrites `b.txt` without prompt.             |
| `cp -p src dest`         | Preserve file attributes (timestamps, ownership, permissions).              | `cp -p a.txt c.txt`                     | `c.txt` keeps original metadata.               |
| `cp *.ext dir/`          | Copy all files matching a pattern (wildcard).                              | `cp *.txt Folder1/`                     | Copies all `.txt` files into `Folder1/`.       |  
</details>

<details>
  
<summary> 📂 move/rename (mv) command</summary>

# Linux Cheat Sheet: 'mv' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `mv file1 file2`         | Rename a file (moves file1 → file2).                                       | `mv old.txt new.txt`                    | Renames `old.txt` to `new.txt`.                 |
| `mv file dir/`           | Move a file into a directory.                                              | `mv notes.txt Documents/`               | Moves `notes.txt` into `Documents/`.            |
| `mv file1 file2 dir/`    | Move multiple files into a directory.                                      | `mv a.txt b.txt c.txt backup/`          | Moves all files into `backup/`.                 |
| `mv -i src dest`         | Interactive mode. Prompts before overwriting.                              | `mv -i report.txt archive/`             | Asks confirmation before replacing existing file. |
| `mv -f src dest`         | Force move. Overwrites destination without prompt.                         | `mv -f data.csv backup/`                | Replaces existing file silently.                |
| `mv -n src dest`         | No-clobber. Prevents overwriting existing files.                           | `mv -n draft.txt archive/`              | Skips move if file already exists.              |
| `mv -v src dest`         | Verbose mode. Shows details of the move/rename operation.                   | `mv -v file.txt archive/`               | "renamed 'file.txt' → 'archive/file.txt'"       |
| `mv dir1 dir2`           | Rename or move a directory.                                                | `mv projects old_projects`              | Renames `projects` to `old_projects`.           |
| `mv *.ext dir/`          | Move all files matching a pattern (wildcard).                              | `mv *.log logs/`                        | Moves all `.log` files into `logs/`.            |  
</details>

<details>
  
<summary> 📂 remove file (rm) command</summary>

# Linux Cheat Sheet: 'rm' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `rm file_name`           | Remove a single file.                                                      | `rm test.txt`                          | Deletes `test.txt`.                             |
| `rm file1 file2 file3`   | Remove multiple files at once.                                             | `rm a.txt b.txt c.txt`                 | Deletes all listed files.                       |
| `rm -i file_name`        | Interactive mode. Prompts before deleting each file.                       | `rm -i data.txt`                       | Asks confirmation before deletion.              |
| `rm -f file_name`        | Force remove. Ignores nonexistent files and never prompts.                 | `rm -f temp.txt`                       | Deletes `temp.txt` without warning.             |
| `rm -r dir_name`         | Recursively remove a directory and its contents.                           | `rm -r old_dir`                        | Deletes `old_dir` and everything inside it.     |
| `rm -rf dir_name`        | Force recursive remove. Deletes directory and contents without prompts.    | `rm -rf project_dir`                   | Removes `project_dir` completely.               |
| `rm --help`              | Display help information for `rm`.                                         | `rm --help`                            | Shows usage guide.                              |
| `rm --version`           | Display version and license info.                                          | `rm --version`                         | Prints version details.                         |  
</details>

<details>
  
<summary> 📂 unix name (uname) command</summary>

# Linux Cheat Sheet: 'uname' Command

| Command / Option | Description                                      | Example Usage   | Example Output / Notes                  |
|------------------|--------------------------------------------------|-----------------|-----------------------------------------|
| `uname`          | Prints the kernel name.                          | `uname`         | `Linux`                                 |
| `uname -a`       | Prints all system information.                   | `uname -a`      | `Linux host 5.15.0-56-generic ...`      |
| `uname -s`       | Prints the kernel name.                          | `uname -s`      | `Linux`                                 |
| `uname -n`       | Prints the network node hostname.                | `uname -n`      | `myhost`                                |
| `uname -r`       | Prints the kernel release version.               | `uname -r`      | `5.15.0-56-generic`                     |
| `uname -v`       | Prints the kernel build version.                 | `uname -v`      | `#62-Ubuntu SMP Tue Sep 20 ...`         |
| `uname -m`       | Prints the machine hardware name (architecture). | `uname -m`      | `x86_64`                                |
| `uname -p`       | Prints the processor type (if available).        | `uname -p`      | `x86_64` or `unknown`                   |
| `uname -i`       | Prints the hardware platform (if available).     | `uname -i`      | `x86_64` or `unknown`                   |
| `uname -o`       | Prints the operating system.                     | `uname -o`      | `GNU/Linux`                             |
  
</details>

<details>
  
<summary> 📂 locate command</summary>

# Linux Cheat Sheet: locate Command

| Command / Option              | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|-------------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `locate filename`             | Search for a file by name using the prebuilt database.                      | `locate test.txt`                      | Lists all paths containing `test.txt`.         |
| `locate pattern`              | Search for files matching a pattern.                                        | `locate *.mp3`                         | Lists all `.mp3` files in the system.          |
| `locate -c pattern`           | Count the number of matching entries.                                       | `locate -c *.txt`                      | Prints total number of `.txt` files.           |
| `locate -i pattern`           | Case-insensitive search.                                                    | `locate -i Readme.txt`                 | Matches `Readme.txt`, `README.TXT`, etc.       |
| `locate -n number pattern`    | Limit the number of results returned.                                       | `locate -n 5 *.log`                    | Shows only first 5 `.log` files.               |
| `locate -r regex`             | Search using a regular expression.                                          | `locate -r '.*\.(jpg|png)$'`           | Finds all `.jpg` and `.png` files.             |
| `locate -q pattern`           | Quiet mode. Suppresses error messages.                                      | `locate -q myfile`                     | Returns results silently.                      |
| `locate -d path pattern`      | Use a specific database file instead of default.                            | `locate -d /custom/db myfile`          | Searches using `/custom/db`.                   |
| `updatedb`                    | Update the locate database (needed for recent changes to be searchable).    | `sudo updatedb`                        | Refreshes database with current filesystem.    |
  
</details>

<details>
  
<summary> 📂 touch command</summary>

# Linux Cheat Sheet: touch Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `touch file_name`        | Create an empty file if it doesn’t exist, or update timestamp if it does.  | `touch newfile.txt`                     | Creates `newfile.txt` or updates its timestamp. |
| `touch file1 file2`      | Create multiple files at once.                                             | `touch a.txt b.txt c.txt`               | Creates all listed files.                       |
| `touch -c file_name`     | Do not create file if it doesn’t exist; only update timestamp if present.  | `touch -c existing.txt`                 | Updates timestamp of `existing.txt`.            |
| `touch -a file_name`     | Change only the access time of the file.                                   | `touch -a notes.txt`                    | Updates access time of `notes.txt`.             |
| `touch -m file_name`     | Change only the modification time of the file.                            | `touch -m report.txt`                   | Updates modification time of `report.txt`.      |
| `touch -t [[CC]YY]MMDDhhmm[.ss] file` | Set specific access/modification time using timestamp format. | `touch -t 202512012200 file.txt`        | Sets time to Dec 1, 2025, 22:00.                |
| `touch -r ref_file file` | Use timestamp of another file as reference.                                | `touch -r old.txt new.txt`              | `new.txt` gets same timestamp as `old.txt`.     |
  
</details>

<details>
  
<summary> 📂 link (ln) command</summary>

# Linux Cheat Sheet: 'ln' Command

| Command / Option        | Description                                                                 | Example Usage                          | Example Output / Notes                          |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------|------------------------------------------------|
| `ln source target`       | Create a hard link to a file.                                              | `ln file1.txt file2.txt`                | `file2.txt` becomes a hard link to `file1.txt`. |
| `ln file dir/`           | Create a hard link inside a directory.                                     | `ln file.txt /home/user/links/`         | Creates hard link in `/home/user/links/`.       |
| `ln -b source target`    | Create a backup of target before linking.                                  | `ln -b file1.txt file2.txt`             | Backs up `file2.txt` before linking.            |
| `ln -f source target`    | Force link creation by removing existing destination.                      | `ln -f file1.txt file2.txt`             | Overwrites `file2.txt` with new link.           |
| `ln -i source target`    | Interactive mode. Prompts before overwriting.                              | `ln -i file1.txt file2.txt`             | Asks confirmation before replacing `file2.txt`. |
| `ln -n source target`    | Do not dereference symbolic links.                                         | `ln -n file1.txt symlink.txt`           | Treats `symlink.txt` as a file, not its target. |
| `ln -s source target`    | Create a symbolic (soft) link.                                             | `ln -s /home/user/docs report_link`     | `report_link` points to `/home/user/docs`.      |
| `ln -v source target`    | Verbose mode. Shows details of link creation.                              | `ln -v file1.txt file2.txt`             | Prints confirmation of link creation.           |
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

<details>
<summary> 📂 '' command</summary>
  
</details>

