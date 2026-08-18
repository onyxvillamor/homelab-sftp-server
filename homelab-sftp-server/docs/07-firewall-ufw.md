# 07 - UFW Firewall

## Status
**Planned / To Be Implemented**

UFW has not yet been configured as part of the current project state.

## Objective
Use UFW (Uncomplicated Firewall) to control incoming and outgoing network traffic on Ubuntu.

## Planned Configuration
Check status:
```bash
sudo ufw status
```

Allow SSH:
```bash
sudo ufw allow 22/tcp
```

Enable UFW:
```bash
sudo ufw enable
```

Verify:
```bash
sudo ufw status verbose
```

## Security Goal
- Allow SSH/SFTP on TCP port 22
- Deny unnecessary incoming connections
- Allow required outgoing traffic
- Verify that SFTP continues to work after firewall activation

## Important
Do not enable a firewall on a remote system until required management access has been explicitly allowed.

Update this document after UFW is actually configured and tested.
