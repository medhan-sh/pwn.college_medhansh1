# Chaining Commands 

### Scripting with Conditionals 

**Flag:** `pwn.college{M3SP5dK59qhgujQHSk4iYDKK1kH.0lNzMDOxwiN2kjNzEzW}`

The challenge wanted me to use conditionals in a way that if the first argument of shell script is pwn it prints college using that logic created `if [ "$1" == "pwn" ]; then'` then used `&&` to chain th output made the script executable then ran `/challnge/run` to obtain the flag.

```
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" == "pwn" ]; then' >> /home/hacker/solve.sh && echo '  echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod u+x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{M3SP5dK59qhgujQHSk4iYDKK1kH.0lNzMDOxwiN2kjNzEzW}
```

## What I learned

1. Using conditional logic and syntax like `if` and `then` inside of bash.
2. To close the if we need to use `fi`.

## References
NONE
