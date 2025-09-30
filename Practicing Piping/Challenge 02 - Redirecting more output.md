# Practicing piping 02 - Redirecting more outputs
This challenge teaches us how redirection of outputs can be applied to different commands.

## My solve
**Flag:** `pwn.college{IHJ5p9LzURlN811k_EaD0rtJQSX.QX1YTN0wSN2kjNzEzW}`

Following the challenge instructions I used the > operator to redirect /challenge/run to myflag.

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IHJ5p9LzURlN811k_EaD0rtJQSX.QX1YTN0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use > on different commands other than echo alone.

## Incorrect tangents 
NA

## References 
NA
