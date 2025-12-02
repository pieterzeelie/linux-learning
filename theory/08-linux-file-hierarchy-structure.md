# 🗂️ Linux File Hierarchy Structure (FHS)

The **Filesystem Hierarchy Standard (FHS)** defines the directory structure and contents in Unix-like systems.  
All files and directories appear under the root `/`, even if stored on different devices.

---

## 📌 Core Directories

### `/` (Root)

- Base of the Linux filesystem.
- Only the root user can write here.
- `/root` is the root user’s home directory (different from `/`).

### `/bin`

- Essential user binaries (e.g., `ls`, `cp`, `grep`, `ping`).
- Available to all users, required in single-user mode.

### `/boot`

- Bootloader and kernel files.
- Examples: `vmlinuz`, `initrd.img`, GRUB configs.

### `/dev`

- Device files (interfaces to hardware/software).
- Block devices (disks) and character devices (terminals, USB).
- Examples: `/dev/sda1`, `/dev/tty1`.

### `/etc`

- System-wide configuration files.
- Startup/shutdown scripts, user info, network configs.
- Examples: `/etc/resolv.conf`, `/etc/logrotate.conf`.

### `/home`

- Personal directories for non-root users.
- Example: `/home/anshu`.

### `/lib`

- Shared libraries required by binaries in `/bin` and `/sbin`.
- Examples: `libncurses.so`, `ld-2.11.1.so`.

### `/media`

- Temporary mount points for removable devices (USB, CD-ROM).
- Examples: `/media/cdrom`, `/media/floppy`.

### `/mnt`

- Temporary mount directory for filesystems (used by sysadmins).

### `/opt`

- Optional third-party software packages.
- Example: `/opt/vendor_app`.

### `/sbin`

- System binaries for administration (root privileges).
- Examples: `iptables`, `fdisk`, `reboot`.

### `/srv`

- Site-specific data for services (web, FTP, CVS).
- Example: `/srv/cvs`.

### `/tmp`

- Temporary files created by programs/users.
- Cleared on reboot.

### `/usr`

- Secondary hierarchy for user applications and data.
- Subdirectories:
  - `/usr/bin`: User binaries (e.g., `awk`, `scp`).
  - `/usr/sbin`: Admin binaries (e.g., `cron`, `sshd`).
  - `/usr/lib`: Libraries for `/usr/bin` and `/usr/sbin`.
  - `/usr/local`: Locally installed programs (e.g., Apache).
  - `/usr/src`: Kernel sources and documentation.

### `/proc`

- Virtual filesystem with process/system info.
- Examples: `/proc/meminfo`, `/proc/uptime`, `/proc/{pid}`.

---

## ✅ Key Takeaways

- **Root `/`** is the starting point of all directories.
- **/bin, /sbin, /lib** contain essential binaries and libraries.
- **/etc** holds critical configuration files.
- **/home** provides personal space for users.
- **/usr** is the largest hierarchy for applications and utilities.
- **/proc** is a pseudo-filesystem for system and process information.

---

📖 Source: [GeeksforGeeks - Linux File Hierarchy Structure](https://www.geeksforgeeks.org/linux-unix/linux-file-hierarchy-structure/)
