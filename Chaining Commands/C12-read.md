# Chaining Commands 

### Reasding shell scripts 

**Flag:** `pwn.college{cL4nV0Tg8Chohjsv9FE_bqApsIT.0lMwgDOxwiN2kjNzEzW}`

This one was pretty easy I read the script invoked by `/challenge/run` to find out the password was 'hack the PLANET` then executed the command with this password to obtain the flag.

```
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run 
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run 
hack the PLANET
CORRECT! Your flag:
pwn.college{cL4nV0Tg8Chohjsv9FE_bqApsIT.0lMwgDOxwiN2kjNzEzW}
```

## What I learned

1. Reading a shell script to understand the logic behind it.

## References

NONE
