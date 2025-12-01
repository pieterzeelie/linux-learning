# 📝 Linux command cheat sheet: Basic

<details>
<summary> 📂 'ls' command</summary>
  
# 📂 Linux Cheat Sheet: 'ls' Command

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
<summary> 📂 'pwd' command</summary>

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
<summary> 📂 'mkdir' command</summary>
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

