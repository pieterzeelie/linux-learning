<details>
<summary><span style="font-size:1.5em; font-weight:bold;">📝 Linux command cheat sheet: Basic</summary>

<details>
<summary> 📂 list (ls) command</summary>
  
# Linux Cheat Sheet: `ls` Command

| Command                       | Description                                                            | Example Output/Use Case                       |
| ----------------------------- | ---------------------------------------------------------------------- | --------------------------------------------- |
| `ls`                          | List files and directories in current folder                           | `ls` → shows names only                       |
| `ls -1`                       | Display one file per line                                              | Easier to read when many files                |
| `ls -l`                       | Long listing: permissions, owner, size, date, filename                 | `-rw-r--r-- 1 user group 1234 Dec 1 file.txt` |
| `ls -lh`                      | Long listing with human‑readable sizes (KB, MB, GB)                    | `1.2K` instead of `1234`                      |
| `ls -ld`                      | Show info about directory itself, not contents                         | `ls -ld /etc`                                 |
| `ls -t`                       | Sort by modification time (newest first)                               | `ls -t                                        |
| `ls -lt`                      | Long listing sorted by modification time                               | Shows details with newest files first         |
| `ls -ltr`                     | Long listing sorted by modification time (oldest first)                | Handy for logs/history                        |
| `ls -a`                       | Show all files including hidden (`.` and `..`)                         | Reveals `.bashrc`, `.git`, etc.               |
| `ls -A`                       | Show hidden files but exclude `.` and `..`                             | Cleaner hidden file view                      |
| `ls -R`                       | Recursive listing (includes subdirectories)                            | `ls -R /etc/apt` → lists all contents         |
| `ls -i`                       | Show inode numbers                                                     | Useful for file system debugging              |
| `ls -q`                       | Hide control/non‑printable characters in names                         | Displays `?` instead of confusing characters  |
| `ls -n`                       | Show numeric UID and GID instead of names                              | `1000 1000` instead of `user group`           |
| `ls -F`                       | Append symbols to classify files (`/` dir, `*` exec, `@` link)         | `script.sh*` → executable file                |
| `ls --color=auto`             | Color‑coded output (dirs in blue, links in green, files default color) | Easier visual classification                  |
| `ls -l --time-style=long-iso` | Customize time format (YYYY-MM-DD HH:MM)                               | Useful for scripts and logs                   |

</details>

<details>
<summary> 📂 print working directory (pwd) command</summary>

# Linux Cheat Sheet: `pwd` Command

| Command     | Description                         | Example Output        |
| ----------- | ----------------------------------- | --------------------- |
| `pwd`       | Prints current directory (logical). | `/home/user/docs`     |
| `/bin/pwd`  | Prints physical path (no symlinks). | `/var/logs`           |
| `pwd -L`    | Logical path (resolves symlinks).   | `/home/user/tmp_link` |
| `pwd -P`    | Physical path (actual directory).   | `/tmp`                |
| `echo $PWD` | Environment variable for directory. | `/home/user/tmp_link` |

</details>

<details>  
<summary> 📂 make directory (mkdir) command</summary>

# Linux Cheat Sheet: `mkdir` Command

| Command / Option         | Description                                                                | Example Usage                     | Example Output / Notes                       |
| ------------------------ | -------------------------------------------------------------------------- | --------------------------------- | -------------------------------------------- |
| `mkdir dir_name`         | Create a single directory in the current location.                         | `mkdir jayesh_gfg`                | Creates `jayesh_gfg` in current path.        |
| `mkdir -v dir_name`      | Create directory with verbose output (shows confirmation message).         | `mkdir -v geeksforgeeks`          | "mkdir: created directory 'geeksforgeeks'"   |
| `mkdir dir1 dir2 dir3`   | Create multiple directories at once.                                       | `mkdir jayesh_gfg_1 jayesh_gfg_2` | Creates all listed directories.              |
| `sudo mkdir dir_name`    | Create directory with root privileges (resolves permission denied errors). | `sudo mkdir geeksforgeek`         | Prompts for root password if needed.         |
| `mkdir /path/to/dir`     | Create directory using absolute path.                                      | `mkdir /home/user/newdir`         | Creates `newdir` at specified path.          |
| `mkdir parent/child`     | Create directory using relative path (nested).                             | `mkdir my_folder/sub_folder`      | Creates `sub_folder` inside `my_folder`.     |
| `mkdir --help`           | Display help information for `mkdir`.                                      | `mkdir --help`                    | Shows usage guide.                           |
| `mkdir --version`        | Display version and license info.                                          | `mkdir --version`                 | Prints version details.                      |
| `mkdir -p path`          | Create parent directories as needed (no error if they already exist).      | `mkdir -p first/second/third`     | Creates full nested structure.               |
| `mkdir -m mode dir_name` | Set permissions while creating directory (like `chmod`).                   | `mkdir -m 755 secure_dir`         | Creates `secure_dir` with `rwxr-xr-x` perms. |

</details>

<details>
  
<summary> 📂 change directory (cd) command</summary>

# Linux Cheat Sheet: `cd` Command

| Command / Option  | Description                                             | Example Usage    | Example Output / Notes                      |
| ----------------- | ------------------------------------------------------- | ---------------- | ------------------------------------------- |
| `cd dir_name`     | Change to a specific directory.                         | `cd Documents`   | Moves into `Documents` directory.           |
| `cd ..`           | Move up one directory level (parent directory).         | `cd ..`          | From `/home/user/docs` → `/home/user`.      |
| `cd ../..`        | Move up two directory levels.                           | `cd ../..`       | From `/home/user/docs` → `/home`.           |
| `cd /path/to/dir` | Change using absolute path.                             | `cd /var/log`    | Moves directly to `/var/log`.               |
| `cd ~`            | Change to the home directory of the current user.       | `cd ~`           | Goes to `/home/user`.                       |
| `cd`              | Without arguments, defaults to home directory.          | `cd`             | Equivalent to `cd ~`.                       |
| `cd -`            | Switch to the previous working directory.               | `cd -`           | Toggles between last two directories.       |
| `cd ~/dir_name`   | Change to a subdirectory inside home.                   | `cd ~/Downloads` | Goes to `/home/user/Downloads`.             |
| `cd /`            | Change to the root directory.                           | `cd /`           | Moves to `/`.                               |
| `cd ./dir_name`   | Change to a subdirectory relative to current directory. | `cd ./scripts`   | Goes to `scripts` inside current directory. |

</details>

<details>
  
<summary> 📂 remove directory (rmdir) command</summary>

# Linux Cheat Sheet: `rmdir` Command

| Command / Option                            | Description                                                        | Example Usage                           | Example Output / Notes                                      |
| ------------------------------------------- | ------------------------------------------------------------------ | --------------------------------------- | ----------------------------------------------------------- |
| `rmdir dir_name`                            | Remove an empty directory.                                         | `rmdir test_dir`                        | Deletes `test_dir` if empty.                                |
| `rmdir -v dir_name`                         | Remove directory with verbose output (shows confirmation message). | `rmdir -v sample_dir`                   | "rmdir: removing directory, 'sample_dir'"                   |
| `rmdir dir1 dir2 dir3`                      | Remove multiple empty directories at once.                         | `rmdir dirA dirB dirC`                  | Deletes all listed empty directories.                       |
| `rmdir -p path`                             | Remove nested parent directories if they become empty.             | `rmdir -p parent/child/grandchild`      | Removes `grandchild`, then `child`, then `parent` if empty. |
| `rmdir --ignore-fail-on-non-empty dir_name` | Ignore errors for non-empty directories (skips them silently).     | `rmdir --ignore-fail-on-non-empty dirX` | Skips `dirX` if not empty, continues with others.           |
| `rmdir --help`                              | Display help information for `rmdir`.                              | `rmdir --help`                          | Shows usage guide.                                          |
| `rmdir --version`                           | Display version and license info.                                  | `rmdir --version`                       | Prints version details.                                     |

</details>

<details>
  
<summary> 📂 copy-paste (cp) command</summary>

# Linux Cheat Sheet: `cp` Command

| Command / Option         | Description                                                                 | Example Usage               | Example Output / Notes                       |
| ------------------------ | --------------------------------------------------------------------------- | --------------------------- | -------------------------------------------- |
| `cp source dest`         | Copy one file to another. Creates dest if not exists, overwrites if exists. | `cp a.txt b.txt`            | Copies `a.txt` → `b.txt`.                    |
| `cp file1 file2 dir/`    | Copy multiple files into a directory.                                       | `cp a.txt b.txt c.txt new/` | Files copied into `new/` directory.          |
| `cp -R src_dir dest_dir` | Copy directories recursively.                                               | `cp -R docs backup/`        | Copies all files from `docs` into `backup/`. |
| `cp -i src dest`         | Interactive mode. Prompts before overwriting.                               | `cp -i a.txt b.txt`         | Asks confirmation before replacing `b.txt`.  |
| `cp -f src dest`         | Force copy. Deletes destination if needed, then copies.                     | `cp -f a.txt b.txt`         | Overwrites `b.txt` without prompt.           |
| `cp -p src dest`         | Preserve file attributes (timestamps, ownership, permissions).              | `cp -p a.txt c.txt`         | `c.txt` keeps original metadata.             |
| `cp *.ext dir/`          | Copy all files matching a pattern (wildcard).                               | `cp *.txt Folder1/`         | Copies all `.txt` files into `Folder1/`.     |

</details>

<details>
  
<summary> 📂 move/rename (mv) command</summary>

# Linux Cheat Sheet: `mv` Command

| Command / Option      | Description                                               | Example Usage                  | Example Output / Notes                            |
| --------------------- | --------------------------------------------------------- | ------------------------------ | ------------------------------------------------- |
| `mv file1 file2`      | Rename a file (moves file1 → file2).                      | `mv old.txt new.txt`           | Renames `old.txt` to `new.txt`.                   |
| `mv file dir/`        | Move a file into a directory.                             | `mv notes.txt Documents/`      | Moves `notes.txt` into `Documents/`.              |
| `mv file1 file2 dir/` | Move multiple files into a directory.                     | `mv a.txt b.txt c.txt backup/` | Moves all files into `backup/`.                   |
| `mv -i src dest`      | Interactive mode. Prompts before overwriting.             | `mv -i report.txt archive/`    | Asks confirmation before replacing existing file. |
| `mv -f src dest`      | Force move. Overwrites destination without prompt.        | `mv -f data.csv backup/`       | Replaces existing file silently.                  |
| `mv -n src dest`      | No-clobber. Prevents overwriting existing files.          | `mv -n draft.txt archive/`     | Skips move if file already exists.                |
| `mv -v src dest`      | Verbose mode. Shows details of the move/rename operation. | `mv -v file.txt archive/`      | "renamed 'file.txt' → 'archive/file.txt'"         |
| `mv dir1 dir2`        | Rename or move a directory.                               | `mv projects old_projects`     | Renames `projects` to `old_projects`.             |
| `mv *.ext dir/`       | Move all files matching a pattern (wildcard).             | `mv *.log logs/`               | Moves all `.log` files into `logs/`.              |

</details>

<details>
  
<summary> 📂 remove file (rm) command</summary>

# Linux Cheat Sheet: `rm` Command

| Command / Option       | Description                                                             | Example Usage          | Example Output / Notes                      |
| ---------------------- | ----------------------------------------------------------------------- | ---------------------- | ------------------------------------------- |
| `rm file_name`         | Remove a single file.                                                   | `rm test.txt`          | Deletes `test.txt`.                         |
| `rm file1 file2 file3` | Remove multiple files at once.                                          | `rm a.txt b.txt c.txt` | Deletes all listed files.                   |
| `rm -i file_name`      | Interactive mode. Prompts before deleting each file.                    | `rm -i data.txt`       | Asks confirmation before deletion.          |
| `rm -f file_name`      | Force remove. Ignores nonexistent files and never prompts.              | `rm -f temp.txt`       | Deletes `temp.txt` without warning.         |
| `rm -r dir_name`       | Recursively remove a directory and its contents.                        | `rm -r old_dir`        | Deletes `old_dir` and everything inside it. |
| `rm -rf dir_name`      | Force recursive remove. Deletes directory and contents without prompts. | `rm -rf project_dir`   | Removes `project_dir` completely.           |
| `rm --help`            | Display help information for `rm`.                                      | `rm --help`            | Shows usage guide.                          |
| `rm --version`         | Display version and license info.                                       | `rm --version`         | Prints version details.                     |

</details>

<details>
  
<summary> 📂 unix name (uname) command</summary>

# Linux Cheat Sheet: `uname` Command

| Command / Option | Description                                      | Example Usage | Example Output / Notes             |
| ---------------- | ------------------------------------------------ | ------------- | ---------------------------------- |
| `uname`          | Prints the kernel name.                          | `uname`       | `Linux`                            |
| `uname -a`       | Prints all system information.                   | `uname -a`    | `Linux host 5.15.0-56-generic ...` |
| `uname -s`       | Prints the kernel name.                          | `uname -s`    | `Linux`                            |
| `uname -n`       | Prints the network node hostname.                | `uname -n`    | `myhost`                           |
| `uname -r`       | Prints the kernel release version.               | `uname -r`    | `5.15.0-56-generic`                |
| `uname -v`       | Prints the kernel build version.                 | `uname -v`    | `#62-Ubuntu SMP Tue Sep 20 ...`    |
| `uname -m`       | Prints the machine hardware name (architecture). | `uname -m`    | `x86_64`                           |
| `uname -p`       | Prints the processor type (if available).        | `uname -p`    | `x86_64` or `unknown`              |
| `uname -i`       | Prints the hardware platform (if available).     | `uname -i`    | `x86_64` or `unknown`              |
| `uname -o`       | Prints the operating system.                     | `uname -o`    | `GNU/Linux`                        |

</details>

<details>
  
<summary> 📂 locate command</summary>

# Linux Cheat Sheet: `locate` Command

| Command / Option           | Description                                                              | Example Usage                  | Example Output / Notes                      |
| -------------------------- | ------------------------------------------------------------------------ | ------------------------------ | ------------------------------------------- |
| `locate filename`          | Search for a file by name using the prebuilt database.                   | `locate test.txt`              | Lists all paths containing `test.txt`.      |
| `locate pattern`           | Search for files matching a pattern.                                     | `locate *.mp3`                 | Lists all `.mp3` files in the system.       |
| `locate -c pattern`        | Count the number of matching entries.                                    | `locate -c *.txt`              | Prints total number of `.txt` files.        |
| `locate -i pattern`        | Case-insensitive search.                                                 | `locate -i Readme.txt`         | Matches `Readme.txt`, `README.TXT`, etc.    |
| `locate -n number pattern` | Limit the number of results returned.                                    | `locate -n 5 *.log`            | Shows only first 5 `.log` files.            |
| `locate -r regex`          | Search using a regular expression.                                       | `locate -r '.\*\.(jpg\|png)$'` | Finds all `.jpg` and `.png` files.          |
| `locate -q pattern`        | Quiet mode. Suppresses error messages.                                   | `locate -q myfile`             | Returns results silently.                   |
| `locate -d path pattern`   | Use a specific database file instead of default.                         | `locate -d /custom/db myfile`  | Searches using `/custom/db`.                |
| `updatedb`                 | Update the locate database (needed for recent changes to be searchable). | `sudo updatedb`                | Refreshes database with current filesystem. |

</details>

<details>
  
<summary> 📂 touch command</summary>

# Linux Cheat Sheet: `touch` Command

| Command / Option                      | Description                                                               | Example Usage                    | Example Output / Notes                          |
| ------------------------------------- | ------------------------------------------------------------------------- | -------------------------------- | ----------------------------------------------- |
| `touch file_name`                     | Create an empty file if it doesn’t exist, or update timestamp if it does. | `touch newfile.txt`              | Creates `newfile.txt` or updates its timestamp. |
| `touch file1 file2`                   | Create multiple files at once.                                            | `touch a.txt b.txt c.txt`        | Creates all listed files.                       |
| `touch -c file_name`                  | Do not create file if it doesn’t exist; only update timestamp if present. | `touch -c existing.txt`          | Updates timestamp of `existing.txt`.            |
| `touch -a file_name`                  | Change only the access time of the file.                                  | `touch -a notes.txt`             | Updates access time of `notes.txt`.             |
| `touch -m file_name`                  | Change only the modification time of the file.                            | `touch -m report.txt`            | Updates modification time of `report.txt`.      |
| `touch -t [[CC]YY]MMDDhhmm[.ss] file` | Set specific access/modification time using timestamp format.             | `touch -t 202512012200 file.txt` | Sets time to Dec 1, 2025, 22:00.                |
| `touch -r ref_file file`              | Use timestamp of another file as reference.                               | `touch -r old.txt new.txt`       | `new.txt` gets same timestamp as `old.txt`.     |

</details>

<details>
  
<summary> 📂 link (ln) command</summary>

# Linux Cheat Sheet: `ln` Command

| Command / Option      | Description                                           | Example Usage                       | Example Output / Notes                          |
| --------------------- | ----------------------------------------------------- | ----------------------------------- | ----------------------------------------------- |
| `ln source target`    | Create a hard link to a file.                         | `ln file1.txt file2.txt`            | `file2.txt` becomes a hard link to `file1.txt`. |
| `ln file dir/`        | Create a hard link inside a directory.                | `ln file.txt /home/user/links/`     | Creates hard link in `/home/user/links/`.       |
| `ln -b source target` | Create a backup of target before linking.             | `ln -b file1.txt file2.txt`         | Backs up `file2.txt` before linking.            |
| `ln -f source target` | Force link creation by removing existing destination. | `ln -f file1.txt file2.txt`         | Overwrites `file2.txt` with new link.           |
| `ln -i source target` | Interactive mode. Prompts before overwriting.         | `ln -i file1.txt file2.txt`         | Asks confirmation before replacing `file2.txt`. |
| `ln -n source target` | Do not dereference symbolic links.                    | `ln -n file1.txt symlink.txt`       | Treats `symlink.txt` as a file, not its target. |
| `ln -s source target` | Create a symbolic (soft) link.                        | `ln -s /home/user/docs report_link` | `report_link` points to `/home/user/docs`.      |
| `ln -v source target` | Verbose mode. Shows details of link creation.         | `ln -v file1.txt file2.txt`         | Prints confirmation of link creation.           |

</details>

<details>

<summary> 📂 concatenate (cat) command</summary>

# Linux `cat` Command Cheat Sheet

| Command / Option                    | Description                                             | Example                                     |
| ----------------------------------- | ------------------------------------------------------- | ------------------------------------------- |
| `cat file_name`                     | View the content of a single file                       | `cat jayesh.txt`                            |
| `cat file1 file2`                   | View contents of multiple files sequentially            | `cat file1 file2`                           |
| `cat > newfile`                     | Create a new file and add content (overwrite if exists) | `cat > jayesh1`                             |
| `cat file1 file2 > merged.txt`      | Concatenate multiple files into one                     | `cat file1.txt file2.txt > merged_file.txt` |
| `cat -n file_name`                  | Display file contents with line numbers                 | `cat -n file2`                              |
| `cat -s file_name`                  | Suppress repeated empty lines                           | `cat -s file2`                              |
| `cat file1 >> file2`                | Append contents of one file to another                  | `cat file1 >> file2`                        |
| `tac file_name`                     | Display file contents in reverse order                  | `tac file2`                                 |
| `cat -E file_name`                  | Highlight end of each line with `$`                     | `cat -E jayesh1`                            |
| `cat -A file_name`                  | Show non-printing chars, line ends, and tabs (`-vET`)   | `cat -A filename`                           |
| `cat -- -dashfile`                  | Open files starting with a dash                         | `cat -- -jayesh2`                           |
| `cat file1 \| more`                 | View long files page by page                            | `cat file2 \| more`                         |
| `cat file1 file2 file3 > merged123` | Merge multiple files into one                           | `cat file1 file2 file3 > merged123`         |
| `cat *.txt`                         | Display contents of all `.txt` files in folder          | `cat *.txt`                                 |
| `cat >> file_name`                  | Append new text to an existing file                     | `cat >> geeks.txt`                          |

## Other Useful Options

| Option | Description                                                      |
| ------ | ---------------------------------------------------------------- |
| `-b`   | Number only non-empty lines                                      |
| `-T`   | Show TAB characters as `^I`                                      |
| `-v`   | Make non-printing characters visible (except tabs & line breaks) |
| `-u`   | Force unbuffered output (useful for real-time devices)           |

</details>

<details>

<summary> 📂 clear command</summary>

# Linux `clear` Command Cheat Sheet

| Command / Option | Description                                               | Example                 |
| ---------------- | --------------------------------------------------------- | ----------------------- |
| `clear`          | Clears the terminal screen, removing all previous output  | `clear`                 |
| `clear -x`       | Clears the screen but keeps the current line at the top   | `clear -x`              |
| `clear -V`       | Displays the version of the `clear` command               | `clear -V`              |
| `clear --help`   | Shows help information and available options              | `clear --help`          |
| `Ctrl + L`       | Keyboard shortcut to clear the terminal (same as `clear`) | _(press keys directly)_ |

## Notes

- `clear` does not delete command history; you can still scroll back with **Shift + PageUp/PageDown**.
- Useful for keeping your workspace tidy during long sessions.

</details>

<details>

<summary> 📂 running processes (ps) command</summary>

# Linux Cheat Sheet: `ps` Command

| Command / Option   | Description                                              | Example Usage    | Example Output / Notes                         |
| ------------------ | -------------------------------------------------------- | ---------------- | ---------------------------------------------- |
| `ps`               | Show processes for the current shell.                    | `ps`             | Lists PID, TTY, TIME, CMD for current session. |
| `ps -A`            | Display all running processes.                           | `ps -A`          | Shows every process on the system.             |
| `ps -a`            | Display processes from all users except session leaders. | `ps -a`          | Lists processes not tied to terminals.         |
| `ps -u`            | Display processes by a specific user.                    | `ps -u username` | Shows processes owned by `username`.           |
| `ps -x`            | Display processes not attached to a terminal.            | `ps -x`          | Includes background daemons.                   |
| `ps -e`            | Equivalent to `ps -A`, shows all processes.              | `ps -e`          | Lists all processes.                           |
| `ps -ef`           | Full-format listing of all processes.                    | `ps -ef`         | Shows UID, PID, PPID, start time, command.     |
| `ps -l`            | Long format listing for current shell.                   | `ps -l`          | Includes priority, flags, and other details.   |
| `ps -u` (with PID) | Detailed info about a specific process ID.               | `ps -u 1234`     | Shows details for process with PID 1234.       |
| `ps -aux`          | BSD style listing of all processes with detailed info.   | `ps -aux`        | Displays CPU%, MEM%, STAT, etc.                |
| `ps -C cmd`        | Show processes by command name.                          | `ps -C firefox`  | Lists all `firefox` processes.                 |
| `ps --help`        | Display help information for `ps`.                       | `ps --help`      | Shows usage guide.                             |

</details>

<details>

<summary> 📂 manual page (man) command</summary>

# Linux Cheat Sheet: `man` Command

| Command / Option      | Description                                                         | Example Usage   | Example Output / Notes                        |
| --------------------- | ------------------------------------------------------------------- | --------------- | --------------------------------------------- |
| `man command`         | Display the manual page for a command.                              | `man ls`        | Shows documentation for `ls`.                 |
| `man -f command`      | Show a short description (same as `whatis`).                        | `man -f ls`     | "ls (1) - list directory contents"            |
| `man -k keyword`      | Search manual pages for a keyword (same as `apropos`).              | `man -k copy`   | Lists all commands related to "copy".         |
| `man section command` | Display manual page from a specific section.                        | `man 5 passwd`  | Shows file format info from section 5.        |
| `man -a command`      | Display all manual pages matching the command, one after another.   | `man -a intro`  | Shows multiple `intro` pages across sections. |
| `man -w command`      | Show the location of the manual page file instead of displaying it. | `man -w ls`     | Prints path to the `ls` man page file.        |
| `man --help`          | Display help information for `man`.                                 | `man --help`    | Shows usage guide.                            |
| `man --version`       | Display version and license info.                                   | `man --version` | Prints version details.                       |

</details>

<details>

<summary> 📂 search (grep) command</summary>

# Linux Cheat Sheet: `grep` Command

| Command / Option                    | Description                                        | Example Usage                    | Example Output / Notes                      |
| ----------------------------------- | -------------------------------------------------- | -------------------------------- | ------------------------------------------- |
| `grep pattern file`                 | Search for a pattern in a file.                    | `grep hello file.txt`            | Prints lines containing "hello".            |
| `grep -i pattern file`              | Case-insensitive search.                           | `grep -i linux file.txt`         | Matches `Linux`, `LINUX`, `linux`, etc.     |
| `grep -n pattern file`              | Show line numbers with matches.                    | `grep -n main program.c`         | Displays matching lines with line numbers.  |
| `grep -c pattern file`              | Count the number of matching lines.                | `grep -c error log.txt`          | Prints number of lines containing "error".  |
| `grep -v pattern file`              | Invert match (show lines that do NOT match).       | `grep -v foo file.txt`           | Displays all lines except those with "foo". |
| `grep -l pattern *`                 | Show only filenames containing the match.          | `grep -l TODO *.c`               | Lists `.c` files containing "TODO".         |
| `grep -w pattern file`              | Match whole words only.                            | `grep -w test file.txt`          | Matches "test" but not "testing".           |
| `grep -r pattern dir/`              | Recursively search in all files under a directory. | `grep -r main ./src`             | Searches "main" in all files under `src/`.  |
| `grep -e pattern1 -e pattern2 file` | Search for multiple patterns.                      | `grep -e cat -e dog animals.txt` | Matches lines containing "cat" or "dog".    |
| `grep --color pattern file`         | Highlight matched text in output.                  | `grep --color error log.txt`     | Highlights "error" in results.              |

</details>

<details>

<summary> 📂 echo command</summary>

# Linux Cheat Sheet: `echo` Command

| Command / Option       | Description                                                         | Example Usage               | Example Output / Notes                       |
| ---------------------- | ------------------------------------------------------------------- | --------------------------- | -------------------------------------------- |
| `echo text`            | Print text to standard output.                                      | `echo Hello World`          | `Hello World`                                |
| `echo $VAR`            | Print the value of a variable.                                      | `echo $HOME`                | `/home/user`                                 |
| `echo "text" > file`   | Redirect output into a file (overwrite).                            | `echo "Hello" > hello.txt`  | Creates/overwrites `hello.txt` with "Hello". |
| `echo "text" >> file`  | Append output to a file.                                            | `echo "World" >> hello.txt` | Adds "World" to `hello.txt`.                 |
| `echo *`               | Print all files/directories in current directory (shell expansion). | `echo *`                    | Lists files in current directory.            |
| `echo -n text`         | Print text without trailing newline.                                | `echo -n "Hello"`           | Outputs `Hello` without moving to new line.  |
| `echo -e "text\ntext"` | Enable interpretation of backslash escapes (e.g., newline, tab).    | `echo -e "Hello\nWorld"`    | Prints `Hello` then `World` on next line.    |
| `echo $?`              | Print exit status of last command.                                  | `echo $?`                   | `0` if success, non-zero if error.           |
| `echo $$`              | Print process ID of current shell.                                  | `echo $$`                   | Displays PID of current shell.               |
| `echo $USER`           | Print current logged-in username.                                   | `echo $USER`                | `pieter` (example).                          |

</details>

<details>

<summary> 📂 network downloader (Wget) command</summary>

# Linux Cheat Sheet: `wget` Command

| Command / Option                  | Description                                                 | Example Usage                                     | Example Output / Notes                       |
| --------------------------------- | ----------------------------------------------------------- | ------------------------------------------------- | -------------------------------------------- |
| `wget URL`                        | Download a file from the web.                               | `wget https://example.com/file.zip`               | Saves `file.zip` in current directory.       |
| `wget -O filename URL`            | Download and save with a custom filename.                   | `wget -O new.zip https://example.com/file.zip`    | Saves file as `new.zip`.                     |
| `wget -c URL`                     | Resume an incomplete download.                              | `wget -c https://example.com/file.zip`            | Continues download from where it stopped.    |
| `wget -b URL`                     | Download in background mode.                                | `wget -b https://example.com/file.zip`            | Runs in background, logs to `wget-log`.      |
| `wget -i file.txt`                | Download URLs listed in a file.                             | `wget -i urls.txt`                                | Downloads all URLs from `urls.txt`.          |
| `wget --limit-rate=200k URL`      | Limit download speed.                                       | `wget --limit-rate=200k https://example.com`      | Restricts speed to 200 KB/s.                 |
| `wget --progress=dot URL`         | Show progress in dot style instead of default bar.          | `wget --progress=dot https://example.com`         | Displays progress with dots.                 |
| `wget --spider URL`               | Check if a file exists on the server (without downloading). | `wget --spider https://example.com/file.zip`      | Reports availability of file.                |
| `wget -r URL`                     | Recursively download files from a website.                  | `wget -r https://example.com/dir/`                | Downloads all files under `/dir/`.           |
| `wget --no-check-certificate URL` | Ignore SSL certificate errors.                              | `wget --no-check-certificate https://example.com` | Downloads even with invalid SSL certificate. |
| `wget --help`                     | Display help information for `wget`.                        | `wget --help`                                     | Shows usage guide.                           |
| `wget --version`                  | Display version and license info.                           | `wget --version`                                  | Prints version details.                      |

</details>

<details>

<summary> 📂 whoami command</summary>

# Linux Cheat Sheet: `whoami` Command

| Command / Option   | Description                                        | Example Usage      | Example Output / Notes  |
| ------------------ | -------------------------------------------------- | ------------------ | ----------------------- |
| `whoami`           | Prints the username of the current effective user. | `whoami`           | `pieter` (example).     |
| `whoami --help`    | Display help information for `whoami`.             | `whoami --help`    | Shows usage guide.      |
| `whoami --version` | Display version and license info.                  | `whoami --version` | Prints version details. |

</details>

<details>

<summary> 📂 sort command</summary>

# Linux Cheat Sheet: `sort` Command

| Command / Option              | Description                                            | Example Usage                     | Example Output / Notes                  |
| ----------------------------- | ------------------------------------------------------ | --------------------------------- | --------------------------------------- |
| `sort file.txt`               | Sort lines in a file alphabetically (ASCII order).     | `sort names.txt`                  | Outputs lines sorted A → Z.             |
| `sort -r file.txt`            | Sort lines in reverse (descending order).              | `sort -r names.txt`               | Outputs lines Z → A.                    |
| `sort -n file.txt`            | Sort numerically (treats numbers as values, not text). | `sort numbers.txt`                | Orders `1, 2, 10, 21` correctly.        |
| `sort -nr file.txt`           | Sort numerically in reverse order.                     | `sort -nr numbers.txt`            | Orders largest → smallest.              |
| `sort -k column file.txt`     | Sort by a specific column (useful for tables).         | `sort -k 2 data.txt`              | Sorts by second column.                 |
| `sort -u file.txt`            | Sort and remove duplicate lines (unique output).       | `sort -u items.txt`               | Outputs sorted list without duplicates. |
| `sort -c file.txt`            | Check if a file is already sorted; reports disorder.   | `sort -c names.txt`               | Prints error if not sorted.             |
| `sort -M file.txt`            | Sort by month names (Jan, Feb, etc.).                  | `sort -M months.txt`              | Orders by calendar month.               |
| `sort -o output.txt file.txt` | Save sorted output into a file.                        | `sort -o sorted.txt unsorted.txt` | Writes sorted result to `sorted.txt`.   |

</details>

<details>

<summary> 📂 calendar (cal) command</summary>

# Linux Cheat Sheet: `cal` Command

| Command / Option | Description                                                | Example Usage   | Example Output / Notes                      |
| ---------------- | ---------------------------------------------------------- | --------------- | ------------------------------------------- |
| `cal`            | Display the current month’s calendar.                      | `cal`           | Shows calendar for current month.           |
| `cal year`       | Display the calendar for an entire year.                   | `cal 2025`      | Prints all months of year 2025.             |
| `cal month year` | Display calendar for a specific month and year.            | `cal 12 2025`   | Shows December 2025 calendar.               |
| `cal -3`         | Display previous, current, and next month together.        | `cal -3`        | Shows three consecutive months.             |
| `cal -m month`   | Display calendar for a specific month of the current year. | `cal -m 7`      | Shows July of current year.                 |
| `cal -y`         | Display calendar for the current year.                     | `cal -y`        | Prints all months of current year.          |
| `cal -j`         | Display Julian calendar (day numbers starting from Jan 1). | `cal -j`        | Shows day-of-year numbers instead of dates. |
| `cal --help`     | Display help information for `cal`.                        | `cal --help`    | Shows usage guide.                          |
| `cal --version`  | Display version and license info.                          | `cal --version` | Prints version details.                     |

</details>

<details>

<summary> 📂 whereis command</summary>

# Linux Cheat Sheet: `whereis` Command

| Command / Option      | Description                                                                  | Example Usage         | Example Output / Notes                         |
| --------------------- | ---------------------------------------------------------------------------- | --------------------- | ---------------------------------------------- |
| `whereis command`     | Locate the binary, source, and manual page files for a command.              | `whereis ls`          | `ls: /bin/ls /usr/share/man/man1/ls.1.gz`      |
| `whereis -b command`  | Search only for binary files.                                                | `whereis -b ls`       | Shows only binary path for `ls`.               |
| `whereis -m command`  | Search only for manual (man) files.                                          | `whereis -m ls`       | Shows only man page location.                  |
| `whereis -s command`  | Search only for source files.                                                | `whereis -s ls`       | Shows source file location if available.       |
| `whereis -u command`  | Search for unusual entries (commands missing man page or source).            | `whereis -u ls`       | Lists binaries without associated docs/source. |
| `whereis -f filename` | Treat argument as filename, not command.                                     | `whereis -f myscript` | Searches for `myscript` file.                  |
| `whereis -l`          | Display directories where `whereis` searches for binaries, sources, and man. | `whereis -l`          | Prints search paths used by `whereis`.         |

</details>

<details>

<summary> 📂 disk free (df) command</summary>

# Linux Cheat Sheet: df Command

| Command / Option | Description                                              | Example Usage  | Example Output / Notes                             |
| ---------------- | -------------------------------------------------------- | -------------- | -------------------------------------------------- |
| `df`             | Show disk space usage of all mounted filesystems.        | `df`           | Displays blocks used, available, and mount points. |
| `df -h`          | Human-readable output (sizes in KB, MB, GB).             | `df -h`        | Easier to read disk usage like `20G`, `512M`.      |
| `df -a`          | Include pseudo, duplicate, and inaccessible filesystems. | `df -a`        | Lists all filesystems including special ones.      |
| `df -T`          | Show filesystem type along with usage.                   | `df -T`        | Displays ext4, tmpfs, etc.                         |
| `df -i`          | Show inode information instead of block usage.           | `df -i`        | Displays inode count and usage.                    |
| `df -k`          | Show sizes in kilobytes.                                 | `df -k`        | Outputs disk usage in KB units.                    |
| `df -m`          | Show sizes in megabytes.                                 | `df -m`        | Outputs disk usage in MB units.                    |
| `df --help`      | Display help information for `df`.                       | `df --help`    | Shows usage guide.                                 |
| `df --version`   | Display version and license info.                        | `df --version` | Prints version details.                            |

</details>

<details>

<summary> 📂 count (wc) command</summary>

# Linux Cheat Sheet: `wc` Command

| Command / Option | Description                                   | Example Usage            | Example Output / Notes                                |
| ---------------- | --------------------------------------------- | ------------------------ | ----------------------------------------------------- |
| `wc file.txt`    | Print line, word, and byte counts for a file. | `wc file.txt`            | `10 50 300 file.txt` → 10 lines, 50 words, 300 bytes. |
| `wc -l file.txt` | Print only the line count.                    | `wc -l file.txt`         | `10 file.txt` → 10 lines.                             |
| `wc -w file.txt` | Print only the word count.                    | `wc -w file.txt`         | `50 file.txt` → 50 words.                             |
| `wc -c file.txt` | Print only the byte count.                    | `wc -c file.txt`         | `300 file.txt` → 300 bytes.                           |
| `wc -m file.txt` | Print only the character count.               | `wc -m file.txt`         | `300 file.txt` → 300 characters.                      |
| `wc -L file.txt` | Print length of the longest line.             | `wc -L file.txt`         | `25 file.txt` → longest line has 25 characters.       |
| `wc file1 file2` | Print counts for multiple files and a total.  | `wc file1.txt file2.txt` | Shows counts for each file plus grand total.          |

</details>

</details>

<details>

<summary><span style="font-size:1.5em; font-weight:bold;">📝Complete Linux commands </summary>

#### 🔗 [Complete Linux Commands](https://www.geeksforgeeks.org/linux-unix/linux-commands/)

</details>
