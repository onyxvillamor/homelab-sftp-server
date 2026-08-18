# Command Reference

## Linux Navigation and Files

### List files
```bash
ls
```

### Print working directory
```bash
pwd
```

### Change directory
```bash
cd ~/shared
```

### Create a directory
```bash
mkdir ~/shared
```

### Move a file
```bash
mv ~/test.txt ~/shared
```

## Networking

### Display interfaces
```bash
ip addr
```

### Show IP address
```bash
hostname -I
```

### Show routes
```bash
ip route
```

### Test connectivity
```bash
ping -c 4 google.com
```

## SSH Service

### Update packages
```bash
sudo apt update
```

### Install OpenSSH Server
```bash
sudo apt install openssh-server
```

### Start SSH
```bash
sudo systemctl start ssh
```

### Check SSH status
```bash
sudo systemctl status ssh
```

### Enable SSH at boot
```bash
sudo systemctl enable ssh
```

### Check whether SSH is enabled
```bash
sudo systemctl is-enabled ssh
```

## SSH Client
From Windows PowerShell:
```powershell
ssh <USERNAME>@<VM_IP>
```

## SFTP
Connect:
```powershell
sftp <USERNAME>@<VM_IP>
```

Upload:
```text
put filename
```

Download:
```text
get filename
```

List remote files:
```text
ls
```

Change remote directory:
```text
cd shared
```

Show local directory:
```text
lpwd
```

List local files:
```text
lls
```

Exit:
```text
exit
```

## Security Reminder
Never commit passwords, private SSH keys, API keys, personal files, or other sensitive credentials to GitHub.
