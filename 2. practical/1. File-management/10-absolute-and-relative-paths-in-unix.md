# Practical Lab: Absolute vs Relative Paths

This lab demonstrates how to use absolute and relative pathnames in Linux.

---

## 1. Navigate to `/etc` using Absolute and Relative Paths

### Absolute Path

Run:

```bash
cd /etc
pwd
```

Output:

```bash
/etc
```

### Relative path

Run:

```bash
cd ~
cd ../etc
pwd
```

Output:

```bash
/etc
```

## 2. use `cd` Repeatedly to move up directories

Run:

```bash
pwd
/home/user/projects/linuxlabs
cd ..
pwd
/home/user/projects
cd ..
pwd
/home/user
```
