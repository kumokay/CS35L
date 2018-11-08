dd if=/dev/urandom of=bigfile.txt bs=1M count=5

YOURPROG 12345 abcde < bigfile.txt

strace -o trace.txt YOURPROG 12345 abcde < bigfile.txt

time YOURPROG 12345 abcde < bigfile.txt

https://linux-audit.com/the-ultimate-strace-cheat-sheet/


## check EOF or other errors:

!feof(stdin)
ferror(stdin)


## homework: use read, write, fstat
```
#include <sys/types.h>
#include <sys/stat.h>
#include <unistd.h>

struct stat buf;
int ret = fstat(STDIN_FILENO, &buf);
printf("ret=%d, file sz=%d\n", ret, buf.st_size);
// if not a file => buf.st_size will be 0
// otherwise it will be the file size
// BUT if the file is realy big, st_size may grow and you still need to check EOF

malloc => buf.st_size+1
```
