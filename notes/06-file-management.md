# Lesson 5 - Linux Directories Explained

## Summary

This lesson introduced the Linux file system hierarchy and explained the purpose of the most important directories found under the root (`/`) directory.

---

## Key Concepts

- Everything in Linux starts at the **root directory (`/`)**.
- The Linux file system is organized as a tree of directories.
- Each directory has a specific purpose.
- Understanding the file system hierarchy makes it easier to find files and troubleshoot systems.

---

## Commands Learned

```bash
ls /
pwd
cd
ls /usr/bin
ls /usr/lib64
ls /usr/share
ls /var/log
```

---

## Notes

### Root Directory (`/`)

- Everything in Linux starts at the root directory (`/`).
- It is the top level of the Linux file system.

### `/home`

- Stores users' personal files and directories.

### `cd`

- Changes the current directory.

### `pwd`

- Prints the current working directory.

### `/etc`

- Stores system configuration files.
- It is good practice to back up configuration files before making changes.

### `/var`

- Stores variable data that changes frequently.
- Examples include logs, mail, and cache files.
- System logs are commonly found in `/var/log`.

### `/usr`

- Contains user programs and installed software.

Important subdirectories:

- `/usr/bin` – Executable programs (binaries).
- `/usr/lib64` – Shared libraries used by applications.
- `/usr/share` – Shared resources such as documentation and data files.

### `/tmp`

- Used for temporary files.
- Linux regularly cleans this directory.
- Do not store important files here.
- All users can access this directory.

### `/root`

- Home directory of the **root** (superuser) account.
- Normal users cannot access this directory.

### `/boot`

- Contains files required to start the operating system, including the Linux kernel.
- Usually only modified when troubleshooting boot-related problems.

### `/mnt`

- Used for temporarily mounting storage devices such as USB drives or network shares.

### `/run`

- Stores information about the current running system.
- Created each time the system boots.
- Cleared whenever the system restarts.

---

## What I Learned

I learned that Linux organizes files into a standard directory structure where each folder has a specific purpose. Understanding the Linux file system hierarchy will help me navigate the operating system and know where to find configuration files, logs, software, and user data.
