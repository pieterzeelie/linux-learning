# Setting Up Dual Boot: Linux + Windows

## 🔑 Summary
Dual booting allows you to run **Linux and Windows on the same machine**.  
- You shrink your Windows partition to create space.  
- Install Linux alongside Windows using a bootable USB.  
- After installation, the **GRUB bootloader** lets you choose which OS to run at startup.  

This setup gives you native Linux performance while keeping Windows available for everyday tasks.

---

## ⚙️ Steps to Install Dual Boot

1. **Prepare Disk Space**  
   - Use Windows Disk Management to shrink your Windows partition.  
   - Allocate ~100–150 GB for Linux.  

2. **Create Bootable USB**  
   - Download Ubuntu ISO.  
   - Use Rufus (Windows) to create a bootable USB drive.  

3. **Adjust BIOS/UEFI Settings**  
   - Disable Secure Boot.  
   - Turn off Fast Startup.  
   - Disable BitLocker if enabled.  

4. **Boot from USB & Install Linux**  
   - Restart and boot from the USB drive.  
   - Select *“Something Else”* during installation.  
   - Create partitions:  
     - **Swap** (equal to RAM size).  
     - **Root** (`ext4`, ~100 GB).  
   - Install Ubuntu alongside Windows.  

5. **Dual Boot Menu**  
   - On restart, the **GRUB bootloader** will let you choose between Linux and Windows.  

---

## 🌟 Benefits of Dual Boot

1. **Native Linux Performance:** Faster than running Linux in a VM.  
2. **Flexibility:** Switch between Windows (proprietary apps) and Linux (development/DevOps).  
3. **Learning:** Practice Linux commands in a real environment.  
4. **Compatibility:** Access both ecosystems without separate hardware.  
5. **Resource Efficiency:** No need to split RAM/CPU like in a VM.  
6. **Direct Hardware Access:** Better support for drivers and GPU acceleration.  
7. **Cost-Effective:** One machine serves both OS needs.  
8. **Professional Practice:** Mirrors real-world setups where engineers use dual boot for testing.  

---
