# Practing Piping 13 - Split piping stderr and stdout
This challenge teaches us how to combine all the different piping arguments.

## My solve
**Flag:** `pwn.college{4tHw51jxeHqwnmDpL7mqnO5xTzo.QXxQDM2wSN2kjNzEzW}`

Following the challenge instructions, I basically ran the /challenge/hack directory and then I ran the output of this directory to /challenge/planet and the errors of this directory to /challenge/the.

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{4tHw51jxeHqwnmDpL7mqnO5xTzo.QXxQDM2wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to combine multiple piping commands to obtain the required result.

## Incorrect tangents 
It did take a bit of trial before nailing the exact format in which all the commands had to be laid out.

## References
NA
