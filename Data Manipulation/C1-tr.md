# Data Manipulation 

### Translating Characters 

**Flag:** `pwn.college{A11HhVGKQOjZeIf3L7oaIP8sG3w.01MxEzNxwiN2kjNzEzW}`

Used `tr` to translate all the upper case to lowe case but failed to translate all the lower case to upper case. Fixed that to obtain the flag. 

```
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZ abcdefghijklmnopqrstuvwxyz
your case-swapped flag:
pwn.college{a11hhvgkqojzeif3l7oaip8sg3w.01mxeznxwin2kjnzezw}
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{A11HhVGKQOjZeIf3L7oaIP8sG3w.01MxEzNxwiN2kjNzEzW}
```

## What I learned

1. Using `tr` to translate characters recieved in input.
2. `tr` changes the character recived in first arguments to the character in the output it can change multiple              characters at once

## References

NONE
