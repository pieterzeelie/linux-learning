# 🧪 Practical Labs: `apt-get` (Debian/Ubuntu)  

## Lab 1 — Update & Upgrade System Packages
🎯 Objective
Learn how to refresh package lists and upgrade installed packages safely.
🧩 Steps
### 1. Refresh package lists
`sudo apt-get update`

### 2. Upgrade installed packages
`sudo apt-get upgrade -y`

### 3. Full upgrade (handles dependencies)
`sudo apt-get dist-upgrade -y`

### 🔍 Verification
`apt-get -s upgrade`

Output:  
`“No packages will be upgraded.”`

🛠️ Troubleshooting
- If you see “Could not get lock /var/lib/dpkg/lock”
→ Another package manager is running. Close it or reboot.

## Lab 2 — Install, Reinstall, and Remove Packages

### 1. Install a package
`sudo apt-get install -y tree`

### 2. Verify installation
`tree --version`

### 3. Reinstall the package
`sudo apt-get install --reinstall -y tree`

### 4. Remove package (keep config)
`sudo apt-get remove -y tree`

### 5. Purge package (remove config)
`sudo apt-get purge -y tree`

### 🔍 Verification
`dpkg -l | grep tree`

Output:  
`No output after purge.`

## Lab 3 — Explore Package Information

### 1. Search for a package
`apt-cache search nginx`

### 2. Show detailed info
`apt-get show nginx`

### 3. Show dependencies
`apt-cache depends nginx`

### 4. Show reverse dependencies
`apt-cache rdepends nginx`

### 🔍 Verification
Disply fields like:  
`Version, Depends, Description, Maintainer.`

## Lab 4 — Fix Broken Packages

### 1. Force install a broken package (simulation)
`sudo apt-get install -f`

### 2. Try installing a package with missing deps
`sudo dpkg -i /tmp/some-broken-package.deb  `

output:  
`Fail`

### 3. Fix it
`sudo apt-get -f install`

### 🔍 Verification
`sudo apt-get check`

Output:  
`“No broken packages.”`

## Lab 5 — Clean Cache & Manage Disk Space

### 1. Check cache size
`du -sh /var/cache/apt/archives`

### 2. Clean all cached packages
`sudo apt-get clean`

### 3. Remove unused dependencies
`sudo apt-get autoremove -y`

### 🔍 Verification
`du -sh /var/cache/apt/archives`

Expected Output:  
`Very small size (a few KB).`

## Lab 6 — Download Packages Without Installing

### 1. Create a download directory
`mkdir ~/deb-downloads && cd ~/deb-downloads`

### 2. Download package only
`sudo apt-get download htop`

### 3. Verify file exists
`ls -lh`

### 🔍 Verification
Output:
`htop_3.0.5-1_amd64.deb`

## Lab 7 — Work With Source Packages

### 1. Enable source repos (if disabled)
```Bash
sudo sed -i 's/^# deb-src/deb-src/' /etc/apt/sources.list
sudo apt-get update
```

### 2. Download source
`apt-get source curl`

### 3. Inspect files
`ls -R curl*/`

### 🔍 Verification
Displaying .c and .h files.

## Lab 8 — Simulate Installations (Dry Run)

### 1. Simulate installing nginx
`sudo apt-get install -s nginx`

### 2. Simulate removing a package
`sudo apt-get remove -s nginx`

### 🔍 Verification
Output:
`“No packages will be installed/removed.”`

## Lab 9 — Create a Broken State and Recover It

### 1. Install a package
`sudo apt-get install -y nginx`

### 2. Manually remove a dependency
`sudo dpkg --remove --force-depends nginx-common`

### 3. Run nginx
`nginx -t`

Output:  
`Fail`

### 4. Fix system
`sudo apt-get -f install`


### 🔍 Verification
`nginx -t`

Output:
`Configuration OK.`

## Lab 10 — Compare apt vs apt-get
```Bash
sudo apt-get update
sudo apt update
```
```Bash
sudo apt-get install -y cowsay
sudo apt install -y cowsay
```

### 🔍 Verification
Observe differences in:
- progress bars
- formatting
- suggestions
