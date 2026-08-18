# 09 - Troubleshooting

This document records problems encountered during the project and how they were resolved.

## 1. SSH Service Was Inactive

### Symptom
```text
Active: inactive
```

### Resolution
```bash
sudo systemctl start ssh
sudo systemctl status ssh
sudo systemctl enable ssh
```

The service was confirmed as:
```text
Active: active (running)
```

---

## 2. VM Used a NAT Address

### Symptom
The VM initially received:
```text
10.0.2.15
```

### Cause
The VirtualBox adapter was configured for NAT.

### Resolution
The adapter was changed to:
```text
Bridged Adapter
```

The VM then received:
```text
192.168.1.55
```

This made direct LAN access possible.

---

## 3. SFTP Reported "No Such File or Directory"

### Symptom
```text
put test.txt
stat test.txt: No such file or directory
```

### Cause
SFTP was running from Ubuntu while `test.txt` existed on Windows.

### Resolution
SFTP was started from Windows PowerShell, where the local file existed:
```powershell
sftp <USERNAME>@192.168.1.55
```

The file then uploaded successfully.

### Lesson
SFTP has both local and remote filesystems. Useful commands include:
```text
pwd
lpwd
ls
lls
```

---

## 4. Ubuntu Server Displayed a CLI

### Symptom
The VM showed a black terminal-style screen instead of a graphical desktop.

### Cause
Ubuntu Server is designed to use a command-line interface by default.

### Resolution
No change was required. The CLI is appropriate for this server project.

## Troubleshooting Approach
1. Identify the symptom.
2. Determine whether it is related to the VM, network, service, or file path.
3. Check system status and configuration.
4. Test one component at a time.
5. Apply a targeted change.
6. Re-test the original function.
