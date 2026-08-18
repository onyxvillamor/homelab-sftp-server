# Self-Hosted SFTP File Server Homelab

A personal homelab project using VirtualBox, Ubuntu Server, OpenSSH, and SFTP to securely transfer files between a Windows laptop, mobile phone, and Linux server over a local network.

## Project Goals
- Learn Linux server administration
- Practice virtualization with VirtualBox
- Understand LAN networking and IP addressing
- Configure SSH and SFTP
- Transfer files securely between devices
- Practice troubleshooting
- Build a foundation for firewalling and server hardening

## Architecture
```text
                    Home Network
                         |
              +----------+----------+
              |                     |
          Phone                 Windows Laptop
              |                     |
              +----------+----------+
                         |
                    VirtualBox
                         |
                  Ubuntu Server
                         |
                  OpenSSH / SFTP
                         |
                 /home/<USER>/shared
```

## Technologies
- VirtualBox
- Ubuntu Server
- Linux
- OpenSSH
- SFTP
- IPv4
- TCP/IP
- Windows PowerShell

## Implemented Features
- Ubuntu Server virtual machine
- Bridged network connectivity
- SSH remote administration
- SFTP file transfer
- Dedicated shared directory
- Windows-to-Ubuntu file transfer
- Ubuntu-to-Windows file transfer
- Mobile phone SFTP access

## Security Considerations
The server is intended for local-network use. Passwords, private keys, personal files, and other sensitive information are not stored in this repository.

Planned improvements include UFW, SSH keys, restricted SFTP users, least-privilege permissions, log monitoring, and backups.

## Documentation
1. [VirtualBox Setup](docs/01-virtualbox-setup.md)
2. [Ubuntu Server](docs/02-ubuntu-server.md)
3. [Network Configuration](docs/03-network-configuration.md)
4. [SSH and SFTP Setup](docs/04-ssh-sftp-setup.md)
5. [File Transfer](docs/05-file-transfer.md)
6. [Phone Access](docs/06-phone-access.md)
7. [UFW Firewall](docs/07-firewall-ufw.md)
8. [Security Hardening](docs/08-security-hardening.md)
9. [Troubleshooting](docs/09-troubleshooting.md)
10. [Command Reference](notes/commands.md)
