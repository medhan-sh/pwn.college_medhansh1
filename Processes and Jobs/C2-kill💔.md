# Processes and Jobs 

### Killing Proccesses

**Flag:** `pwn.college{4PL1BGyWnExOGv74ucGdBlPeAW4.QXyQDO0wiN2kjNzEzW}`

First used `ps -f` to figure out the PID for the command /challenge/dont_run then used `kill` as instructed to kill the command.
```
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 07:29 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 07:29 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 07:29 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 07:29 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 07:29 ?        00:00:00 sleep 6h
hacker       148       1  0 07:29 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --int
hacker       152     148  0 07:29 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       162     152  0 07:30 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge.run 
bash: /challenge.run: No such file or directory
hacker@processes~killing-processes:~$ /challenge/run 
Great job! Here is your payment:
pwn.college{4PL1BGyWnExOGv74ucGdBlPeAW4.QXyQDO0wiN2kjNzEzW}
```

## What I learned

1. Using `kill ` command to terminate a command
2. `kill` when used with PID of the command you wanna terminate as the argument. 

## References

NONE
