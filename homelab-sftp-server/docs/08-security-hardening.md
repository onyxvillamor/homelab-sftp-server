# 08 - Security Hardening

## Current Security Controls
- SSH/SFTP encrypted communication
- Account-based authentication
- Local-network access
- Dedicated shared directory
- Virtualized server environment

## Planned Improvements

### 1. UFW Firewall
Restrict unnecessary incoming connections.

### 2. SSH Key Authentication
Replace password-based SSH authentication with public/private key authentication.

### 3. Disable Password Authentication
After verifying key-based authentication, password-based SSH authentication can be disabled.

### 4. Dedicated SFTP User
Create a separate account specifically for file transfers instead of using the primary administrative account.

### 5. Least-Privilege Permissions
Limit the SFTP user's access to only the directories and files required for file transfer.

### 6. SSH Log Monitoring
Review authentication logs to identify failed or unexpected login attempts.

### 7. Backups
Create backups of important transferred data outside the VM.

## Security Principle
The project will follow least privilege: users and services should have only the access required for their intended tasks.

## Status
These improvements are planned unless explicitly marked as implemented later.
