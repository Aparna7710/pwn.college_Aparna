# Pondering Paths 08 - Implicit Relative paths
This challenge helps us to get more familiarised with using the '.' operator to access directories.

## My solve
**Flag:** `pwn.college{cEnlV7bID1lzYCtk66ueMLGvD0R.QXxUTN0wSN2kjNzEzW}`

I followed the task instructions and first accessed the /challenge directory after which I used the '.' operator to access the /run directory.

```bash
$ cd /challenge
/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{cEnlV7bID1lzYCtk66ueMLGvD0R.QXxUTN0wSN2kjNzEzW}
```

## What I learned 
This task just helped me better understand the usage of '.' in accessing directories.

