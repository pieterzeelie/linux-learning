# Linux File Hierarchy: Practical Labs

This guide provides hands-on exercises to understand the Linux/Unix file hierarchy structure.  
Each section includes commands, expected outputs, and challenge tasks.

---

## 1. System Navigation & Permissions

- Explore the root directory:
  Run:
  ```bash
  ls /
  ```
  Output:
  ```bash
  in dev init lib64 mnt root sbin.usr-is-merged sys var
  bin.usr-is-merged etc lib lost+found opt run snap tmp
  boot home lib.usr-is-merged media proc sbin srv usr
  ```

## 2. Essential Binaries

- List binaries in `/bin`:
  Run:
  ```bash
  ls /bin | head -10
  ```
  Output:
  ```bash
  NF
  X11
  aa-enabled
  aa-exec
  aa-features-abi
  add-apt-repository
  addpart
  addr2line
  apport-bug
  ```

## 3. Boot and Kernel awareness

-Inspect kernel versions
Run:

```bash
ls /boot/vmlinuz*
```

## 4. Device Management

-Explore block devices

Run:

```bash
ls /dev/sd*
```

-Mount a USB driver
Run:

```bash
sudo mount /dev/sdb1 /mnt
ls /mnt
```

## 5. Configuration Files

-Inspect user and group definitions
Run:

```bash
cat /etc/passwd
cat /etc/group
```

-modify /etc/hosts
Run:

```bash
sudo nano /etc/hosts
ping custom.local
```

## 6. Temporary files

- Create a file in /tmp
  Run:

```bash
echo "Temporary Data" > /tmp/test.txt
```

## 7. Libraries and Dependencies

-Explore shared files

Run:

```bash
ls /lib /usr/lib
```

-check binary dependencies
Run:

```bash
ldd /bin/ls
```

## 8. Process Monitoring

-Inspect System info
Run:

```bash
cat /proc/cpuinfo
cat /proc/meminfo
```

-Explore a running process
Run:

```bash
ps aux | grep bash
ls /proc/<PID>
```
