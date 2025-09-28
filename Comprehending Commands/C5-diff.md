# Comprehending Commands 

### comparing files

**Flag:** `pwn.college{8wmxIcKq-SPqf2b5-elWoNP1aOa.01MwMDOxwiN2kjNzEzW}`

Used the `diff` command as instructed 

```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
66a67
> pwn.college{8wmxIcKq-SPqf2b5-elWoNP1aOa.01MwMDOxwiN2kjNzEzW}
```

## What I learned

1. Intro to diff command
2. 'diff' command reads and compares the two files line by line.
3. How the output is read for diff command 
   66a67: 66 reffers to line number 66 in the first file, a stands for add to make it simmilar , 67 reffers to line       number 67 in the second file. c reffers to change d reffers to delete.

## References

NONE 
