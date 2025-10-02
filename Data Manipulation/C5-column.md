# Data Manipulation 

### Extracting Specific Section of text 

**Flag:** `pwn.college{0J5gitoBQI5FwqhOTgX0bRH9XVm.01NxEzNxwiN2kjNzEzW}`

Aftet running the command `/challenge/run` i got to know that i needed to segregate the second column so used `cut` as instructed with process substitution then deleted all the newlines after piping the output to obtain the flag.

```
hacker@data~extracting-specific-sections-of-text:~$ cut -d " " -f 2 <(/challenge/run) | tr -d "\n"
pwn.college{0J5gitoBQI5FwqhOTgX0bRH9XVm.01NxEzNxwiN2kjNzEzW}
```

## What I learned

1. Using `cut`.
2. `cut` is used to gather specific columns of data it is used with `-d` argument to specify the diffrentiator then `-f` to specify the column no..

## References

NONE
