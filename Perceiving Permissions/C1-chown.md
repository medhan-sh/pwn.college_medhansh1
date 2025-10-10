# Perceiving Permissions 

### hanginf File owenership 

**Flag:** `pwn.college{4p_G5LdzMXEPKd1VctPoRwTWr5V.QXxEjN0wiN2kjNzEzW}`

Used `chown` as instructed to change the ownership of the file `flag` from root to hacker then read the flag to obtain the flag. 
```
hacker@permissions~changing-file-ownership:~$ chown hacker flag
hacker@permissions~changing-file-ownership:~$ cat flag
pwn.college{4p_G5LdzMXEPKd1VctPoRwTWr5V.QXxEjN0wiN2kjNzEzW}
```

## What I learned

1. Access to files is dictated by ownership and the `chown` command can change the ownership of a file.
2. Only the root user can change the ownership of the file. 

## References

NONE
