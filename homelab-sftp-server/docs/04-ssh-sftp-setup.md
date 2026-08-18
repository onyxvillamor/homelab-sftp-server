# 04 - SSH and SFTP Setup

## Objective
Install and configure OpenSSH to provide secure remote administration and SFTP file transfer.

## SSH
SSH stands for **Secure Shell**. It is a protocol used to securely connect to and administer remote systems.

Example:
```powershell
ssh <USERNAME>@192.168.1.55
```

## SFTP
SFTP stands for **SSH File Transfer Protocol**. It provides file transfers through an SSH connection and normally uses TCP port 22.

## Install OpenSSH Server
```bash
sudo apt update
sudo apt install openssh-server
```

## Start and Enable SSH
```bash
sudo systemctl start ssh
sudo systemctl status ssh
sudo systemctl enable ssh
sudo systemctl is-enabled ssh
```

Expected running state:
```text
Active: active (running)
```

Expected enabled state:
```text
enabled
```

## SSH Test
From Windows PowerShell:
```powershell
ssh <USERNAME>@192.168.1.55
```

## SFTP Test
```powershell
sftp <USERNAME>@192.168.1.55
```

A successful connection displays:
```text
sftp>
```

## Result
OpenSSH was successfully installed, enabled, and used for both SSH remote administration and SFTP file transfers.
