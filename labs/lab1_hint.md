# Laboratory: Linux and Emacs scavenger hunt

Instructions: Do this assignment on the SEASnet GNU/Linux servers lnxsrv06, lnxsrv07, lnxsrv09, or lnxsrv10, with /usr/local/cs/bin prepended to your PATH. Use the commands that you learned in class to find answers to these questions. Don't use a search engine like Google, and don't ask your neighbor, don't use GitHub, etc. If you need a hint, ask the TA. When you find a new command, run it so you can see exactly how it works. In addition to turning in the answers to these questions, turn in a description of your session discovering them.

As you do actions, use Emacs to record your keystrokes and each answer in plain-text files key1.txt and ans1.txt that you will submit as part of the assignment. If you prefer, you can record and submit Org files key1.org and ans1.org instead of .txt files; see Hello Worg for Org introductions and tutorials.

1. What shell command uses the man program to print all the commands that have a specific word in their man page (or at least the description part of the man page)? (hint: man man)

man -k SOME_COMMAND

2. Where are the mv and sh programs located in the file system? List any shell commands you used to answer this question.

which SOME_COMMAND

3. What executable programs have names that are exactly two characters long and end in r, and what do they do? List any shell commands you used to answer this question.

man -k ^[a-z]r$

4. When you execute the command named by the symbolic link /usr/bin/emacs, which file actually is executed? List any shell commands you used to answer this question.

which COMMAND

5. What is the version number of the /usr/bin/gcc program? of the plain gcc program? Why are they different programs?

/usr/bin/gcc -v
gcc -v

6. The chmod program changes permissions on a file. What does the symbolic mode u+sx,o-w mean, in terms of permissions?

do `man chmod` and you will see

7. Use the find command to find all directories modified in the last four weeks that are located under (or are the same as) the directory /usr/local/cs. List any shell commands you used to answer this question.

find DIR_PATH -type d -mtime -N_DAYS

8. Of the files in the same directory as find, how many of them are symbolic links? List any shell commands you used to answer this question.

find DIR_PATH -type l -mtime -N_DAYS

9. What is the oldest regular file in the /usr/lib64 directory? Use the last-modified time to determine age. Specify the name of the file without the /usr/lib64/ prefix. Consider files whose names start with ".". List any shell commands you used to answer this question.

ls -lt

10. Where does the locale command get its data from? List any shell commands you used to answer this question.

do `man locale` search for PATH by typing '/PATH'

11. In Emacs, what commands have downcase in their name? List any Emacs commands you used to answer this question.

C-h a KEYWORD

12. Briefly, what do the Emacs keystrokes C-M-r through C-M-v do? Can you list their actions concisely? List any Emacs commands you used to answer this question.

C-h c KEYSTROKES

13. In more detail, what does the Emacs keystroke C-g do? List any Emacs commands you used to answer this question.

do `C-h c KEYSTROKES` it will show `C-g runs the command keyboard-quit`

then search for more details by doing `C-h f keyboard-quit`

14. What does the Emacs yank function do, and how can you easily invoke it using keystrokes? List any Emacs commands you used to answer this question.

C-h f DESCRIPTION

15. When looking at the directory /usr/bin, what's the difference between the output of the ls -l command, and the directory listing of the Emacs dired command? List any shell or Emacs commands you used to answer this question.

run `C-x d DIR_PATH` and `ls -l` to see the difference.

