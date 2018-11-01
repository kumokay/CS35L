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







void qsort (void* base, size_t num, size_t size,
            int (*compar)(const void*,const void*));

| a | b | c | d | ....
  ^   ^
  p1  p2

int mycmp(const void* p1,const void* p2)
{
    return *p1 - *p2  
}

compar ==> mycmp (memory)



\0Quick23   \0Jumps!

secret1: memfrob("\0Quick23", 9) => "*{_CIA\030\031 "
secret2: memfrob("\0Jumps!", 9) => "*`_GZY\v "

The memfrob() function encrypts the first n bytes of the memory area s
       by exclusive-ORing each character with the number 42.  
==> ch ^ 42


frobcmp("*{_CIA\030\031 ", "*`_GZY\v ")
=> memfrob("*{_CIA\030\031 ", NBYTES) => "\0Quick23"
=> memfrob("*`_GZY\v ", NBYTES) => "\0Jumps!"

=> 0
=> Q,J +1

a - b = ?
'\0' - '\0' 
'Q' - 'J' > 0 ==> +


gcc -o sfrob -g sfrob.c


'*~BO *{_CIA *hXE]D *LER #@_GZY #E\\OX #^BO #FKPS #NEM\4'

*~BO 
*{_CIA *hXE]D 
*LER 
#@_GZY 
#E\\OX 
#^BO 
#FKPS 
#NEM\4

^@The
^@Quick
^@Brown
^@fox
^Ijumps
^Iover
^Ithe
^Ilazy
^Idog.

^@Brown
^@Quick
^@The
^@fox
^Idog.
^Ijumps
^Ilazy
^Iover
^Ithe

qsort(array1, NUM, frobcmp)



int frobcmp(char const* a, char const* b)
{

  // result = 0, 1, -1
  return result;
}

a (pointer) -> 'asdfggsdagsdahagdgsgera'
b (pointer) -> 'asdfggsdagfsdfasdahaera'



> run /tmp/tmp.iBxo93Salp -lt --full-time wwi-armistice now now1



