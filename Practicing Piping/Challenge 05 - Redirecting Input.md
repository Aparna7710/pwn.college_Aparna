# Practicing Piping 05 - Redirecting Input
This challenge teaches us how to redirect input.


## My solve
**Flag:** `pwn.college{cW6fvWbSgZFSoXqy9ydggwn63DO.QXwcTN0wSN2kjNzEzW}`

Following the challenge instructions I used > to redirect output of PWN to COLLGE and used < to redirect input of /challenge/run to PWN


```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{cW6fvWbSgZFSoXqy9ydggwn63DO.QXwcTN0wSN2kjNzEzW}
```

## What I learned
This challenge taught me how to use the < operator to redirect inputs.

## Incorrect tangents 
NA

## References
NA
