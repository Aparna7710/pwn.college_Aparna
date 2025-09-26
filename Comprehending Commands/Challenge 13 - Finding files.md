# Comprehending commands 13 - Finding files
This challenge aims to teach us how to find files in a directory by mentioning name or other specific criteria

## My solve
**Flag:** `pwn.college{8jzgLeFe9ip-IS5pY3J2GZQRlmj.QXyMDO0wSN2kjNzEzW}`
So I first accessed the / directory after which I used the find command to find the file flag and got two directories and then followed those two.
```bash
cd /
hacker@commands~finding-files:/$ find -name flag
find: ‘./root’: Permission denied
find: ‘./etc/ssl/private’: Permission denied
find: ‘./tmp/tmp.4mK6TfTSUV’: Permission denied
./usr/local/lib/python3.8/dist-packages/pwnlib/flag
./usr/lib/python3/dist-packages/numpy/polynomial/flag
^C
hacker@commands~finding-files:/$ find ./usr/local/lib/python3.8/dist-packages/pwnlib/flag
./usr/local/lib/python3.8/dist-packages/pwnlib/flag
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/__pycache__
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/__pycache__/__init__.cpython-38.pyc
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/__pycache__/flag.cpython-38.pyc
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/__init__.py
hacker@commands~finding-files:/$ find ./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
hacker@commands~finding-files:/$ cd ./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
bash: cd: ./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py: Not a directory
hacker@commands~finding-files:/$ find ./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
./usr/local/lib/python3.8/dist-packages/pwnlib/flag/flag.py
hacker@commands~finding-files:/$ ^C
hacker@commands~finding-files:/$ find ./usr/lib/python3/dist-packages/numpy/polynomial/flag
./usr/lib/python3/dist-packages/numpy/polynomial/flag
hacker@commands~finding-files:/$ cat ./usr/lib/python3/dist-packages/numpy/polynomial/flag
pwn.college{8jzgLeFe9ip-IS5pY3J2GZQRlmj.QXyMDO0wSN2kjNzEzW}
```

## What I learned 
This challenge helped me the learn the use of the find command and taught me how to use it with specific parameters according to the different scenarios.
