# 05 - File Transfer

## Objective
Test bidirectional file transfers between Windows and Ubuntu Server.

## Dedicated Shared Directory
The server uses:
```text
/home/<USERNAME>/shared/
```

## Windows to Ubuntu
From Windows PowerShell:
```powershell
sftp <USERNAME>@192.168.1.55
```

Inside SFTP:
```text
cd shared
put test.txt
```

A real image was also uploaded:
```text
put "C:\Users\User\Pictures\Screenshots\stars.png"
```

The remote directory contained:
```text
stars.png
test.txt
```

## Ubuntu to Windows
The `get` command was used:
```text
get test.txt
```

This confirmed bidirectional transfer.

## Useful SFTP Commands
```text
ls
cd shared
put filename
get filename
lpwd
lls
```

## Result
Bidirectional SFTP transfers were successfully tested between Windows and Ubuntu.
