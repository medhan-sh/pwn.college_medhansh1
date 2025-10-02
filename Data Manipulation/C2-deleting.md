# Data Manipulation 

### Deleting Characters

**Flag:** `pwn.college{sDqQO8JdI616qoQGAB3slRPkFTO.0FNxEzNxwiN2kjNzEzW}`

Used `tr -d` as instructed to delete ^ and % from the flag.

```
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{sDqQO8JdI616qoQGAB3slRPkFTO.0FNxEzNxwiN2kjNzEzW}
```

## What I learned

1. Using `tr -d` to delete characters. 

## References

NONE
