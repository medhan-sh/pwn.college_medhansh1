# Chaining Commands 

### Scripting with Multiple Conditions 

**Flag:** `pwn.college{EHCGBZiL1dRgvZ_szCkQd-LeCPN.0FOzMDOxwiN2kjNzEzW}`

Tried something new this time chained all the commands into one the challenge wanted to write multiple conditions using `elif` the code is 
```
if [ "$1" == "hack" ]; then
  echo "the planet"
elif [ "$1" == "pwn" ]; then
  echo "college"
elif [ "$1" == "learn" ]; then
  echo "linux"
else
  echo "unknown"
fi
```
Wrote this inside th script then ran the command`/challenge/run` to obtain the flag after making the script executable.

```
hacker@chaining~scripting-with-multiple-conditions:~$ { echo '#!/bin/bash'; echo 'if [ "$1" == "hack" ]; then'; echo '  echo "the planet"'; echo 'elif [ "$1" == "pwn" ]; then'; echo '  echo "college"'; echo 'elif [ "$1" == "learn" ]; then'; echo '  echo "linux"'; echo 'else'; echo '  echo "unknown"'; echo 'fi'; } > /home/hacker/solve.sh && chmod u+x /home/hacker/solve.sh && /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{EHCGBZiL1dRgvZ_szCkQd-LeCPN.0FOzMDOxwiN2kjNzEzW}
```

## What I learned

1. Simmilar to last one introduced a new conditional `elif` this time. 

## References

NONE
