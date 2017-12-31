# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * **pwd**: show current working directory path
> > * **mkdir**: creating a directory
> > * **rm -r**: deleting a directory
> > * **touch test.txt**: create file "text.txt" using "touch" command
> > * **rm test.txt**: deleting file "text.txt" 
> > * **mv A.txt B.txt**: renaming file "A.txt" to "B.txt"
> > * **ls -a**: listing files including hidden files
> > * **cp dir1/test.txt dir2/**: copy file test.txt from dir1 to dir2
> > * **echo A.txt > B.txt**: copy the contents in file A.txt to B.txt, overwriting existing contents in B.txt
> > * **cat A.txt**: view the contents of A.txt
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > **ls**: list all files and directories in the current folder  
> > **ls -a**: **ls** including hidden files  
> > **ls -l**: **ls** using the long format (file mode, number of links, owner name, group name, bytes, month/day/year/hour/minute last modified, path-name)  
> > **ls -lh**, **ls** using long format, with byte number in Byte, Kilobyte, Megabyte, Gigabyte, Terabyte, or Petabyte in order to reduce the number of digits  
> > **ls -lah**: **ls** including hidden files, using long format and bite number in unit suffixes  
> > **ls -t**: **ls** in the order of most recently modified  
> > **ls -Glp**: **ls** using long format and colorized output, also directories will be displayed with a slash ('/') after the file name  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > **ls -c**: display files by timestamp  
> > **ls -lur**: display files using long format, by most recent access  
> > **ls -d**: display directories only  
> > **ls -R**: display sub-directories as well  
> > **ls -1**: display each file on one line  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > REPLACE THIS TEXT WITH YOUR RESPONSE

 

