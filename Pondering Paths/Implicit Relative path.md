# Pondering Paths 06 - Implicit relative paths, from /
This challenege helps us to learn about the concept of accesing relative paths

## My solve
**Flag:** `pwn.college{kZb5vRt_YeQek1b6yuC2iyogBwo.QX5QTN0wSN2kjNzEzW}`

Following the challenge, I started running /challenge/run and from there followed the hints to access the relative path

```bash
$ cd /challenge/run
bash: cd: /challenge/run: Not a directory
~$ cd
~$ pwd
/home/hacker
~$ cd /challenge/run
bash: cd: /challenge/run: Not a directory
~$ cd /
/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{kZb5vRt_YeQek1b6yuC2iyogBwo.QX5QTN0wSN2kjNzEzW}
```

## What I learned
This task taught me the difference between absolute and relative paths and also the different syntaxes for accessing each of them.

## Incorrect tangents 
As seen from the code, I initially did not understand the exact concept of relative path and its syntax and thus it took me a bit of trial before
understanding what exactly needed to be done.

