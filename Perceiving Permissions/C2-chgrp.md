# Perceiving Permissions 

### Groups and Files 

**Flag:** `pwn.college{k-Z5F-4CWZFg9R5qVsOWliElOQ7.QXxcjM1wiN2kjNzEzW}`

Used `chgrp` to give group access to user hacker then read the file to obtain the flag 

```
hacker@permissions~groups-and-files:~$ chgrp hacker flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{k-Z5F-4CWZFg9R5qVsOWliElOQ7.QXxcjM1wiN2kjNzEzW}
```

## What I learned

1. Unlike `chown` which changes the ownership of a file completely `chgrp` gives group accss to a file making it          accessible by multiple users.

## References

NONE
