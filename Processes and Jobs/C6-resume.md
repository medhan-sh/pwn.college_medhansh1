# Processes and jobs

### Resuming programmes 

**Flag:** `pwn.college{wdgE4ssDH8rejYpsyGj6SUpgVUG.QX2QDO0wiN2kjNzEzW}`

Used `fg` to resume suspended program as instructed.

```
hacker@processes~resuming-processes:~$ /challenge/run 
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{wdgE4ssDH8rejYpsyGj6SUpgVUG.QX2QDO0wiN2kjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I learned

1. Suspended programmes can be resumed by `fg`.

## References

NONE
