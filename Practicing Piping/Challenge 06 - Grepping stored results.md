# Practicing Piping 06 - Grepping stored results
This challenge teaches us how to use grep command to search through the stored output.


## My solve
**Flag:** `pwn.college{k4aPXJA7hkPwtTMN_T8gSH2T8kT.QX4EDO0wSN2kjNzEzW}`

Following the challenge instructions, I first redirected the output and then used the grep command to search through the output. I searched for pwn since all flags begin with it.


```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "pwn" /tmp/data.txt
pwning
pwn.college{k4aPXJA7hkPwtTMN_T8gSH2T8kT.QX4EDO0wSN2kjNzEzW}
pwns
pwn
pwned
```

## What I learned 
This challenge taught me how to search through huge outputs

## Incorrect tangents 
NA

## References
NA
