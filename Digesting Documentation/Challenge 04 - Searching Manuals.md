# Digesting Documentation 04 - Searching Manuals
This challenge teaches us how to navigate and search through manuals.

## My solve
**Flag:** `pwn.college{EmSTASenkVzAtVFfJcxF77QZ3Xi.QX1EDO0wSN2kjNzEzW}`

As instructed in the question, I accesed the manual of challenge using man command after which I used / to search for the word flag and then found this argument in the manual "--im This argument will give you the flag!".
I then ran this argument and accessed the flag.

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --im
Initializing...
Correct usage! Your flag: pwn.college{EmSTASenkVzAtVFfJcxF77QZ3Xi.QX1EDO0wSN2kjNzEzW}
hacker@man~searching-manuals:~$
```

## What I learned 
This challenge taught me the various ways of searching through a manual.

## Incorrect tangents
NA

## References 
NA
