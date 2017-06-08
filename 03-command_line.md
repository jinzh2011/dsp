# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

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

> >  Use | Command
> > ------- | --------------------
    show current working directory path| `pwd`
    creating a directory | `mkdir`*`dir_name`*
    deleting a directory | `rm -rf`*`dir_name`*
    creating a file using `touch` command | `touch`*`file_name`*
    deleting a file | `rm`*`file_name`*
    renaming a file | `mv`*`file_name new_file_name`*
    listing hidden files | `ls -a`
    copying a file from one directory to another | `cp`*`original_file_name  new_dir_name`*
    copying all files from current directory to another | `cp`* `new_dir_name`*
    change directory | `cd`*`dir_name`*
    change directory to two levels up | `cd ../..`
    move file from one directory to another | `mv`*`file_name new_dir_name`*




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

> > Command | Use
> > ------- | ---------
    `ls` |  lists all files and directories in the working directory
    `ls -a` |  lists all contents, including hidden files and directories
    `ls -l` | lists all contents of a directory in long format
    `ls -lh` |  lists all contents of a directory in long format, print size in human readable format
    `ls -lah` | lists all contents of a directory including hidden files in long format, print size in human readable format
    `ls -t` | order files and directories by the time they were last modified
    `ls -Glp` | lists all contents of a directory in long format, don't list group names, add slash to directories


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > * ls -a
* ls -lh
* ls -t
* ls -p
* ls -l1r


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` build and execute command lines from standard in. For example, the following bash command shows how to use `xargs` to remove all files with file extension .c. `find . -name "*.c" ` returns all files names with extension .c as standard in, and `xargs` take the standard in and execute it with `rm -rf` command to remove files with extension .c.
```bash
$ ls
apple.c  apple.h  orange.c  orange.h
$ find . -name "*.c" | xargs rm -rf
$ ls
apple.h  orange.h
```
