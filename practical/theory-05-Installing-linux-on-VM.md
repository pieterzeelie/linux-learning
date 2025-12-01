## 🚀 Setting Up Linux in a Virtual Machine

To practice Linux commands safely, install Ubuntu in a Virtual Machine:

1. Download [VirtualBox](https://www.virtualbox.org/).
2. Create a new VM → Select "Linux" → Choose "Ubuntu (64-bit)".
3. Attach the Ubuntu ISO image.
4. Allocate resources:
   - RAM: 50% of your system memory (e.g., 8GB if you have 16GB).
   - Disk: At least 20GB.
5. Start the VM and follow the Ubuntu installation wizard.
6. Install Guest Additions for full-screen and clipboard support:
   ```bash
   sudo apt update
   sudo apt install -y build-essential linux-headers-$(uname -r)
