# Perceiving Permissions 

### The SUID bit 

**Flag:** `pwn.college{MKT5LuQlm5AOrZ7GdbwE-o56wKn.QXzEjN0wiN2kjNzEzW}`

I first added an SUID to `/challenge/getroot` by using `chmod u+s /challenge/getroot` which when executed gives me root access after which i simply read the file to obtain the flag. i went wrong with using the traditional way of using chmod to change the permissions and then reading the file .

```
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ cat flag
cat: flag: Permission denied
hacker@permissions~the-suid-bit:~$ ls -l /flag
-r-------- 1 root root 60 Oct 10 16:29 /flag
hacker@permissions~the-suid-bit:~$ chmod uo+x
This challenge restricts chmod to its simple usage:

    chmod MODE FILE
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{MKT5LuQlm5AOrZ7GdbwE-o56wKn.QXzEjN0wiN2kjNzEzW}
```

## What I learned

1. The "Set User ID" (SUID) bit is a special permission that, when set on an executable file, allows it to run with the privileges of the file's owner.
2. To provide this one must  `chmod u+s [program]`.

## References

NONE
