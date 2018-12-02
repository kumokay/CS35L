### one-liner linux command: 10 * 3 => 30
- Linux commands we learned in Assignment 1-9
  * find grep mv ls chmod wget tr ln touch sleep cat sort shuf grep apt-get
- How to use `|`, `&&`, `>`, `<`, etc

### short answer and coding: 6 * 5 => 30
- Assignment 2. Shell scripting
  * how to manipulate text from the command line with sed and regular expression
- Assignment 3. Modifying and rewriting software
  * given a patch file, what is the result after applied the patch
- Assignment 4. C programming and debugging
  * how to use malloc and free correctly
- Assignment 6. Multithreaded performance
  * given a piece of c code, modify it to make it multithreaded
- Assignment 7. Dynamic linking
  * write a makefile to build your project

### open-ended question: 4 * 10 => 40 (print out the slides and you can find the aswer)
- Assignment 5. System call programming and debugging
- Assignment 7. Dynamic linking
- Assignment 8. SSH setup and use in applications
- Assignment 9. Change management

### sample questions:
- one-liner linux command:
  * pick a random integer from [1,10] and save the result to number.txt
    ```
    shuf -i 1-10 -n 1 > number.txt
    ```
- scripting and coding:
  * To build test.c we need to run `gcc -o test test.c`. Create a makefile such that we only need to type `make` to compile test.c and type `clean` to delete the old executable file.
    ```
    CC = gcc
    
    default: test

    test: test.c
        $(CC) -o test test.c

    clean:
        rm test
    ```
    
- open-ended question:
  * Explain how the sender/receiver communicate securely using public key and private key
  ```
  You can find the answer on the slides. 
  As long as there is nothing too crazy you will not lose any points.
  ```
