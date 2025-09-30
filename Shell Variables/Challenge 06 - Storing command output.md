# Shell variables 06 - Storing command output
This challenge teaches us how to store the output of commands.

## My solve
**Flag:** `pwn.college{4gRmKZPuqtl6XZIGiq-DGdZ9BXE.QX1cDN1wSN2kjNzEzW}`

Following the challenge instructions I stored the output of /challenge/run to the variable PWN and then accessed the variable through cat command.

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{4gRmKZPuqtl6XZIGiq-DGdZ9BXE.QX1cDN1wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to store the output of certain commands into variables for future reference.

## Incorrect tangents 
NA

## References
NA
