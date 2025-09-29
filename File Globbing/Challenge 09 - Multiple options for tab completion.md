# File Globbing 09 - Multiple options for tab completion
This challenge teaches us how to use tab completion more properly when there are multiple possible files starting with the same letter.

## My solve
**Flag:** `pwn.college{IIpiHThSnzhhcLOyua7A57Aefyh.0lN0EzNxwSN2kjNzEzW}`

I started by using the cat command on /challenge/files/p and from there on I repeatedly used tab to get the correct file.

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{IIpiHThSnzhhcLOyua7A57Aefyh.0lN0EzNxwSN2kjNzEzW}
```

## What I learned
This challenge taught me how to use the tab command in more specific scenarios.

## Incorrect tangents 
NA

## References 
NA
