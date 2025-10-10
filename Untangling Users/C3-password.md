# Untangling Users

### Cracking Passwords

**Flag:** `pwn.college{wxwmwEUcBe6KJDQWfPeoCNrIJdc.QX3UDN1wiN2kjNzEzW}`

This was kinda cool. The challenge gave me the location of the file where the encrypted passwords are stored `/challenge/shadow-leak` I used john to decrypt the password then gained access to zardus to obtain the flag.

```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04899g/s 285.3p/s 285.3c/s 285.3C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{wxwmwEUcBe6KJDQWfPeoCNrIJdc.QX3UDN1wiN2kjNzEzW}
```

## What I learned

1. `/etc/shadow` is used to store all the passwords in one place. This file can only be read with root access.
2. Passwords are stored in one-way cryptogryphic hash
3. Using `john` to decrypt the password.

## References

NONE
