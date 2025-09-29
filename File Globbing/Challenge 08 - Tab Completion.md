# File Globbing 08 - Tab completion
This challenge teaches us how to use the tab button to autocomplete the directory.

## My solve
**Flag:** `pwn.college{EhR73ngk_CLchR2fdGbBxcRDz9_.0FN0EzNxwSN2kjNzEzW}`

Following the question instructions I used cat to enter into the /challenge/pwncollege file but used tab to finish the later part of the path.

```bash
hacker@globbing~tab-completion:~$ cd /challenge
hacker@globbing~tab-completion:/challenge$ ls
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:/challenge$ cat /challenge/pwncollege​
pwn.college{EhR73ngk_CLchR2fdGbBxcRDz9_.0FN0EzNxwSN2kjNzEzW}
```

## What I learned 
This challenge taught me how and where to properly use the tab key to complete the required path.

## Incorrect tangents 
NA

## References 
NA
