#  Pondering Paths 

### Program and absolute paths

**Flag:** `pwn.college{8-JbMFXruOvbYuQDxL6nwDdkJ_Z.QX1QTN0wiN2kjNzEzW}`

Adhered to the instruction provided. As directed in the content video i wanted to know which directory i was currently inside of so used pwd .

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{8-JbMFXruOvbYuQDxL6nwDdkJ_Z.QX1QTN0wiN2kjNzEzW}
hacker@paths~program-and-absolute-paths:~$ pwd
/home/hacker

```

## What I learned

1. One can run a command regardless of their current position if you know the absolute path to it .
2. Unlike the first challenge where command was inside the root directory, the command was in another challenge           directory which was inside root directory /challenge/run .

## References

NONE
