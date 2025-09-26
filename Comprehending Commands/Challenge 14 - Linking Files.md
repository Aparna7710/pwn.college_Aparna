# Comprehending Commands 14 - Linking files
This challenge aims to teach us the method and use of linking files and teacher us about both hard linking and soft linking.

## My solve
**Flag:** `pwn.college{Q9AkUEAK4_yJbGXY4cJyR6Wnb3p.QX5ETN1wSN2kjNzEzW}`
From reading the question I understood that I had to use symbolic links to change the file that the directory was reading to the right file and so I executed the commands to carry out the same.
```bash
ln -s /flag //home/hacker/not-the-flag
~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Q9AkUEAK4_yJbGXY4cJyR6Wnb3p.QX5ETN1wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to do symbolic or soft linking using the ln -s command.
