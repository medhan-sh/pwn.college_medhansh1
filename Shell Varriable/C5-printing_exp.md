# Shell Varriable 

### Printing Exported Varriable 

**Flag:** `pwn.college{ARwmlNIj4gUifjB2_mjmRX3jyUz.QX4UTN0wiN2kjNzEzW}`

Used `env` command as instructed to obtain the flag.

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=f95f16333751b976a5223b05cfda4dddfe16d567fda3ed8905d5e7b2dc73279b
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{ARwmlNIj4gUifjB2_mjmRX3jyUz.QX4UTN0wiN2kjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I learned

1. `env` command lists out all the exported command.

## References

NONE
