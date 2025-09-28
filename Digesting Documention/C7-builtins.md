# Digesting Documents 

### Help for builtins

**Flag:** `pwn.college{wM0y8-0No3_oq6crDlDuxKjEbg2.QX0ETO0wiN2kjNzEzW}`

Since `challenge` was a shell builting used help as it was instructed read through the output to find I have to invoke -secret VALUE command to obtain the flag. 
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "wM0y8-0N".
hacker@man~help-for-builtins:~$ challenge --secret wM0y8-0N
Correct! Here is your flag!
pwn.college{wM0y8-0No3_oq6crDlDuxKjEbg2.QX0ETO0wiN2kjNzEzW}
```

## What I learned

1. Builtin are commands which are neither programmed with man nor with help, they are invoked jsut like commands.
2. Using help for builtin commands. 

## References

NONE
