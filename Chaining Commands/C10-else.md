# Chaining Commands 

### Scripting with Default Case 

**Flag:** `pwn.college{M2BUvU8qB5OD86DDN9xiR-UCsVx.01NzMDOxwiN2kjNzEzW}}`

This challenge was very simmilar to the previous challenge they just introduced an `else` the challenge wanted me to print college if first argument was pwn and 'nope' is anything else. Using that logic the code would be 

```
if [ "$1" == "pwn" ]; then
echo "college"
else
echo "nope"
```
I directed it inside the script then ran `/challenge/run` to obtain the flag. 



```
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'if [ "$1" == "pwn" ]; then' >> /home/hacker/solve.sh && echo '  echo "college"' >> /home/hacker/solve.sh && echo 'else' >> /home/hacker/solve.sh && echo '  echo "nope"' >> /home/hacker/solve.sh && echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run 
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{M2BUvU8qB5OD86DDN9xiR-UCsVx.01NzMDOxwiN2kjNzEzW}
```

## What I learned

1. Simmilar to last one just introduced `else`.

## References

NONE
