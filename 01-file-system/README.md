# File System Basics

## Instructions

Branch off from main, and then update this README with the answers / commands used for each question.
Add, commit and push your changes in git, and then submit a pull request on github.

## Navigation Questions

1. Display all the users currently logged on to your system - users

2. Using the help facility how can you make the command show the time the system was last started - uptime

3. Using the date command display the date in the following format "Tue 09 Aug 2016 - 13:46 BST" - date -R

4. Look for a command that will concatenate the output of a file to the screen (also known as standard output). Use that command to show the contents of the /etc/hosts file - cat /etc/hosts

5. What option to cat will show you the line numbers in the file? cat -b

6. List all files and their attributes in the current directory including hidden files ls -a

7. What option to ls will give me the file sizes in human readable format? Run the command on the /tmp directory. - ls -h , cd/tmp ls -h
cd 
8. What option will show just the size and filename, and how can you sort it by size. -s, -S

9. The output from your answer in 8 would have been from highest to lowest. Is there an option to reverse the order? -r


## Manipulation Questions

1. From your home directory and then each directory in turn work out a cd command that will provide a relative move to the following directories;

```bash - cd /```bash
/usr/bin - cd /usr/bin
/usr/share/lib/terminfo - cd /usr/share/lib/terminfo 
/etc - cd /etc
``` - cd /```

2. From the following absolute paths can you draw the tree structure?

```bash
/home/system

/home/system/hoth
/home/system/hoth/base , /home/system/hoth/planet

/home/system/destroyer
/home/system/destroyer/droid

/home/user1
/home/user1/somedir
```

3. Find out what directory you are in. - pwd

4. What is the quickest way of getting back to your home directory? Execute the command. cd ~

5. The command touch allows you to create an empty file if it does not already exist, or update times if it does. touch 

6. Create a filename that has spaces in it. touch file name

7. Are there any hidden files in your home directory? .bash_history  .bash_profile    .ssh 
..  .bash_logout   .bashrc        .lesshst

8. What is the largest file in your directory? How do you find it? ls -s , passwd

9. Locate all the files in the /usr/bin and the /etc directory that begin with a p. find /usr/bin p*

10. Locate files in the system that are of a character or block type. You will need to consult the manual pages for the command. Hint: you will need a –o option to look for more of the same criteria.


11. Copy the /etc/passwd file to your home directory. - cp /etc/passwd .

12. Who owns the file? Can you delete it? If so, why? Could you delete the /etc/passwd file? If not why not? root root,  no it is write protected

13. Make a directory in your home directory called newdir. - mkdir newdir

14. Create 3 files in the directory called file1, file2 and file3. - touch file1 , touch file2, touch file3

15. Rename the directory to olddir. Can you delete the directory? Which commands did you try? rm-r olddir

16. How many entries are there in the /etc/passwd file, without manually counting them?  cat -b /etc/passwd - 24

17. What type of file is /etc/rc? non existent

18. Try out these commands;

```bash - syntax error
cat /etc/passwd - shows the tree
cat /etc/hosts - local host domains
cat /etc/passwd /etc/hosts - same as cat /etc/hosts
```

What happened?

19. Enter the following commands and observe what happens using commands like, ls –l, cat

```bash - error
cd - no such file or directory
touch "This file   ""		# 3 spaces after file - saves as seperate files
ls –l				# Can you see the spaces? - no
```

Try the following command to identify the spaces:
```bash
ls | od - 

c0000000   e   x   a   m   p   l   e   -   f   i   l   e  \n   f   i   l
0000020   e  \n   p   a   s   s   w   d  \n   t   e   s   t  \n   t   e
0000040   s   t   -   2  \n   t   h   i   s  \n

```

