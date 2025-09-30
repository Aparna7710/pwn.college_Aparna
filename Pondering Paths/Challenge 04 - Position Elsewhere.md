# Pondering Paths 04 - Position Elsewhere
This task gives a more advanced idea about modifying your current working directory by accessing subprograms/sublevels of the main path.

## My solve
**Flag:** `pwn.college{gEG4xSH9ZR5H9DENShtqrM4G9KG.QX3QTN0wSN2kjNzEzW}`
I just followed the task instructions and typed /challenge/run after which i was given the correct directory to access.

```bash
$ /challenge/run
Incorrect...
You are not currently in the /proc/154/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /proc/154/fd
hacker@paths~position-elsewhere:/proc/154/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gEG4xSH9ZR5H9DENShtqrM4G9KG.QX3QTN0wSN2kjNzEzW}
```


