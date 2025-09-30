# Practicing Piping 10 - Duplication piped data with tee
This challenge teaches us how to see the data that we pipe.

## My solve
**Flag:** `pwn.college{Yxs1OZIWIKDe1ZNojAcedLNU9k1.QXxITO0wSN2kjNzEzW}`

Following the challenge instructions, I used the tee command along with | to see the commands as I piped them and then obtained the secret key and hence the flag.

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ touch file
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn |tee file |  /challenge/college
Processing...
WARNING: you are overwriting file file with tee's output...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat file
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "Yxs1OZIW"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret  Yxs1OZIW | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{Yxs1OZIWIKDe1ZNojAcedLNU9k1.QXxITO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to properly use to see the tee command to see the commands being piped.

## Incorrect tangents 
I initially did not realise that an additional file had to be created to store the commands obtained through tee and so on second trial I created the additional file and executed the commands.

## References
NA
