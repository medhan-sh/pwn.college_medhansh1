# Untangling Users 

### Becoming Root with su 

**Flag:** `pwn.college{EkcekswqPdVFrw5JLXAffm2Ys1A.QX1UDN1wiN2kjNzEzW}`

Used `su` with the given password to gain root access then read `flag` to obtain the flag. 

```
hacker@users~becoming-root-with-su:~$ su 
Password: 
root@users~becoming-root-with-su:/home/hacker# cat flag
pwn.college{EkcekswqPdVFrw5JLXAffm2Ys1A.QX1UDN1wiN2kjNzEzW}
root@users~becoming-root-with-su:/home/hacker# 
```

## What I learned

1. SUID is a special file permission it changes the status from user to owner.
2. `su` grants you a root shell after performing a security check
3. `su` is used to change between different users on the same device. 

## References

NONE
