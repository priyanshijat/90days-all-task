# Linux
## What is Linux?
Linux is an open-source operating system (OS) based on Unix. It was first created by Linus Torvalds in 1991. Unlike Windows or macOS, Linux is free to use, modify, and distribute.

### Key points about Linux:
* **Open Source**: Its source code is freely available.

* **Kernel**: The core part of Linux is called the kernel. It manages hardware, processes, memory, and system calls.

* **Distributions**: Linux comes in many versions called distributions (distros) like Ubuntu, Fedora, Debian, CentOS, etc.

* **Multiuser**: Supports multiple users running programs at the same time.

* **Multitasking**: Can run many programs simultaneously.

* **Security**: Highly secure and widely used in servers, embedded systems, and desktops.

* **Command Line Interface (CLI)**: Linux is well-known for its powerful command-line shell (like Bash).

---
### 1. Create a user devops_user
```bash
sudo useradd -m devops_user
```
* -m creates a home directory for the user.
  
### 2. Create a group devops_team
```bash
sudo groupadd devops_team
```

### 3. Add devops_user to devops_team
```bash
sudo usermod -aG devops_team devops_user
```

### Set a password for devops_user
```bash
sudo passwd devops_user
```

### 5. Grant sudo access to devops_user
* Option 1: Add to the sudo group (on Ubuntu/Debian)
```bash
sudo usermod -aG sudo devops_user
```
* Option 2: Add a custom sudo rule
  ```bash
  sudo visudo
```
Then add this line at the end:
```bash
devops_user ALL=(ALL) NOPASSWD:ALL
```
NOPASSWD is optional. Remove it if you want to require password.

### 6. Restrict SSH login for certain users
Edit the SSH configuration file:
```bash
sudo nano /etc/ssh/sshd_config
```
To deny specific users from SSH:
Add this line (replace with actual usernames to deny):
```bash
DenyUsers user1 user2
```
Then restart SSH service:
```bash
sudo systemctl restart sshd
```

### ✅ Files Explained:

* /etc/passwd: Contains user account information.

* /etc/group: Contains group info.

* /etc/sudoers: Controls sudo access.

* /etc/ssh/sshd_config: Controls SSH server settings.
