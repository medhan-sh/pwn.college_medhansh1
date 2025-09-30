# Practicing Piping 

### Duplicating piped data with tee 

**Flag:** `pwn.college{ExRF15VW_BvVgKeZVNF56vEu6pO.QXxITO0wiN2kjNzEzW}`

This challenge made me question my life decisions this was just not happening. Took a friends help to understand i needed to interecept /challenge/pwn output into pwn then read the file to gain the secret argument  then pipe's /challenge/pwn with right argument to /challenge/college to obtain the flag .

```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "ExRF15VW"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret ExRF15VW | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{ExRF15VW_BvVgKeZVNF56vEu6pO.QXxITO0wiN2kjNzEzW}
```

## What I learned

1. Using tee .
2. tee command reads data from standard input and simultaneously writes that to an ouput and a file .
3. How not to let your emotions take over rational decision making, and to control anger. 

## References

Garrisht tp-4
