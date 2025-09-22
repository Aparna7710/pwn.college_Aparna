# Pondering Paths 03 - Position thy self
This task teachers us about the concept of current working directory of our process.

## My solve
**Flag:** `pwn.college{Yj7trf-oVPrK2J6OyDrhSSATr9O.QX2QTN0wSN2kjNzEzW}`

```bash
/challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
$ cd /etc/apt/sources.list.d
hacker@paths~position-thy-self:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Yj7trf-oVPrK2J6OyDrhSSATr9O.QX2QTN0wSN2kjNzEzW}
```

## What I learned
It taught me how to change the current directory using cd command.
