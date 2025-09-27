# File Globbing 07 - Exclusionary Globbing
This challenge teaches us how to apply conditions/exclusions to globbing commands.

## My solve
**Flag:** `pwn.college{gSkY0gVbc_h4rw-587EdZTdkgRy.QX2IDO0wSN2kjNzEzW}`

Followed the challenge instructions and used the ! command in [] to exclude p,w,n.

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files.
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{gSkY0gVbc_h4rw-587EdZTdkgRy.QX2IDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to apply exclusionary conditions to globbing commands.

## Incorrect tangents 
NA

## References 
NA
