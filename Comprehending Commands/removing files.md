# Comprehending Commands 08 - Removing files
This challenge teaches us how to delete files.

## My solve
**Flag:** `pwn.college{0OwhO1oTy5cKHOXthIhLyQZmLHl.QX2kDM1wSN2kjNzEzW}`
Followed the instructions as is and created a file which I then deleted and then ran the /challenge/check command to access the file.
```bash
touch delete_me
$ rm delete_me
$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{0OwhO1oTy5cKHOXthIhLyQZmLHl.QX2kDM1wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use the rm command to delete files.
