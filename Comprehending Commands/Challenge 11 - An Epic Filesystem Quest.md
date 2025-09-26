# Comprehending Paths 11 - An Epic Filesystem Quest
This challenge aims to get us more used to using ls la and cd commands to access various directories and clues

## My solve
**Flag:** `pwn.college{ER_nVdNIR02DmavYkTsnPDYddiF.QX5IDO0wSN2kjNzEzW}`
I first used cd command to access the / directory after which I found the first hint in BLUEPRINT and from there on I went on accessing the other hints using cd ls -la and cat.


```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -la
total 80
drwxr-xr-x    1 root root 4096 Sep 26 17:11 .
drwxr-xr-x    1 root root 4096 Sep 26 17:11 ..
-rwxr-xr-x    1 root root    0 Sep 26 16:58 .dockerenv
-rw-r--r--    1 root root  229 Sep 26 16:58 BLUEPRINT
lrwxrwxrwx    1 root root    7 Apr  4 02:03 bin -> usr/bin
drwxr-xr-x    2 root root 4096 Apr 15  2020 boot
drwxr-xr-x    1 root root 4096 Sep 26 16:58 challenge
drwxr-xr-x    6 root root  380 Sep 26 16:58 dev
drwxr-xr-x    1 root root 4096 Sep 26 16:58 etc
-r--------    1 root root   60 Sep 26 16:58 flag
drwxr-xr-x    1 root root 4096 Sep  7 01:38 home
lrwxrwxrwx    1 root root    7 Apr  4 02:03 lib -> usr/lib
lrwxrwxrwx    1 root root    9 Apr  4 02:03 lib32 -> usr/lib32
lrwxrwxrwx    1 root root    9 Apr  4 02:03 lib64 -> usr/lib64
lrwxrwxrwx    1 root root   10 Apr  4 02:03 libx32 -> usr/libx32
drwxr-xr-x    2 root root 4096 Apr  4 02:03 media
drwxr-xr-x    2 root root 4096 Apr  4 02:03 mnt
drwxr-xr-x    1 root root   16 Oct 26  2024 nix
drwxr-xr-x    1 root root 4096 Sep  7 01:38 opt
dr-xr-xr-x 3702 root root    0 Sep 26 16:58 proc
drwx------    1 root root 4096 Sep  7 01:38 root
drwxr-xr-x    1 root root 4096 Sep 26 16:58 run
lrwxrwxrwx    1 root root    8 Apr  4 02:03 sbin -> usr/sbin
drwxr-xr-x    2 root root 4096 Apr  4 02:03 srv
dr-xr-xr-x   13 root root    0 Aug 27 03:13 sys
drwxrwxrwt    1 root root 4096 Sep 26 16:58 tmp
drwxr-xr-x    1 root root 4096 Sep  7 01:22 usr
drwxr-xr-x    1 root root 4096 Sep  7 01:22 var
hacker@commands~an-epic-filesystem-quest:/$ cat BLUEPRINT
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/xfrm

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls -la /opt/linux/linux-5.4/include/config/xfrm
total 16
drwxr-xr-x 1 root   root   4096 Sep 26 16:58 .
drwxr-xr-x 1 root   root   4096 Sep  7 01:25 ..
-rw-r--r-- 1 hacker hacker  251 Sep 26 16:58 POINTER-TRAPPED
-rw-r--r-- 1 root   root      0 Sep  7 01:25 algo.h
-rw-r--r-- 1 root   root      0 Sep  7 01:25 user.h
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/config/xfrm
cat: /opt/linux/linux-5.4/include/config/xfrm: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/config/xfrm/POINTER-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/sage/schemes/elliptic_curves

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ ls -la /usr/lib/python3/dist-packages/sage/schemes/elliptic_curves
total 2768
drwxr-xr-x 1 root root   4096 Sep 26 16:58 .
drwxr-xr-x 1 root root   4096 Sep  7 01:23 ..
-rw-r--r-- 1 root root    255 Sep 26 16:58 .BRIEF
-rw-r--r-- 1 root root  35548 Jan  1  2020 BSD.py
-rw-r--r-- 1 root root      0 Jan  1  2020 __init__.py
drwxr-xr-x 2 root root   4096 Sep  7 01:23 __pycache__
-rw-r--r-- 1 root root   1630 Jan  1  2020 all.py
-rw-r--r-- 1 root root  19580 Jan  1  2020 cardinality.py
-rw-r--r-- 1 root root  30342 Feb  8  2020 cm.py
-rw-r--r-- 1 root root  54799 Jan  1  2020 constructor.py
-rw-r--r-- 1 root root 187992 Feb  8  2020 descent_two_isogeny.cpython-38-x86_64-linux-gnu.so
-rw-r--r-- 1 root root  45165 Jan  1  2020 descent_two_isogeny.pyx
-rw-r--r-- 1 root root   6514 Jan  1  2020 ec_database.py
-rw-r--r-- 1 root root 151879 Jan  1  2020 ell_curve_isogeny.py
-rw-r--r-- 1 root root  15086 Jan  1  2020 ell_egros.py
-rw-r--r-- 1 root root  53152 Jan  1  2020 ell_field.py
-rw-r--r-- 1 root root  63011 Jan  1  2020 ell_finite_field.py
-rw-r--r-- 1 root root 104544 Jan  1  2020 ell_generic.py
-rw-r--r-- 1 root root  46329 Jan  1  2020 ell_local_data.py
-rw-r--r-- 1 root root  28114 Jan  1  2020 ell_modular_symbols.py
-rw-r--r-- 1 root root 159019 Jan  1  2020 ell_number_field.py
-rw-r--r-- 1 root root   3047 Jan  1  2020 ell_padic_field.py
-rw-r--r-- 1 root root 122907 Feb  8  2020 ell_point.py
-rw-r--r-- 1 root root 259593 Jan  1  2020 ell_rational_field.py
-rw-r--r-- 1 root root  24271 Jan  1  2020 ell_tate_curve.py
-rw-r--r-- 1 root root  14089 Jan  1  2020 ell_torsion.py
-rw-r--r-- 1 root root  11940 Jan  1  2020 ell_wp.py
-rw-r--r-- 1 root root  23930 Jan  1  2020 formal_group.py
-rw-r--r-- 1 root root  57888 Jan  1  2020 gal_reps.py
-rw-r--r-- 1 root root  55734 Jan  1  2020 gal_reps_number_field.py
-rw-r--r-- 1 root root   5497 Jan  1  2020 gp_simon.py
-rw-r--r-- 1 root root 254142 Jan  1  2020 heegner.py
-rw-r--r-- 1 root root  69424 Jan  1  2020 height.py
-rw-r--r-- 1 root root  57925 Jan  1  2020 isogeny_class.py
-rw-r--r-- 1 root root 132596 Jan  1  2020 isogeny_small_degree.py
-rw-r--r-- 1 root root   8352 Jan  1  2020 jacobian.py
-rw-r--r-- 1 root root  11181 Jan  1  2020 kodaira_symbol.py
-rw-r--r-- 1 root root  34615 Jan  1  2020 kraus.py
-rw-r--r-- 1 root root  33184 Jan  1  2020 lseries_ell.py
-rw-r--r-- 1 root root   6176 Jan  1  2020 mod5family.py
-rw-r--r-- 1 root root  11209 Jan  1  2020 modular_parametrization.py
-rw-r--r-- 1 root root  63478 Jan  1  2020 padic_lseries.py
-rw-r--r-- 1 root root  63390 Jan  1  2020 padics.py
-rw-r--r-- 1 root root  72296 Jan  1  2020 period_lattice.py
-rw-r--r-- 1 root root 207488 Feb  8  2020 period_lattice_region.cpython-38-x86_64-linux-gnu.so
-rw-r--r-- 1 root root  25367 Jan  1  2020 period_lattice_region.pyx
-rw-r--r-- 1 root root  18963 Jan  1  2020 saturation.py
-rw-r--r-- 1 root root  42874 Jan  1  2020 sha_tate.py
-rw-r--r-- 1 root root  21902 Jan  1  2020 weierstrass_morphism.py
-rw-r--r-- 1 root root   7619 Jan  1  2020 weierstrass_transform.py
hacker@commands~an-epic-filesystem-quest:/$ ls -la /usr/lib/python3/dist-packages/sage/schemes/elliptic_curves/.BRIEF
-rw-r--r-- 1 root root 255 Sep 26 16:58 /usr/lib/python3/dist-packages/sage/schemes/elliptic_curves/.BRIEF
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/lib/python3/dist-packages/sage/schemes/elliptic_curves/.BRIEF
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2/six

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls -la /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2/six
total 24
drwxr-xr-x 1 root   root   4096 Sep 26 16:58 .
drwxr-xr-x 1 root   root   4096 Sep  7 01:23 ..
-rw-r--r-- 1 hacker hacker   80 Sep 26 16:58 TEASER-TRAPPED
-rw-r--r-- 1 root   root   3722 Dec 20  2019 __init__.pyi
drwxr-xr-x 3 root   root   4096 Sep  7 01:23 moves
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2/six/TEASER-TRAPPED
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/m68k/hp300
hacker@commands~an-epic-filesystem-quest:/$ ls -la /opt/linux/linux-5.4/arch/m68k/hp300
total 52
drwxrwxr-x 1 root root 4096 Sep 26 16:58 .
drwxrwxr-x 1 root root 4096 Nov 25  2019 ..
-rw-rw-r-- 1 root root  134 Nov 25  2019 Makefile
-rw-rw-r-- 1 root root  501 Nov 25  2019 README.hp300
-rw-r--r-- 1 root root  121 Sep 26 16:58 TRACE
-rw-rw-r-- 1 root root 6744 Nov 25  2019 config.c
-rw-rw-r-- 1 root root 5563 Nov 25  2019 hp300map.map
-rw-rw-r-- 1 root root  513 Nov 25  2019 reboot.S
-rw-rw-r-- 1 root root 2753 Nov 25  2019 time.c
-rw-rw-r-- 1 root root   52 Nov 25  2019 time.h
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/m68k/hp300/README.hp300
HP300 notes
-----------

The Linux/HP web page is at <http://www.tazenda.demon.co.uk/phil/linux-hp/>

Currently only 9000/340 machines have been tested.  Any amount of RAM should
work now but I've only tried 16MB and 12MB.

The serial console is probably broken at the moment but the Topcat/HIL keyboard
combination seems to work for me.  Your mileage may vary.

The LANCE driver works after a fashion but only if you reset the chip before
every packet.  This doesn't make for very speedy operation.

hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/m68k/hp300/TRACE
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/series/benchmarks
hacker@commands~an-epic-filesystem-quest:/$ ls -la /usr/local/lib/python3.8/dist-packages/sympy/series/benchmarks
total 28
drwxr-sr-x 1 root staff 4096 Sep 26 16:58 .
drwxr-sr-x 1 root staff 4096 Sep  7 01:37 ..
-rw-r--r-- 1 root staff  188 Sep 26 16:58 DOSSIER
-rw-r--r-- 1 root staff    0 Sep  7 01:37 __init__.py
drwxr-sr-x 2 root staff 4096 Sep  7 01:37 __pycache__
-rw-r--r-- 1 root staff  173 Sep  7 01:37 bench_limit.py
-rw-r--r-- 1 root staff  207 Sep  7 01:37 bench_order.py
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/sympy/series/benchmarks/DOSSIER
Congratulations, you found the clue!
The next clue is in: /usr/share/cmake-3.16/Help

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/cmake-3.16/Help
hacker@commands~an-epic-filesystem-quest:/usr/share/cmake-3.16/Help$ ls -la /usr/share/cmake-3.16/Help
total 144
drwxr-xr-x 1 root   root    4096 Sep 26 16:58 .
drwxr-xr-x 1 root   root    4096 Sep  7 01:21 ..
-rw-r--r-- 1 hacker hacker   208 Sep 26 16:58 EVIDENCE
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 command
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 cpack_gen
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 envvar
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 generator
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 include
-rw-r--r-- 1 root   root    1177 Jan 21  2020 index.rst
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 manual
drwxr-xr-x 2 root   root   12288 Sep  7 01:21 module
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 policy
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_cache
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_dir
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_gbl
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_inst
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_sf
drwxr-xr-x 2 root   root    4096 Sep  7 01:21 prop_test
drwxr-xr-x 2 root   root   20480 Sep  7 01:21 prop_tgt
drwxr-xr-x 3 root   root    4096 Sep  7 01:21 release
drwxr-xr-x 2 root   root   36864 Sep  7 01:21 variable
hacker@commands~an-epic-filesystem-quest:/usr/share/cmake-3.16/Help$ cat /EVIDENCE
cat: /EVIDENCE: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/cmake-3.16/Help$ cat /usr/share/cmake-3.16/Help/EVIDENCE
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/sh/include/mach-sh03

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/cmake-3.16/Help$ cd /opt/linux/linux-5.4/arch/sh/include/mach-sh03
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/include/mach-sh03$ ls -la
total 20
drwxrwxr-x 1 root   root   4096 Sep 26 16:58 .
drwxrwxr-x 1 root   root   4096 Nov 25  2019 ..
-rw-r--r-- 1 hacker hacker  232 Sep 26 16:58 ALERT
drwxrwxr-x 2 root   root   4096 Nov 25  2019 mach
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/include/mach-sh03$ cat //opt/linux/linux-5.4/arch/sh/include/mach-sh03/ALERT
Congratulations, you found the clue!
The next clue is in: /usr/lib/ruby/2.7.0/net/http

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/include/mach-sh03$ ls -la /usr/lib/ruby/2.7.0/net/http
total 92
drwxr-xr-x 1 root root  4096 Sep 26 16:58 .
drwxr-xr-x 1 root root  4096 Sep  7 01:21 ..
-rw-r--r-- 1 root root   146 Sep 26 16:58 SECRET-TRAPPED
-rw-r--r-- 1 root root   609 Dec 25  2019 backward.rb
-rw-r--r-- 1 root root   873 Dec 25  2019 exceptions.rb
-rw-r--r-- 1 root root  9738 Dec 25  2019 generic_request.rb
-rw-r--r-- 1 root root 16206 Dec 25  2019 header.rb
-rw-r--r-- 1 root root   272 Dec 25  2019 proxy_delta.rb
-rw-r--r-- 1 root root   746 Dec 25  2019 request.rb
-rw-r--r-- 1 root root  2981 Dec 25  2019 requests.rb
-rw-r--r-- 1 root root 10749 Dec 25  2019 response.rb
-rw-r--r-- 1 root root 10040 Dec 25  2019 responses.rb
-rw-r--r-- 1 root root  2242 Dec 25  2019 status.rb
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/sh/include/mach-sh03$ cat /usr/lib/ruby/2.7.0/net/http/SECRET-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{ER_nVdNIR02DmavYkTsnPDYddiF.QX5IDO0wSN2kjNzEzW}
```

## What I learned 
I learnt how to go on following hints and also learned how to access files without directly using cd.


