# Comprehending paths 05 - Comparing files
This challenge teaches us about diff command.

## My solve
**Flag:** `pwn.college{QVvkM36SfD3s2-EnuJG8zGtTA5Z.01MwMDOxwSN2kjNzEzW}`

Followed the instructions in the question and used diff command to compare two files stored at the directories given in the question.
```bash
diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
54a55
> pwn.college{QVvkM36SfD3s2-EnuJG8zGtTA5Z.01MwMDOxwSN2kjNzEzW}
```

## What I learned
This challenge taught me the syntax of diff command and how to use it to compare the information stored in two files.
