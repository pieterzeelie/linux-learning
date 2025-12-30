# Linux Directory Structure: Practical Labs

This guide provides hands-on exercises to understand the Linux/Unix directory structure.  
Each section includes commands, expected outputs, and challenge tasks.

---

## 1. `/etc` – System Configuration

- Edit hostname mappings:

  Run:

  ```bash
  sudo nano /etc/hosts
  ping custom.local
  ```

- Explore scheduled tasks

  Run:

  ```bash
  cat /etc/crontab
  ```

- Inspect disk mount points

  Run:

  ```bash
  cat /etc/fstab
  ```

## 2. `/home` - User Environment

- Create a new user and switch to their home directory:

  Run:

  ```bash
  sudo adduser testuser
  ls /home/testuser
  ```

- customize shell environment

  Run:

  ```bash
  nano ~/.bashrc
  alias ll='ls -la'
  ```

## 3. /var/log - Monitoring & Troubleshooting

- Inspect system logs:
