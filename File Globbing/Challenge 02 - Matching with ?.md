# File Globbing 02 - Matching with ?
This challenge teaches us the usage of ? character which is treated as a single wildcard character.

## My solve
**Flag:** `pwn.college{UPK7G94L7isRg3Zoxh1ti5opdqW.QXyIDO0wSN2kjNzEzW}`

Following the challenge instructions I replaced all c and h in the /challenge directory with ? to access it using cd.

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{UPK7G94L7isRg3Zoxh1ti5opdqW.QXyIDO0wSN2kjNzEzW}
hacker@globbing~matching-with-:/challenge$
```

## What I learned 
This challenge taught me the use of the ? command.

## Incorrect tangents
NA

## References 
NA
