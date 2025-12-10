# Bandit Level 3

## Level Goal
The password for the next level is stored in a hidden file in the **inhere** directory.

## Commands Used
- ls
- cd
- cat

## Steps
1. Listed the folders with `ls` and found a folder named `inhere`.
2. Used `cd inhere"` to change current directory to the folder. 
3. Used `ls -a` to list all files and found `...Hiding-From-You`. The `-a` flag is necessary to show all files including hidden files.
4. Used `cat ...Hiding-From-You` to view the contents.

## Summary
This level introduces how to handle hidden files in Linux.