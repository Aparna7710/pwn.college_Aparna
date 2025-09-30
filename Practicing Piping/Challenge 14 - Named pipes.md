# Practicing Piping 14 - Named pipes
This challenge teaches us how to create persistent named pipes.

## My solve
**Flag:** `pwn.college{UvK9ZRAG0NWo6D3KJi6qUo-xhDK.01MzMDOxwSN2kjNzEzW}`

Following the command instructions, I created a FIFO pipe using mkfifo command and then I redirected the output of /challenge/run to it.

```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!

hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{UvK9ZRAG0NWo6D3KJi6qUo-xhDK.01MzMDOxwSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to make and use a persistent pipe using mkfifo command and the syntax related to same.

## Incorrect tangents 
Every time I ran the first command, my terminal seemed to lock up and I couldn’t type additional commands. Hitting Ctrl+C returned the prompt, but it also interrupted the process. Searching around I learned that using two terminals solves this — so I ran the writer in the pwn terminal and the reader in my system’s Ubuntu terminal, which worked.

## References
NA
