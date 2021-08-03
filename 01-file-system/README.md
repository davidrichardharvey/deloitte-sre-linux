# File System Basics

## Instructions

Branch off from main, and then update this README with the answers / commands used for each question.
Add, commit and push your changes in git, and then submit a pull request on github.

## Questions

1. Display all the users currently logged on to your system
		i. who

2. Using the help facility how can you make the command show the time the system was last started
		i. man who; command is who -b

3. Using the date command display the date in the following format "Tue 09 Aug 2016 - 13:46 BST"
		i. date +'%a %d %b %Y - %R %Z'
		
4. Look for a command that will concatenate the output of a file to the screen (also known as standard output). Use that command to show the contents of the /etc/hosts file
		i. cat /etc/hosts
		
5. What option to cat will show you the line numbers in the file?
		i. -b
		
6. List all files and their attributes in the current directory including hidden files
		i. ls -la .
		
7. What option to ls will give me the file sizes in human readable format? Run the command on the /tmp directory.
		i. -sh
		
8. What option will show just the size and filename, and how can you sort it by size.
		i.  -sS

9. The output from your answer in 8 would have been from highest to lowest. Is there an option to reverse the order?
		i. -r