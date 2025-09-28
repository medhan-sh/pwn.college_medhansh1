# File Globbing 

### Multiple Globs 

**Flag:** `pwn.college{MbZ9NirYaca0Szk3AD_n0eAKWY_.0lM3kjNxwiN2kjNzEzW}`

After changing to /challenge/flies I was supposed to run /challenge/run with an 3 character argument containing the letter p so I started globbing as instructed case by case to obtain the flag.
well lookin at it now there was only one possible case `*p*` * and ** would give the same output .

```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run p**
Your expansion did not expand to the requested files (happy optimistic pwning 
splendid uplifting).
Instead, it expanded to:
pwning
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{MbZ9NirYaca0Szk3AD_n0eAKWY_.0lM3kjNxwiN2kjNzEzW}
```

## What I learned

1. Using multiple globbing on a string 

## References

NONE
