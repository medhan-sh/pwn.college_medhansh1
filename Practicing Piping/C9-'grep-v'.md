# Practicing Piping 

### Filtering with grep -v

**Flag:** `pwn.college{UjsdTB5u60ZU-UrzP_Y2d85QfEj.0FOxEzNxwiN2kjNzEzW}`

Succesfully used `grep -v` to filter out all the DECOYS to obtain the flag 

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{UjsdTB5u60ZU-UrzP_Y2d85QfEj.0FOxEzNxwiN2kjNzEzW}
```

## What I learned

1. Using `grep -v` to filter out all the files including the string given in the argument. 

## References

NONE
