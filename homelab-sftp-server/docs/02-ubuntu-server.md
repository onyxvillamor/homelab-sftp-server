# 02 - Ubuntu Server

## Objective
Set up a lightweight Linux server that can host SSH and SFTP services.

## Why Ubuntu Server?
Ubuntu Server provides a CLI-based environment that is well suited to server workloads and consumes fewer resources than a desktop environment.

## Initial Verification
```bash
lsb_release -a
```
Checks Ubuntu release information.

```bash
whoami
```
Displays the current username.

```bash
pwd
```
Displays the current working directory.

```bash
ls
```
Lists files and directories.

## Directory Management
Create the dedicated transfer directory:
```bash
mkdir ~/shared
```

Move the test file:
```bash
mv ~/test.txt ~/shared
```

Verify:
```bash
ls ~/shared
```

The resulting directory is:
```text
/home/<USERNAME>/shared/
```

## Result
Ubuntu Server was successfully installed and configured as the Linux server environment for the homelab.
