# Pondering Paths 09 - Home Sweet Home
This task teaches us how ~ serves as a shorthand for the representation of the absolute path to our home directory.

## My solve
**Flag:** `pwn.college{QRFqASo23zT17ZmSzDao32bdgO7.QXzMDO0wSN2kjNzEzW}`

So I first ran the /challenge/run command and as an argument I specified the path to a file f in the home directory.

```bash
$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{QRFqASo23zT17ZmSzDao32bdgO7.QXzMDO0wSN2kjNzEzW}
```

## What I learned 
I learnt how to use the shorthand of ~ when writing paths that lead to home directory.

## Incorrect tangents 
Initially, I did misunderstand a bit and tried writing the full path instead of the shorthand version. 
