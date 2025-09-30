# Pondering Paths 05 - Position Yet Elsewhere
This task just builds on the concept of position yourself and changing the current working directory.

## My solve
**Flag:** `pwn.college{cQOQYcbZiSmAKZOsk_iLA_0lfBE.QX4QTN0wSN2kjNzEzW}`

I followed the task instructions and typed /challenge/run after which i followed the instructions to access /var and thus found the correct path.

```bash
$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /var
hacker@paths~position-yet-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{cQOQYcbZiSmAKZOsk_iLA_0lfBE.QX4QTN0wSN2kjNzEzW}
```
