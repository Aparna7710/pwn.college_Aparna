# Shell Variables 04 - Exporting variables
This challenge teaches us how to export variables such that they are accessible outside their shell.

## My solve
**Flag:** `pwn.college{8QLDVPK8SOoR7_ZwVKvAlSlI85y.QXyYTN0wSN2kjNzEzW}`

Following the command instructions, I set PWN to COLLEGE and COLLEGE to PWN but I only exported PWN to /challenge/run using export command and then accessed PWN through it.

```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ sh
sh-5.2$ /challenge/run $PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{8QLDVPK8SOoR7_ZwVKvAlSlI85y.QXyYTN0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use the export and sh command to export variables to other shells.

## Incorrect tangents 
NA

## References
NA
