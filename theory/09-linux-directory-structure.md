# 📂 Linux Directory Structure

In Linux, **everything is treated as a file** — whether it’s a normal file, directory, or device.  
All files and directories are stored under the **root `/` directory**, following the **Filesystem Hierarchy Standard (FHS)**.

---

## 📌 Types of Files

- **General Files**: Ordinary files (text, images, videos, binaries).
- **Directory Files**: Containers for other files (including subdirectories).
- **Device Files**: Represent hardware devices (e.g., `/dev/sda1`, `/dev/null`).

---

## 🏗️ Top-Level Directories under `/`

| Directory | Description                            |
| --------- | -------------------------------------- |
| `/bin`    | Essential user binaries (executables). |
| `/etc`    | System configuration files.            |
| `/home`   | User home directories.                 |
| `/opt`    | Optional/third-party software.         |
| `/tmp`    | Temporary files (cleared on reboot).   |
| `/usr`    | User-related programs and data.        |
| `/var`    | Variable data (logs, spool files).     |

---

## 🔧 Other Important Directories

| Directory     | Description                                  |
| ------------- | -------------------------------------------- |
| `/boot`       | Bootloader and kernel files.                 |
| `/dev`        | Device files (disks, terminals, USB).        |
| `/lib`        | Kernel modules and shared libraries.         |
| `/lost+found` | Recovered corrupted file fragments.          |
| `/media`      | Mount points for removable devices.          |
| `/mnt`        | Temporary mount points.                      |
| `/proc`       | Virtual filesystem with process/system info. |
| `/run`        | Volatile runtime data.                       |
| `/sbin`       | System binaries for administration.          |
| `/srv`        | Service-related data (web, FTP).             |
| `/sys`        | Virtual filesystem for devices and drivers.  |

---

## ⚙️ Key Configuration Files in `/etc`

- `/etc/bashrc` → Bash shell defaults and aliases.
- `/etc/crontab` → Scheduled tasks.
- `/etc/fstab` → Disk drives and mount points.
- `/etc/passwd` → User account info.
- `/etc/group` → Security group definitions.
- `/etc/hosts` → Hostname-to-IP mappings.
- `/etc/grub.conf` → GRUB bootloader config.
- `/etc/resolv.conf` → DNS configuration.
- `/etc/init.d/` → Service startup scripts.
- `/etc/profile` → System-wide shell defaults.

---

## 👤 User-Related Files in `/usr`

- `/usr/bin` → Most user executables.
- `/usr/sbin` → Admin commands.
- `/usr/lib` → Libraries and object files.
- `/usr/include` → Header files for C programs.
- `/usr/share` → Architecture-independent shared files.

---

## 📊 Process Info in `/proc`

- `/proc/cpuinfo` → CPU details.
- `/proc/meminfo` → Memory usage.
- `/proc/modules` → Loaded kernel modules.
- `/proc/mounts` → Mounted filesystems.
- `/proc/stat` → System statistics.
- `/proc/swaps` → Swap file info.

---

## 📝 Log Files in `/var/log`

- `/var/log/messages` → Global system messages.
- `/var/log/wtmp` → Login/logout history.
- `/var/log/lastlog` → Last login info.

---

## ✅ Key Takeaways

- **Root `/`** is the starting point of all directories.
- **/bin, /sbin, /lib** contain essential binaries and libraries.
- **/etc** holds critical configuration files.
- **/usr** is the largest hierarchy for user-space programs.
- **/proc** and **/sys** provide dynamic system and process information.
- **/var/log** is crucial for monitoring and troubleshooting.

---

📖 Source: [GeeksforGeeks - Linux Directory Structure](https://www.geeksforgeeks.org/linux-unix/linux-directory-structure/)
