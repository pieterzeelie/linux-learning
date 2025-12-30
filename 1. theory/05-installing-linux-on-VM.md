# Installing Linux Using a Virtual Machine

## 🔑 Summary
A Virtual Machine (VM) allows you to run Linux inside your existing operating system (Windows/macOS) without changing your main setup.  
- **Tools:** VirtualBox (free), VMware Workstation Player, Hyper-V.  
- **Process:** Download a Linux ISO (e.g., Ubuntu), create a VM, allocate CPU/RAM/disk, and install.
-  
## Benefits: 
- Safe Sandbox: Mistakes won’t affect your host OS — perfect for beginners experimenting with commands.
- Snapshots & Rollback: Save the VM state before testing. Roll back instantly if something breaks.
- Portability: Copy or move your VM to another computer easily.
- Resource Control: Allocate CPU, RAM, and disk space as needed.
- Multiple Environments: Run different Linux distros side by side (Ubuntu, CentOS, Fedora).
- Isolation: Each VM is separate, so experiments don’t interfere with other projects or your host system.
- Cost-Effective: Free tools like VirtualBox let you practice without buying extra hardware.
- Real-World Practice: Mirrors how DevOps teams use virtualization and containers in production.

---

## ⚙️ Steps to Install Linux in a VM

1. **Download VirtualBox** (or VMware/Hyper-V).  
2. **Create a new VM** → Select *Linux* → Choose *Ubuntu (64-bit)*.  
3. **Attach the ISO image** (Ubuntu ISO).  
4. **Allocate resources:**  
   - RAM: ~50% of system memory (e.g., 8GB if you have 16GB).  
   - Disk: At least 20GB.  
5. **Run the VM** and follow the Ubuntu installation wizard.  
6. **Install Guest Additions** for better integration (clipboard, full-screen, shared folders).  

Run:
```bash
sudo apt update
sudo apt install -y build-essential linux-headers-$(uname -r)
