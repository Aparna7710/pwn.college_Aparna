# Digesting Documentation 01 - Learning from Documentation
This challenge aims to teach us how to correctly use commands like cd and how to pass arguments.

## My solve
**Flag:** `pwn.college{I6e2q7nfUjjYs4QIcYygFZM7FfB.QX0ITO0wSN2kjNzEzW}`
Followed the commands and first accessed the /challenge directory after which I passed the required argument to a subfile of the directory.

```bash
hacker@man~learning-from-documentation:~$ cd /challenge
hacker@man~learning-from-documentation:/challenge$ ls -la
total 20
drwxr-xr-x 1 root root 4096 Sep 27 11:52 .
drwxr-xr-x 1 root root 4096 Sep 27 11:54 ..
-rwsr-xr-x 1 root root   74 Jan 14  2025 .init
-rwsr-xr-x 1 root root 1317 Sep  1 05:06 DESCRIPTION.md
-rws--x--x 1 root root  377 Jan 14  2025 challenge
hacker@man~learning-from-documentation:/challenge$ cd challenge/challenge
bash: cd: challenge/challenge: Not a directory
hacker@man~learning-from-documentation:/challenge$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{I6e2q7nfUjjYs4QIcYygFZM7FfB.QX0ITO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to pass arguments to a directory.

## Incorrect tangents 
NA

## References
NA
## References (optional)
Add any references or videos you may have used while solving the challenge. If you looked up anything or watched any videos to help in solving, this section should be included.
