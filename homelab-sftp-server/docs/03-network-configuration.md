# 03 - Network Configuration

## Objective
Configure the Ubuntu VM so other devices on the local network can reach the SFTP server.

## Initial NAT Configuration
The VM initially used VirtualBox NAT networking and received an address similar to:
```text
10.0.2.15
```

NAT allowed the VM to access the internet, but it was not convenient for direct phone-to-VM access.

## Bridged Adapter
VirtualBox networking was changed to:
```text
Bridged Adapter
```

The VM then received:
```text
192.168.1.55
```

Bridged networking placed the VM on the same LAN as the host and phone.

## Verification
```bash
ip addr
hostname -I
ip route
ping -c 4 google.com
```

## Network Design
```text
Phone
  |
Wi-Fi
  |
Home Router
  |
Windows Laptop
  |
VirtualBox Bridged Adapter
  |
Ubuntu Server
192.168.1.55
```

## Result
The VM successfully joined the local network and became reachable from the Windows host and mobile device.
