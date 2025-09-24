# Comprehending Commands 10 - Hidden Files
This challenge aims to teach us how to find the list of all files in a directory which will not typically show with a simple ls command.

## My solve
**Flag:** `pwn.college{sQfxkG17ecVpATgtXc8JDYZEXw5.QXwUDO0wSN2kjNzEzW}`

Followed the commands and used -a command with ls to access all the files under / and found the file containing flag. I then used cat command to get the flag.
```bash
$ ls /
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
$ ls -a /
.                   bin        etc    lib64   nix   run   tmp
..                  boot       home   libx32  opt   sbin  usr
.dockerenv          challenge  lib    media   proc  srv   var
.flag-872818017826  dev        lib32  mnt     root  sys
$ cat /.flag-872818017826
pwn.college{sQfxkG17ecVpATgtXc8JDYZEXw5.QXwUDO0wSN2kjNzEzW}
```

## What I learned 
This challenge taught me how to access all files stored in a given directory by using -a command with ls.
