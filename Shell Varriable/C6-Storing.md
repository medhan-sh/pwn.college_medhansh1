# Shell Varriable 

### Storing Command Output 

**Flag:** `pwn.college{M3OhvtrSp8yx4LRKnfFdrncWWUg.QX1cDN1wiN2kjNzEzW}`

Stored the out put of `/challenge/run` in the varriable PWN then read the varriable to obtain the flag. 

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ 
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{M3OhvtrSp8yx4LRKnfFdrncWWUg.QX1cDN1wiN2kjNzEzW}
```

## What I learned

1. How to Assign the output of a command to a varriable.

## References

NONE
