# 06 - Phone Access

## Objective
Connect a mobile phone to the Ubuntu SFTP server and transfer files over the local Wi-Fi network.

## Network Requirement
The phone must be able to reach the Ubuntu VM's LAN IP address:
```text
192.168.1.55
```

The phone and VM may use different Wi-Fi bands, such as 2.4 GHz and 5 GHz, as long as the router permits communication between them.

## SFTP Client Configuration
| Field | Value |
|---|---|
| Protocol | SFTP |
| Host | `<VM_IP>` |
| Port | 22 |
| Login | `<USERNAME>` |
| Password | Ubuntu account password |
| Login path | `/home/<USERNAME>/shared` |

Sensitive credentials are intentionally not documented.

## Result
The phone successfully connected to the Ubuntu SFTP server and accessed the dedicated shared directory.

## Security Note
This project is intended for local-network access. The SFTP server should not be exposed directly to the public internet without additional security controls.
