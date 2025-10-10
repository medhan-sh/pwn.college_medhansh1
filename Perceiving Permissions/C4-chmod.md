# Perceiving Permissions

### Changing Permissions 

**Flag:** `pwn.college{gaRxERRpB1ikApjR4IDzxmtEiM9.QXzcjM1wiN2kjNzEzW}`

After finding out the permissions associated with the file `flag` used `chmod 0+rwx` to give others access to read,write and execute. Read the file to obtain the file. 

```
hacker@permissions~changing-permissions:~$ ls -l /
total 64
lrwxrwxrwx    1 root root    7 Apr  4  2025 bin -> usr/bin
drwxr-xr-x    2 root root 4096 Apr 15  2020 boot
drwxr-xr-x    1 root root 4096 Oct 10 15:43 challenge
drwxr-xr-x    6 root root  380 Oct 10 15:43 dev
drwxr-xr-x    1 root root 4096 Oct 10 15:43 etc
-r--------    1 root root   60 Oct 10 15:43 flag
drwxr-xr-x    1 root root 4096 Sep 26 17:24 home
lrwxrwxrwx    1 root root    7 Apr  4  2025 lib -> usr/lib
lrwxrwxrwx    1 root root    9 Apr  4  2025 lib32 -> usr/lib32
lrwxrwxrwx    1 root root    9 Apr  4  2025 lib64 -> usr/lib64
lrwxrwxrwx    1 root root   10 Apr  4  2025 libx32 -> usr/libx32
drwxr-xr-x    2 root root 4096 Apr  4  2025 media
drwxr-xr-x    2 root root 4096 Apr  4  2025 mnt
drwxr-xr-x    1 root root   16 Oct 26  2024 nix
drwxr-xr-x    1 root root 4096 Sep 26 17:24 opt
dr-xr-xr-x 3447 root root    0 Oct 10 15:43 proc
drwx------    1 root root 4096 Sep 26 17:24 root
drwxr-xr-x    1 root root 4096 Oct 10 15:43 run
lrwxrwxrwx    1 root root    8 Apr  4  2025 sbin -> usr/sbin
drwxr-xr-x    2 root root 4096 Apr  4  2025 srv
dr-xr-xr-x   13 root root    0 Aug 26 04:26 sys
drwxrwxrwt    1 root root 4096 Oct 10 15:43 tmp
drwxr-xr-x    1 root root 4096 Sep 26 17:09 usr
drwxr-xr-x    1 root root 4096 Sep 26 17:08 var
hacker@permissions~changing-permissions:~$ chmod o+rwx flag
hacker@permissions~changing-permissions:~$ cat flag
pwn.college{gaRxERRpB1ikApjR4IDzxmtEiM9.QXzcjM1wiN2kjNzEzW}
```

## What I learned

1. `chmod` is used to change the permissions associated with a file.
2. r-read,w-write,x-execute 

## References

NONE
