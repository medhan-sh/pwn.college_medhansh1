# Shell Varriable

### Exporting Varriable 

**Flag:** `pwn.college{8jix1mUdylVAU5EME9k-JQ1E6I2.QXyYTN0wiN2kjNzEzW}`

Assigned values to PWN and COLLEGE and exported PWN varriable as instructed to obtain the flag. I did not export COLLEGE but somehow it still worked.

```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
Incorrect...
You have not set the COLLEGE variable to the correct value (it should be 
'PWN'). Do that before running this script! Even though it is not exported, in 
this challenge, we have ways to check...
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{8jix1mUdylVAU5EME9k-JQ1E6I2.QXyYTN0wiN2kjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I learned

1. Variables that you set in a shell session are local to that shell process.
2. Exporting varriable

## References
NONE
