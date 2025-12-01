# Linux File System - Summary

## 📚 What is a Linux File System?

- A set of processes that control how, where, and when data is stored/retrieved.
- Everything in Linux is treated as a file (including devices and applications).
- Uses **mount points** under the root `/` directory instead of drive letters (C:, D:).

---

## 🏗️ File System Structure

1. **Logical File System**
   - Interface between user applications and the file system.
   - Handles operations like open, read, close.

2. **Virtual File System (VFS)**
   - Provides a standardized interface for multiple file systems.
   - Ensures compatibility and cohesion.

3. **Physical File System**
   - Manages physical memory blocks on disk.
   - Handles low-level storage and retrieval.

---

## ⚙️ Characteristics of a File System

- **Space Management**: Allocation of memory blocks, fragmentation.
- **Filename Rules**: Length, special characters, case sensitivity.
- **Directory Structure**: Linear or hierarchical with index tables.
- **Metadata**: Stores file attributes (size, permissions, timestamps).
- **Utilities**: Operations like copy, move, backup, recovery.
- **Design Limits**: Maximum data capacity and constraints.

---

## 🔑 Key Concepts

- **Journaling**: Logs changes before committing to disk.
  - Modes: Journal (safe, slow), Ordered (balanced), Writeback (fast, risky).
- **Versioning**: Stores previous versions of files.
- **Inode**: Data structure representing file attributes and location.

---

## 🗂️ Types of Linux File Systems

- **ext (1992)**: First Linux-specific FS.
- **ext2 (1993)**: Non-journaling, efficient for flash/SSD.
- **Xiafs (1993)**: Limited, obsolete.
- **ext3 (1999)**: Introduced journaling, online growth.
- **JFS (IBM, 1990)**: Good performance, less common now.
- **ReiserFS (2001)**: B+ Tree indexing, tail packing.
- **XFS (2001)**: 64-bit journaling, optimized for large files, parallel I/O.
- **SquashFS (2002)**: Read-only, used in embedded systems.
- **Reiser4 (2004)**: Incremental ReiserFS, limited adoption.
- **ext4 (2006)**: Default FS in many distros, backward compatible, large file support.
- **btrfs (2007)**: Snapshots, pooling, self-healing, default in Fedora.
- **bcachefs (2015)**: Copy-on-write, encryption, compression.
- **Others**: NTFS, exFAT (for interoperability).

---

## 📊 Comparison Highlights

- **Best performers**: ext4, XFS, btrfs.
- **ext4**: Default choice due to stability, backward compatibility, and balanced performance.
- **XFS**: Excels with large files and concurrency.
- **btrfs**: Feature-rich but sometimes buggy.

---
