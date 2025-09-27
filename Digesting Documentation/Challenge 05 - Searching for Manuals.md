# Digesting Documentation 05 - Searching for manuals.
This challenge teaches us how to search for the right manual.

## My solve
**Flag:** `pwn.college{QhxJtH0zY3CwCOPuS-tgNLJZ9Cy.QX2EDO0wSN2kjNzEzW}`
So, I followed the challenge instructions and firstly accessed the man man manual and from there I got this hint "man -K [man options] [section] term ...". 
Using this hint I ran the command "man -K /challenge/challenge" and read the next manual from where i got the hint "--hxtzwu NUM print the flag if NUM is 039" and then used this argument to get the flag.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -K /challenge/challenge
hacker@man~searching-for-manuals:~$ /challenge/challenge --hxtzwu 039
Correct usage! Your flag: pwn.college{QhxJtH0zY3CwCOPuS-tgNLJZ9Cy.QX2EDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to search for the right manual.

## Incorrect tangents 
NA

## References 
NA
