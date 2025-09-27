# Challenge Name
This challenge teaches us what manuals are, their general layout and how to read and navigate through them to find useful information. 

## My solve
**Flag:** `pwn.college{Ar7AIJgOaZ1Rp8b9sWGZzS9cKtp.QX0EDO0wSN2kjNzEzW}`

Following the instructions in the command, I first used the man command to read challenge and from the manual I got the hint "--rgapbs NUM print the flag if NUM is 718" and so I passed the required arguments to get the flag.
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --rgapbs 718
Correct usage! Your flag: pwn.college{Ar7AIJgOaZ1Rp8b9sWGZzS9cKtp.QX0EDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use the man command. 

## Incorrect tangents 
I did incorrectly pass the argument once and tried to directly pass --rgapbs NUM.

## References
