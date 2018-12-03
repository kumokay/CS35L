### when and where
12/11 (Tue.) 3pm-6pm, Final Exam: COM SCI 35L LAB 6 (BOELTER 3760)

### one-liner linux command: 10 * 3 => 30
- Linux commands we learned in Assignment 1-9
  * find grep mv ls chmod wget tr ln touch sleep cat sort shuf grep apt-get
- How to use `|`, `&&`, `>`, `<`, etc

### coding: 6 * 5 => 30
- Assignment 2. Shell scripting
  * how to manipulate text from the command line with sed and regular expression
- Assignment 3. Modifying and rewriting software
  * given the source code and a patch file, what is the result after applied the patch
- Assignment 4. C programming and debugging
  * how to use malloc and free correctly
- Assignment 6. Multithreaded performance
  * given a piece of c code, modify it and make it multithreaded
- Assignment 7. Dynamic linking
  * given some gcc commands to build a project, write a makefile based on those commands

### open-ended question: 4 * 10 => 40 (print out the slides and you can find the aswer)
- Assignment 5. System call programming and debugging
- Assignment 7. Dynamic linking
- Assignment 8. SSH setup and use in applications
- Assignment 9. Change management

### other things
- We will not ask you to write a shell script or a python script
- We will not ask you any question regarding emacs, vim, and other editors
- We will not ask you any question regarding beaglebone setup
- There will be a bonus question (10 points) that you can use any language you like (either c, c++, or python). But the maximum you can get in total is still 100 points.

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
