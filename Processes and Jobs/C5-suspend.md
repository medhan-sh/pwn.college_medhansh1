# Processes and Jobs 

### Suspending Processes 

**Flag:** `pwn.college{Qhw5SikziEjS4YhT7RJ_MMc2wy0.QX1QDO0wiN2kjNzEzW}`

The challenge wanted me to suspend the process then run it again to obtain the flag. 

```
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 09:41 pts/0    00:00:00 bash /challenge/run
root         148     146  0 09:41 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 09:41 pts/0    00:00:00 bash /challenge/run
root         153     136  0 09:42 pts/0    00:00:00 bash /challenge/run
root         155     153  0 09:42 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{Qhw5SikziEjS4YhT7RJ_MMc2wy0.QX1QDO0wiN2kjNzEzW}
```

## What I learned

1. `ctrl+z` makes the program suspend in the background.

## References

NONE
