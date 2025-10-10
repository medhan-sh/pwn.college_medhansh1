# Chaining Commands

### Understanding Shebangs

**Flag:** `pwn.college{012fk9j-G2ccX5bwGM0lDvZTvAV.0VOzMDOxwiN2kjNzEzW}`

After creating the desird script I made it executable then ran the command `/challenge/run` to obtain the flag.

```
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > /home/hacker/solve.sh && echo 'echo "hack the planet"' >> /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod u+x ~/solve.sh 
hacker@chaining~understanding-shebangs:~$ /challenge/run 
Testing your script...
Perfect! Your flag:
Flag: pwn.college{012fk9j-G2ccX5bwGM0lDvZTvAV.0VOzMDOxwiN2kjNzEzW}
```

## What I learned

1. Programs start with `#!` to mark there form of interpretation for linx these are called shebangs.

## References

NONE
