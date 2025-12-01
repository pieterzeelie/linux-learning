# 🛠️ Practical Example: Using XFS File System in Linux

## 1. Install XFS Utilities

Run:

```bash
sudo apt-get install xfsprogs
```

## 2. Create a partition

Run:

```bash
sudo fdisk /dev/sda
```

- Create a new partition (n)
- Write changes (w)

## 3. Format the partition with XFS

run:

```bash
sudo mkfs.xfs /dev/sda1 -f
```

## 4. Mount the partition

Run:

```bash
sudo mount /dev/sda1 /mnt/xfs_partition
```

## 5. Verify the mount

Run:

```bash
df -h
```

## 6. Create a file to test

Run:

```bash
sudo touch /mnt/xfs_partition/test_file.txt
```
