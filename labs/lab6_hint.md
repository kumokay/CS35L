### Lab hint

1. check your sort version; make sure that it supports multithreading
```
sort --version
```

2. generate a file of random floats
```
od -An -t fF -N NUMBER_OF_BYTES < /dev/urandom | tr -s [:blank:] '\n' | sed '/^$/d' > random.txt
```

3. sort
```
time -p sort -g random.txt > /dev/null
time -p sort -g --parallel=N_THREADS random.txt > /dev/null
```

### Homework hint

1. get the source code, compile and try it!
```
wget https://web.cs.ucla.edu/classes/fall18/cs35L/assign/srt.tgz
tar -xf srt.gz
cd srt
make
./srt
```

2. follow the example on wiki to modify main.c : https://en.wikipedia.org/wiki/POSIX_Threads
- move the per-pixel operations inside the for-loop to a function, and run that function in THREADS
```
void *perform_work(void *arguments){
    // your code
}
```
- use malloc to get memory space for thread-IDs, arguments, etc
```
struct MyArgument
{
    // some values that you need to pass into the function
};

pthread_t*  tid = (pthread_t*) malloc(sizeof(pthread_t) * nthreads);
struct MyArgument* argument = (struct MyArgument*) malloc(sizeof(struct MyArgument) * nthreads);
```
