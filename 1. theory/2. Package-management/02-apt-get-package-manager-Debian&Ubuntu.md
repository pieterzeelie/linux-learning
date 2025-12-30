# Debian & Ubuntu Package Management `apt-get`

## 📌 Overview
`apt-get` is a command‑line tool used on Debian-based Linux distributions (Ubuntu, Debian, Linux Mint, Kali) to install, update, upgrade, and remove packages.
It retrieves packages from authenticated repositories and handles dependencies automatically.

## 🧱 Basic Syntax
```bash
sudo apt-get [options] [command] [package(s)]
```

### Components
- sudo — required for administrative package operations
- apt-get — the package manager
- options — modify behavior (-y, -s, etc.)
- packages — one or more package names

## 🚀 Common Commands
|Command  |Purpose  |Example  | 
|---------|---------|---------|
| update |Refresh package lists  | sudo apt-get update | 
| upgrade |Upgrade installed packages  | sudo apt-get upgrade | 
| dist-upgrade |Upgrade + handle dependency changes (may remove packages)  | sudo apt-get dist-upgrade | 
| install |Install or upgrade a package  | sudo apt-get install vim | 
| --reinstall |Reinstall a package  | sudo apt-get install --reinstall firefox | 
| remove |Remove package (keep config files)  | sudo apt-get remove vim | 
| purge |Remove package + config files| sudo apt-get purge vim | 
| autoremove |Remove unused dependency packages  | sudo apt-get autoremove | 
| clean |Clear cached .deb files| sudo apt-get clean | 
| download |Download package without installing  | sudo apt-get download firefox | 
| source |Download source code  | sudo apt-get source firefox | 
| show |Display package metadata  | sudo apt-get show firefox | 
| list |List installed/available packages  | sudo apt-get list | 



## ⚙️ Useful Options
|Option  |Description  | 
|--------|-------------|
| --no-install-recommends |Install only required dependencies  | 
| --install-suggests |Install suggested packages too  | 
| -d--download-only |Download but do not install  | 
| -f--fix-broken |Fix broken dependencies  | 
| -m--ignore-missing |Ignore missing packages  | 
| --no-download |Use only cached packages  | 
| -q--quiet |Reduce output (useful in scripts)  | 
| -s--simulate |Dry-run (no changes made)  | 
| -y--yes |Auto-confirm prompts| 
| --assume-no |Auto-decline prompts  | 
| --no-show-upgraded |Hide upgrade list output  | 
| -V |Show package versions during update  | 
| --show-progress |Show progress bar  | 
| --no-upgrade |Install without upgrading  | 
| --only-upgrade |Upgrade only, don’t install new packages  | 



## 🏗️ Debian vs Red Hat Note
- `apt-get` works only on Debian-based systems.
- Red Hat–based distros (RHEL, CentOS, Fedora) use yum or dnf instead.
