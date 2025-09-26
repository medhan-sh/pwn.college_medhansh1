# Comprehending Commands 

### touching files 

**Flag:** `pwn.college{cxhKYihO-riMH_bO9sNtVeM3_2R.QXwMDO0wiN2kjNzEzW}`

Used the 'touch' command to create to new files pwn and college, tried fiddling with the command to find if it works woth absolute paths or you HAVE to be in the directory you want to create the file in.

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls /tmp
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ /challnege/run
bash: /challnege/run: No such file or directory
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{cxhKYihO-riMH_bO9sNtVeM3_2R.QXwMDO0wiN2kjNzEzW}
hacker@commands~touching-files:~$ touch /tmp/abc
hacker@commands~touching-files:~$ ls /tmp
abc  bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
```

## What I learned

1. Intro to touch command.
2. touch command is the standard command used for making new empty files in a directory
3. The command can also work with absoulte path .

## References

None 
