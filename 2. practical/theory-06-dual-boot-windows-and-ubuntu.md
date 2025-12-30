## ⚙️ Steps to Install Ubuntu

### 1. Prepare Your Laptop
- Backup important data.
- Ensure at least 25 GB free storage.
- Have a USB stick (≥ 8 GB).
- If dual booting with Windows, shrink your Windows partition using Disk Management.

### 2. Download Ubuntu ISO
- Visit [Ubuntu Downloads](https://ubuntu.com/download).
- Choose the latest **LTS version** (e.g., Ubuntu 24.04 LTS).
- Save the `.iso` file.
- (Optional) Verify checksum to ensure file integrity.

### 3. Create Bootable USB
- Insert your USB stick.
- Use a tool like **Rufus (Windows)**, **Etcher (Windows/macOS/Linux)**, or **Startup Disk Creator (Linux)**.
- Select the Ubuntu ISO and your USB drive.
- Start the process (this erases the USB).

### 4. Boot from USB
- Restart your laptop.
- Enter the boot menu (keys vary: F12, Esc, F2, Del).
- Select the USB drive as the boot device.
- Ubuntu installer will load.

### 5. Installation Setup
- Choose language and keyboard layout.
- Connect to Wi-Fi if needed.
- Select installation type:
  - **Erase disk and install Ubuntu** (clean install).
  - **Install alongside Windows** (dual boot).
  - **Something else** (manual partitioning).

### 6. Partitioning (if dual booting)
- Create:
  - **Root partition** (`ext4`, ~100 GB).
  - **Swap partition** (equal to RAM size).
  - Optional: **Home partition** for user files.

### 7. User Setup
- Enter your name, username, and password.
- Choose your time zone.

### 8. Complete Installation
- Click **Install Now**.
- Wait for files to copy and installation to finish.
- Restart your laptop.
- Remove the USB when prompted.

### 9. First Boot
- If dual booting, you’ll see the **GRUB menu** to choose Ubuntu or Windows.
- Log in with your username and password.
- Run updates:
```bash
sudo apt update && sudo apt upgrade -y

