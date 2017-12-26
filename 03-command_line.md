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

> > pwd : show current working directory path  
> > mkdir $name: create a directory  
> > rm $name : delete a directory or file (-r recursive, -f force)  
> > touch $name: create a file (if not existing) or update access / modified dates (if existing)  
> > mv $currentname $newname: rename a file  
> > ls -a : lists all files (including hidden)  
> > ls -d .?* : lists only hidden files & directories  
> > mv $source $dest: move a file  
> > cp $source $dest: copy a file  
> > cd $directory : change current working directory  

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

>> ls : list files in current directory  
>> ls -a : list all files in current directory (include hidden)  
> > ls -l : list files w/ long-form details (permissions, create date, size)  
> > ls -lh : list files w/ long-form details + human readable size (e.g. kb / mb)  
> > ls -lah : list all files (include hidden) w/ long form details + human readable size  
> > ls -t : list files sorted by last modified  
> > ls -Glp : list files w/ long form details, exclude group name, add / after directory names  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -R : also runs ls on subdirectories  
> > ls -d : only list directories  
> > ls -m : list as a single comma-separated line  
> > ls -r : reverse order  
> > ls -X : sort by entry extension  
> > ls -S : sort by file size  

---


### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > REPLACE THIS TEXT WITH YOUR RESPONSE

 

