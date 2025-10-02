# Data Manipulation 

### Extracting First lines with head

**Flag:** `pwn.college{0xzhC8WN_NmpwJamBCgPDnHTpJa.0lNxEzNxwiN2kjNzEzW}`

Used `head` to take only the first few lines and used it with the argument `n -7` to only get the first 7 lines .

```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{0xzhC8WN_NmpwJamBCgPDnHTpJa.0lNxEzNxwiN2kjNzEzW}
```

## What I learned

1. Using the `head` command
2. `head` is used to extract only the first few lines  of a file we can set the ammount of lines with `n -7` argument. 

## References

NONE
