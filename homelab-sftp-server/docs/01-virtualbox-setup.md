# 01 - VirtualBox Setup

## Objective
Create an isolated Linux server environment on a Windows laptop without replacing the host operating system.

## Hypervisor
**VirtualBox**

## VM Configuration
| Resource | Configuration |
|---|---|
| Hypervisor | VirtualBox |
| Operating System | Ubuntu Server |
| RAM | 5 GB |
| CPU | 2 virtual CPUs |
| Network | NAT initially, later Bridged Adapter |
| Storage | Virtual disk |

> Resource allocations can be adjusted based on the host laptop's available RAM and CPU.

## Installation Process
1. Download the Ubuntu Server ISO.
2. Create a new VM in VirtualBox.
3. Attach the Ubuntu Server ISO.
4. Allocate RAM, CPU, and virtual storage.
5. Start the VM.
6. Complete the Ubuntu Server installation.
7. Reboot into the installed system.
8. Verify that the Ubuntu CLI is accessible.

## Why a VM?
Using a VM allows the server environment to run alongside Windows. It also makes experimentation safer because the virtual machine can be backed up, recreated, or modified independently of the host operating system.

## Result
The Ubuntu Server VM successfully booted to the command-line interface and was ready for network and SSH configuration.
