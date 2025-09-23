# Challenge Name
This challenge teaches us how to access the info about all the files that is stored in a specific directory.

## My solve
**Flag:** `pwn.college{AW-D1QE8DknqA3IAv_6f9YJFXAP.QX4IDO0wSN2kjNzEzW}`
I accessed the files under challenge, found the renamed run file and then accessed that.

```bash
$ ls /challenge
21385-renamed-run-22299  DESCRIPTION.md
$ /challenge/21385-renamed-run-22299
Yahaha, you found me! Here is your flag:
pwn.college{AW-D1QE8DknqA3IAv_6f9YJFXAP.QX4IDO0wSN2kjNzEzW}
```

## What I learned
This challenge taught me how to use the ls command to access all the files stored in a directory.
