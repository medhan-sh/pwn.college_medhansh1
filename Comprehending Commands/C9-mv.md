# Comprehending Commands 

### moving files 

**Flag:** `pwn.college{UqI5pqWbLpyp17lVRHKCAszq9BG.0VOxEzNxwiN2kjNzEzW}`

Used ls command to find the flag found out was in the wrong directory could have used the absolute path to move files but changed to root directory first to move the file 

```
hacker@commands~moving-files:~$ ls
9  a  b
hacker@commands~moving-files:~$ cd /
hacker@commands~moving-files:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~moving-files:/$ mv flag /tmp/hack-the-planet
Correct! Performing 'mv flag /tmp/hack-the-planet'.
hacker@commands~moving-files:/$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{UqI5pqWbLpyp17lVRHKCAszq9BG.0VOxEzNxwiN2kjNzEzW}
```

## What I learned

1. Introduction to mv command 
2. There are two uses for the mv command like we see in the example it changed the name of the file and during the        challenge we see its other use which is to move files from one location to other.

## References

None 
