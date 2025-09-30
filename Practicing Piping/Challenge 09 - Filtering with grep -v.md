# Practicing Piping 09 - Filtering with grep -v
This challenge teaches us how to filter the wrong outputs when using grep.

## My solve
**Flag:** `pwn.college{YouqOarc4FvQg1IjpQSuuffqNXL.0FOxEzNxwSN2kjNzEzW}`

Following the challenge instructions, I redirected the output of /challenge/run and through | operator I used grep command with the add on of -v operator to remove all the decoy flags.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{YouqOarc4FvQg1IjpQSuuffqNXL.0FOxEzNxwSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to use the -v operator with the grep command to filter out all the wrong outputs

## Incorrect tangents 
NA

## References
NA
