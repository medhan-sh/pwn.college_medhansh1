# Processes and Jobs

### Listing Processes 

**Flag:** `pwn.college{MC4oWXQ9N8jd7SSl5NRUDEsaCuh.QX4MDO0wiN2kjNzEzW}`

As it was given the command was launched so i used `ps -ef` to list all the running commands and found the command which gave the flag. 

```
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 16:30 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 16:30 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 16:30 ?        00:00:00 /challenge/7414-run-2422
root         135     132  0 16:30 ?        00:00:00 sleep 6h
hacker       146       1  0 16:30 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --int
hacker       150     146  0 16:30 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160       0  0 16:30 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run
hacker       166     160  0 16:30 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       175     150  0 16:47 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/7414-run-2422
Yahaha, you found me! Here is your flag:
pwn.college{MC4oWXQ9N8jd7SSl5NRUDEsaCuh.QX4MDO0wiN2kjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## What I learned

1. Listing processes with `ps` simmilar to `ls ` which is used to list out files `ps` lists out all the processes running.
2. Arguments like `-ef`,`-aux` 
    -ef shows the standard syntax which is the PPID 
    -aux shows BSD syntax which shows the %CPU %MEM.

## References

NONE
