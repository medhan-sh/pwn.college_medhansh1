# Practicing Piping 

### Put challenge description here

**Flag:** `pwn.college{Uue0OfshRmyxld0_SzCskcIElKF.0lNwMDOxwiN2kjNzEzW}`

Used diff command with on the two commands directly using process substitution to obtain th flag 

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
29a30
> pwn.college{Uue0OfshRmyxld0_SzCskcIElKF.0lNwMDOxwiN2kjNzEzW}
```

## What I learned

1. Process Substitution creates a temporarry file for the storing the output of commands so they can be used as inputs    for other commands.
2. This is done by `<(command)`.

## References

NONE
