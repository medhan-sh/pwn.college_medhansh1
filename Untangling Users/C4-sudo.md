# Untangling Users 

### Using sudo 

**Flag:** `pwn.college{MDBl-U_tB4hdG1J7r4A0U5u8RZ8.QX4UDN1wiN2kjNzEzW}`

After confirming the current user I used `sudo cat /etc/passwd` to figure out if there were any suspicious users i should look into to obtain the flag, coudn't find any obvious guesses so started with root `sudo su` gave me direct access to root shell without the passwrod used `cat /flag` to obtain the flag. 

```
hacker@users~using-sudo:~$ whoami 
hacker
hacker@users~using-sudo:~$ sudo cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
_apt:x:100:65534::/nonexistent:/usr/sbin/nologin
systemd-timesync:x:101:101:systemd Time Synchronization,,,:/run/systemd:/usr/sbin/nologin
systemd-network:x:102:103:systemd Network Management,,,:/run/systemd:/usr/sbin/nologin
systemd-resolve:x:103:104:systemd Resolver,,,:/run/systemd:/usr/sbin/nologin
mysql:x:104:105:MySQL Server,,,:/nonexistent:/bin/false
messagebus:x:105:106::/nonexistent:/usr/sbin/nologin
sshd:x:106:65534::/run/sshd:/usr/sbin/nologin
hacker:x:1000:1000::/home/hacker:/bin/bash
root:x:0:0:root:/root:/run/dojo/bin/bash
hacker:x:1000:1000:hacker:/home/hacker:/run/dojo/bin/bash
sshd:x:112:65534::/run/sshd:/usr/sbin/nologin
hacker@users~using-sudo:~$ sudo su 
root@users~using-sudo:/home/hacker# cat /flag
pwn.college{MDBl-U_tB4hdG1J7r4A0U5u8RZ8.QX4UDN1wiN2kjNzEzW}
root@users~using-sudo:/home/hacker# 



```

## What I learned

1. Unlike `su` which changes your shell to the specified user `sudo` runs commands as if you are the specified user
2. Learned the standard syntax `sudo [command]`, which executes a single command with root privileges.
3. Since `su` was already running as root with the help of `sudo`  it did not require any password to change to root.

## References

NONE
