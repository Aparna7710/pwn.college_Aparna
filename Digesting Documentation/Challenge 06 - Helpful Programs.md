# Digesting Documentation 06 - Helpful Programs
This challenge teaches us about the concept of --help command and its uses. 

## My solve
**Flag:** `pwn.college{w4A5SmfLU9NUrI-EEEvLhWLA0r1.QX3IDO0wSN2kjNzEzW}`

So just like the previous challenges, I first accessed the /challenge/challenge directory and here i ran the argument --help to it. After which i got two hints, one to get the correct value to get the flag and the other, the command to get the flag itself. 
So, I followed both the arguments and executed the code. 

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 459
hacker@man~helpful-programs:~$ /challenge/challenge -g 459
Correct usage! Your flag: pwn.college{w4A5SmfLU9NUrI-EEEvLhWLA0r1.QX3IDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me the various forms of --help command and how to use it when manuscript might not be given.

## Incorrect tangents
NA

## References 
NA
