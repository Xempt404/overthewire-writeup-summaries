# Bandit Level 5

## Level Goal
The password for the next level is stored in the only human-readable file in the `inhere` directory. Tip: if your terminal is messed up, try the “reset” command.

## Commands Used
- ls
- cd
- file
- cat

## Steps
1. Listed the folders with `ls` and found a folder named `inhere`.
2. Used `cd inhere` to change current directory to the folder. 
3. Used `ls` to list files and found 10 files `-file00` to `-file09`.
4. Used `file ./*` to data types in current directory and found `-file07` was ASCII text.
5. Used `cat ./-file07` to view the contents.

## Summary
This level introduces how to examine a filetype from its contents.