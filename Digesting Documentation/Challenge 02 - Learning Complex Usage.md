# Digesting Documentation 01 - Learning Complex Usage
This challenge teaches us the concept of arguments that take arguments.

## My solve
**Flag:** `pwn.college{UZdD0ewL3jQSrPx1K49oiAUx0BE.QX1ITO0wSN2kjNzEzW}`

First I accessed the /challenge directory and used the ls -la command to see all the files. Knowing that the flag file was not stored in there, I then accessed the / directory to get the path to the flag and then passed the arguments as instructed in the challenge.
```bash
cd /challenge
hacker@man~learning-complex-usage:/challenge$ ls -la
total 20
drwxr-xr-x 1 root root 4096 Sep 27 12:02 .
drwxr-xr-x 1 root root 4096 Sep 27 12:03 ..
-rwsr-xr-x 1 root root   74 Jan 14  2025 .init
-rwsr-xr-x 1 root root 1115 Sep  1 05:06 DESCRIPTION.md
-rws--x--x 1 root root  475 Jan 14  2025 challenge
hacker@man~learning-complex-usage:/challenge$ cd /
hacker@man~learning-complex-usage:/$ ls -la
total 72
drwxr-xr-x    1 root root 4096 Sep 27 12:03 .
drwxr-xr-x    1 root root 4096 Sep 27 12:03 ..
-rwxr-xr-x    1 root root    0 Sep 27 12:02 .dockerenv
lrwxrwxrwx    1 root root    7 Apr  4 02:03 bin -> usr/bin
drwxr-xr-x    2 root root 4096 Apr 15  2020 boot
drwxr-xr-x    1 root root 4096 Sep 27 12:02 challenge
drwxr-xr-x    6 root root  380 Sep 27 12:02 dev
drwxr-xr-x    1 root root 4096 Sep 27 12:02 etc
-r--------    1 root root   60 Sep 27 12:02 flag
drwxr-xr-x    1 root root 4096 Sep 26 17:24 home
lrwxrwxrwx    1 root root    7 Apr  4 02:03 lib -> usr/lib
lrwxrwxrwx    1 root root    9 Apr  4 02:03 lib32 -> usr/lib32
lrwxrwxrwx    1 root root    9 Apr  4 02:03 lib64 -> usr/lib64
lrwxrwxrwx    1 root root   10 Apr  4 02:03 libx32 -> usr/libx32
drwxr-xr-x    2 root root 4096 Apr  4 02:03 media
drwxr-xr-x    2 root root 4096 Apr  4 02:03 mnt
drwxr-xr-x    1 root root   16 Oct 26  2024 nix
drwxr-xr-x    1 root root 4096 Sep 26 17:24 opt
dr-xr-xr-x 2639 root root    0 Sep 27 12:02 proc
drwx------    1 root root 4096 Sep 26 17:24 root
drwxr-xr-x    1 root root 4096 Sep 27 12:02 run
lrwxrwxrwx    1 root root    8 Apr  4 02:03 sbin -> usr/sbin
drwxr-xr-x    2 root root 4096 Apr  4 02:03 srv
dr-xr-xr-x   13 root root    0 Aug 27 03:13 sys
drwxrwxrwt    1 root root 4096 Sep 27 12:02 tmp
drwxr-xr-x    1 root root 4096 Sep 26 17:09 usr
drwxr-xr-x    1 root root 4096 Sep 26 17:08 var
hacker@man~learning-complex-usage:/$ cd
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{UZdD0ewL3jQSrPx1K49oiAUx0BE.QX1ITO0wSN2kjNzEzW}
```

## What I learned
This challenge taught me how to pass arguments to certain arguments.

## Incorrect tangents
NA

## References 
NA
