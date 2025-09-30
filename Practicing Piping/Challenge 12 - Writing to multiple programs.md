# Practicing Piping 12 - Writing to multiple programs
This challenge essentially aims to teach us output process substitution with the >(command) argument.

## My solve
**Flag:** `pwn.college{4EeysbAnVj4CdIu4rzfig2WH5pr.QXwgDN1wSN2kjNzEzW}`

Following the challenge instructions, I duplicated the output of the challenge/hack command and put it as input into the /challenge/the and challenge/planet commands using tee and >(command) arguments.

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
124621756313729778
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{4EeysbAnVj4CdIu4rzfig2WH5pr.QXwgDN1wSN2kjNzEzW}
```

## What I learned
This challenge taught me the difference between >(command) and <(command) and the method of output process substitution.

## Incorrect tangents 
NA

## References
NA
