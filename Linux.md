# Linux Basics Guide

## 1) What is Linux
Linux is a kernel-based operating system.

**Kernel:**  
Kernel is an intermediate layer between hardware and software.

---

## 2) Types of Users
- **Local User** (ubuntu)  
- **Root User** (root)

---

## 3) Architecture of Linux
- Application  
- Shell  
- Kernel  
- Hardware  

---

## 4) Basic Linux Commands

| Command | Description |
|--------|-------------|
| `ls` | Lists files and directories |
| `cd` | Change directory (`cd`, `cd ..`) |
| `sudo -i` | Switch to root user |
| `Ctrl + d` | Return to local user |
| `mkdir` | Create directory |
| `rmdir` | Remove empty directory |
| `touch` | Create file |
| `head` | First 10 lines (`head -20`) |
| `tail` | Last 10 lines (`tail -13`) |
| `cp` | Copy files/directories |
| `mv` | Move or rename |
| `rm` | Remove files/directories |
| `pwd` | Show current directory |
| `cat` | Display file content |
| `ll` | Long listing with permissions |
| `chmod` | Change permissions |
| `df` | Disk usage (`df -h` for readable) |
| `ping` | Test network |
| `wget` | Download files |
| `ssh` | Remote connection |
| `history` | Command history |
| `clear` | Clear terminal |
| `whoami` | Show current user |
| `vim file` | Edit file |
| `find -name file` | Find file |
| `apt-get update` | Update system |
| `apt-get upgrade` | Upgrade system |
| `apt-get install pkg` | Install package |
| `apt-get remove pkg` | Remove package |

---

# DAY-3

## 5) User & Group Management

### User Management

| Command | Description |
|--------|-------------|
| `useradd` | Create user (no skeleton file) |
| `adduser` | Create user with skeleton |
| `usermod` | Modify user |
| `usermod -l new old` | Rename user |
| `usermod -aG group user` | Add user to group |
| `userdel` | Delete user |
| `passwd user` | Set password |

### Group Management

| Command | Description |
|--------|-------------|
| `groupadd` | Create group |
| `groupmod` | Modify group |
| `groupdel` | Delete group |
| `groupmod -n new old` | Rename group |
| `gpasswd -a user group` | Add user to group |
| `gpasswd -d user group` | Remove user |

---

# DAY-4

## 6) Permission Management

### Permission Values

| Symbol | Value | Meaning |
|--------|------|--------|
| r | 4 | Read |
| w | 2 | Write |
| x | 1 | Execute |

**Format:**  
`rwxrwxrwx` → owner, group, others  

### Commands

| Command | Description |
|--------|-------------|
| `chmod u+r file` | Add read permission |
| `chmod g-r file` | Remove read permission |
| `chmod o=x file` | Only execute permission |
| `chown user file` | Change owner |
| `chown user:group file` | Change owner & group |

---

# DAY-5

## 7) Vim Editor

### Open File
```bash
vim filename
vim +n filename     # Open at line n
vim + filename      # Open at last line

```
---
📝 Vim Modes

| Mode    | How to Enter      | Purpose     |
| ------- | ----------------- | ----------- |
| Normal  | ESC               | Navigation  |
| Insert  | Normal mode + `i` | Insert text |
| Visual  | Normal mode + `v` | Select text |
| Command | Normal mode + `:` | Save, quit  |

---
✍️ NORMAL MODE (Common Commands)

| Action        | Key                                           |
| ------------- | --------------------------------------------- |
| Move cursor   | `h` (left), `l` (right), `j` (down), `k` (up) |
| Delete a line | `dd`                                          |
| Copy a line   | `yy`                                          |
| Paste         | `p`                                           |
| Undo          | `u`                                           |
| Redo          | `Ctrl + r`                                    |

---
🔍 VISUAL MODE

| Key Press | What It Does         |
| --------- | -------------------- |
| `v`       | Select by characters |
| `V`       | Select by lines      |

---

⚙️ COMMAND MODE

| Command     | Meaning             |
| ----------- | ------------------- |
| `:w`        | Save (write)        |
| `:q`        | Quit                |
| `:wq`       | Save and quit       |
| `:q!`       | Quit without saving |
| `:set nu`   | Show line numbers   |
| `:set nonu` | Hide line numbers   |
| `:help`     | Open Vim help       |

---

# 🔐 Permission Management

## 📂 Check Permissions
```bash
ll   # Check permissions of any file or folder

```

---
🔢 Permission Values

| Symbol | Value | Meaning | Description    |
| ------ | ----- | ------- | -------------- |
| r      | 4     | Read    | View content   |
| w      | 2     | Write   | Modify content |
| x      | 1     | Execute | Run as program |

---

⚙️ Change Permissions (chmod)

```bash

chmod u+r filename   # Add read permission to user  
chmod g-r filename   # Remove read permission from group  
chmod o=x filename   # Give only execute permission to others

```
---

👤 Change Ownership (chown)
 ```bash
 
chown user filename           # Change owner of file  
chown user:group filename     # Change owner and group of file

```
---

# 📂 File Management
### 📌 Types of Files in Linux

| File Type        | Symbol | Description                     |
| ---------------- | ------ | ------------------------------- |
| Regular file     | `-`    | Normal files (text, images, etc.) |
| Directory        | `d`    | Folder / directory              |
| Character device | `c`    | Character device files          |
| Block device     | `b`    | Block device files              |
| Pipe (FIFO)      | `p`    | Inter-process communication     |
| Socket           | `s`    | Network communication           |
| Symbolic link    | `l`    | Shortcut / link to another file |

---

### 📁 Important System Files

- `/etc/passwd`  → Stores user account information  
- `/etc/group`   → Stores group information  
- `/etc/shadow`  → Stores encrypted user passwords  
- `/etc/gshadow` → Stores secure group information
- `/etc/skel`     → Skeleton directory (default files for new users)  
- `/var/log`      → Stores system log files and logs information

---



# 🐧 Linux Basics – Interview Preparation Guide

This document contains **Scenario-Based**, **Interview-Based**, and **Conceptual Questions** based on Linux fundamentals.

---

# 📌 1. Scenario-Based Questions (Real-World)

### 🔹 Scenario 1: Permission Issue  
A user cannot edit a file even though they are part of the group.  
- What will you check?  
- How will you fix it?  

---

### 🔹 Scenario 2: Disk Full  
Your system shows 100% disk usage.  
- Which commands will you use to investigate?  
- How will you fix it?  

---

### 🔹 Scenario 3: User Creation Issue  
You created a user using `useradd`, but the home directory is missing.  
- Why did this happen?  
- How will you fix it?  

---

### 🔹 Scenario 4: File Deletion  
You accidentally deleted a file using `rm`.  
- Can you recover it?  
- If yes, how? If no, why?  

---

### 🔹 Scenario 5: SSH Connection Failure  
You are unable to connect to a remote server using `ssh`.  
- What troubleshooting steps will you follow?  

---

### 🔹 Scenario 6: Group Permission  
A file should be accessible to a group but not others.  
- How will you configure permissions?  

---

### 🔹 Scenario 7: High CPU Usage  
System is slow and CPU usage is high.  
- How will you identify the issue?  

---

# 💼 2. Interview-Based Questions

## 🔹 Basic Questions
- What is Linux?  
- What is a kernel?  
- Difference between Linux and Unix?  
- What happens when you run a command?  

---

## 🔹 Commands
- Difference between `cp`, `mv`, and `rm`  
- Difference between `head` and `tail`  
- What does `chmod 777` mean? Is it safe?  
- Difference between `apt-get update` and `apt-get upgrade`  

---

## 🔹 User Management
- Difference between `useradd` and `adduser`  
- How do you add a user to a group?  
- What happens when you delete a user?  

---

## 🔹 Permissions
- Explain `rwxr-xr--`  
- How do you change file ownership?  
- Difference between symbolic and numeric permissions  

---

## 🔹 File System
- What are different file types in Linux?  
- What is a symbolic link?  
- Difference between hard link and soft link  

---

## 🔹 Networking
- What does `ping` do?  
- What is SSH?  

---

# 📘 3. Conceptual Questions

## 🔹 Linux Basics
- Why is Linux called a kernel-based OS?  
- What is the role of the shell?  
- Explain Linux architecture  

---

## 🔹 Permissions Concept
- What do values 4, 2, and 1 represent?  
- What does permission `755` mean?  
- Why is execute permission required for directories?  

---

## 🔹 System Files
- What is `/etc/passwd`?  
- Difference between `/etc/passwd` and `/etc/shadow`  
- Why is `/etc/shadow` more secure?  

---

## 🔹 Commands & Processes
- Difference between `find` and `locate`  
- What does `history` store?  
- How does `sudo` work?  

---

## 🔹 Vim Editor
- Explain Vim modes  
- Difference between `:wq` and `:q!`  
- How to undo and redo changes?  

---

# 🎯 Bonus Tricky Questions

- Why is Linux more secure than Windows?  
- What happens if you run `rm -rf /`?  
- Can a file exist without a name in Linux?  
- Why does Linux treat everything as a file?  

---


