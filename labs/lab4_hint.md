## How to use gdb

https://www.cs.cmu.edu/~gilpin/tutorial/
https://www.cs.cmu.edu/~gilpin/tutorial/main.cc
https://darkdust.net/files/GDB%20Cheat%20Sheet.pdf

gcc –o FooBarBinary -g foobar.c
gdb FooBarBinary

## Lab4 hint:
wget https://web.cs.ucla.edu/classes/fall18/cs35L/assign/coreutils-with-bug.tar.gz
tar -xvzf TARBALL
./configure
make
make install
or do whatever you did for lab3

patch -p0 < YOUR_PATCH_FILE

gdb src/ls
run -lt --full-time /tmp/tmp.K1YC7ewlat

result:
-rw-r--r-- 1 hsiaoyun csgrad 0 1918-11-11 03:00:00.000000000 -0800 wwi-armistice
-rw-r--r-- 1 hsiaoyun csgrad 0 2018-10-30 11:17:49.523957656 -0700 now1
-rw-r--r-- 1 hsiaoyun csgrad 0 2018-10-30 11:17:25.492544342 -0700 now

should be
-rw-r--r-- 1 hsiaoyun csgrad 0 2018-10-30 11:17:49.523957656 -0700 now1
-rw-r--r-- 1 hsiaoyun csgrad 0 2018-10-30 11:17:25.492544342 -0700 now
-rw-r--r-- 1 hsiaoyun csgrad 0 1918-11-11 03:00:00.000000000 -0800 wwi-armistice

(1) hint about where to start:
gdb> break main  # let's start from the main()
gdb> next........
(2) what should we look for?
seems like the sorted file list is wrong.. find something related to "sort"




