# Shell Variables - Printing exported variables
This challenge teaches us the use of env command in printing exported variables.

## My solve
**Flag:** `pwn.college{cPPvyqsos92Fd8nvwrNhFerKZqm.QX4UTN0wSN2kjNzEzW}`

Following the challenge instructions, I ran the env command to print out all the exported variables and then found the flag from there.

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=37d33839c1f046e0ab0aa78e4310571e28e0cd350aa84321f519908452235007
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{cPPvyqsos92Fd8nvwrNhFerKZqm.QX4UTN0wSN2kjNzEzW}
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
This challenge taught me how to use the env command.

## Incorrect tangents 
NA

## References
NA
