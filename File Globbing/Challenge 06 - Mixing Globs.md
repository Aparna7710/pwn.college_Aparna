# File globbing 06 - Mixing globs
This challenge teaches us how to use multiple different globbing commands in one argument.

## My solve
**Flag:** `pwn.college{AUs7rWc95dE-sb_hVAi0ac0iNuU.QX1IDO0wSN2kjNzEzW}`

I entered the starting letter of the given three words withing the [] command and then used the * command to leave the rest of the word as a wildcard that can be filled by the compiler.
```bash
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{AUs7rWc95dE-sb_hVAi0ac0iNuU.QX1IDO0wSN2kjNzEzW}
```

## What I learned
This challenge taught me how to use different globbing commands together and how to observe for patterns for executing the same.

## Incorrect tangents 
NA

## References 
NA
