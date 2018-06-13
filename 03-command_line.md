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

> > - show current working directory path: ```pwd```  
> > - creating a directory: ```mkdir <directory name> ``` 
> > - deleting a directory: ```rmdir <directory name>```  
> > - creating a file using touch command: ```touch <filename>```        
> > - deleting a file: ```rm <filename>```  
> > - renaming a file: ```mv <original file name> <new file name>```  
> > - listing hidden files: ```ls -a```  
> > - copying a file from one directory to another: ```cp <source file (can include the path to that file. For example /home/user/Desktop/from.txt> <destination directory>```  
> > - changing directory: ```cd <destination directory>```  
> > - returns a list of environment variables: ```env```  

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

> > - ```Ls``` : lists all files and directories in the working directory.  
> > - ```ls -a```: lists all contents of a directory, including hidden files and directories  
> > - ```ls -l```: lists all contents in long format  
> > - ```ls -lh```:  lists long format with readable file size  
> > - ```ls -lah```: lists long format with readable file size, including hidden files and directories.  
> > - ```ls -t```: orders files and directories by the time they were last modified.  
> > - ```ls -Glp```:  lists all contents in long format with two options. Displaying directories with “/” at the end, and excluding the name of the group that owns the file.  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > - ```Ls -mp```: displays the names as a comma-separated list adding “/” at the end for directories.  
> > - ```Ls -o```: similar to ls -Gl, lists long format excluding group name.  
> > - ```Ls -rp```: lists files and directories in reverse order, adding “/” at the end for directories.  
> > - ```Ls -1p```: lists each entry on a line, adding “/” at the end for directories.  
> > - ```Ls -R```: lists files and directories, including sub-directories as well.  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > REPLACE THIS TEXT WITH YOUR RESPONSE

 

