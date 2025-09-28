# File Globbing 

### Mixing globs

**Flag:** `pwn.college{scSjOrfQ0_yBr9YhOGQHRN94_GG.QX1IDO0wiN2kjNzEzW}`

After changing to /challenge/files i listed out the files to look for patters the starting characters c,e,p were unique so i used `[cep]` globbing combined with `*` to glob out the correct arguments .

```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing      delightful   great       jovial    magical     pwning   splendid   victorious  youthful
beautiful    educational  happy       kind      nice        queenly  thrilling  wonderful   zesty
challenging  fantastic    incredible  laughing  optimistic  radiant  uplifting  xenial
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{scSjOrfQ0_yBr9YhOGQHRN94_GG.QX1IDO0wiN2kjNzEzW}
```

## What I learned

1. Using various different types of globes together to get desired outcomes. 

## References

NONE
