# Practicing piping 11 - Process substitution for input
This challenge aims to teach us how to use the <(command) operator to help in process substitution.

## My solve
**Flag:** ` pwn.college{s9ef3ugnJOYaRy41jskoo_t5NI0.0lNwMDOxwSN2kjNzEzW}`

Following the challenge instructions I used the diff command on the output of two different files using <(command) operator.

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
89a90
> pwn.college{s9ef3ugnJOYaRy41jskoo_t5NI0.0lNwMDOxwSN2kjNzEzW}
```

## What I learned
This challenge taught me how to use the <(command) operator to convert outputs of commands to files so as to use them in file related commands.

## Incorrect tangents 
NA

## References
NA
