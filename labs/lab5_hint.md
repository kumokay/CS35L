dd if=/dev/urandom of=bigfile.txt bs=1M count=5

YOURPROG 12345 abcde < bigfile.txt

strace -o trace.txt YOURPROG 12345 abcde < bigfile.txt

time YOURPROG 12345 abcde < bigfile.txt

https://linux-audit.com/the-ultimate-strace-cheat-sheet/
