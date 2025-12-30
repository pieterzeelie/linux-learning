# 🐧 Linux Package Managers & systemctl
## 📦 What Are Package Managers?
Tools that automate installing, updating, removing, and querying software packages on Linux.
They handle:
- Installation (with automatic dependency resolution)
- Upgrades
- Removal
- Querying package info
- Repository management

## 🔧 Major Linux Package Managers
APT (Debian/Ubuntu)
- High‑level package manager for .deb systems
- Strong dependency resolution
- Uses online repositories
- Maintains local package cache

### Common Commands
```bash
sudo apt-get install <pkg>
sudo apt-get update
sudo apt-get upgrade
sudo apt-get remove <pkg>
apt-cache search <pkg>
```


## YUM (CentOS/RHEL) — Legacy
- Handles dependencies
- Works with repo metadata
- Being replaced by dnf
### Commands
```bash
sudo yum install <pkg>
sudo yum makecache
sudo yum update
sudo yum remove <pkg>
```


## DNF (Fedora/RHEL modern)
- Successor to YUM
- Faster, better dependency handling
### Commands
```bash
sudo dnf install <pkg>
sudo dnf upgrade
```

## Pacman (Arch/Manjaro)
- Simple, transparent package operations
- Supports rolling‑release model
- Works with AUR via helpers like yay
### Commands
```bash
sudo pacman -S <pkg>
sudo pacman -Syu
sudo pacman -R <pkg>
pacman -Q <pkg>
```

## Zypper (openSUSE)
- Strong dependency resolution
- Safe transactions (rollback on failure)
- Works with many official/community repos
### Commands
```bash
sudo zypper in <pkg>
sudo zypper up
sudo zypper rm <pkg>
zypper se <pkg>
```


## DPKG (Low‑level Debian tool)
- Installs .deb files directly
- Does NOT resolve dependencies
- Often used with APT
### Commands
```bash
sudo dpkg -i <file.deb>
sudo dpkg -r <pkg>
dpkg -l | grep <pkg>
```

## ⚙️ systemd & systemctl
### What is systemd?
A modern init system that:
- Starts services in parallel
- Manages dependencies
- Integrates with cgroups
- Provides logging via journalctl
- Supports socket activation

### systemctl — Main Commands
Start/Stop Services:
```bash
sudo systemctl start <service>
sudo systemctl stop <service>
```

Enable/Disable at Boot:
```bash
sudo systemctl enable <service>
sudo systemctl disable <service>
```

Restart/Reload:
```bash
sudo systemctl restart <service>
sudo systemctl reload <service>
```

Check Status:
```bash
systemctl status <service>
```

List Active Units:
```bash
systemctl list-units --type=service
```

## ✅ Key Takeaways
- Package managers differ by distro but share core functions.
- APT/YUM/DNF/Pacman/Zypper each serve different ecosystems.
- DPKG is low‑level and doesn’t handle dependencies.
- systemd is the dominant init system, and systemctl is its control interface.
- Mastering package managers + systemctl is essential for Linux administration.
