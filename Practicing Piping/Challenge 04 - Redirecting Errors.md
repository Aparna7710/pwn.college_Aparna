# Practicing Piping 04 - Redirecting errors
This challenge aims us to teach the concept of file directors and also how to use multiple file directors in the same command.

## My solve
**Flag:** `pwn.college{E9t5n7IwR-HSavx8dBHbNiLwEPi.QX3YTN0wSN2kjNzEzW}`

Following the challenge instructions, I redirected /challenge/run to myflag and the errors to instructions, after which I used cat to access the flag.

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{E9t5n7IwR-HSavx8dBHbNiLwEPi.QX3YTN0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me the concept of file directors and the proper syntax to use multiple of them in the same command.

## Incorrect tangents 
NA

## References
NA
