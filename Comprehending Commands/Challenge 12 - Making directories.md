# Comprehending Commands 12 - Making directories
This challenge aims to teach us how to make out own directories.

## My solve
**Flag:** `pwn.college{cdhSGpqsMQz--ecMbs7FnFWC44E.QXxMDO0wSN2kjNzEzW}`
I followed the challenge instructions and used the cd command to enter the tmp directory and then mkdir command to make my own pwn directory in it.

```bash
$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{cdhSGpqsMQz--ecMbs7FnFWC44E.QXxMDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use the mkdir command.
