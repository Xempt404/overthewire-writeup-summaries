# Bandit Level 5

## Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable


## Commands Used
- ls
- cd
- ls
- file

## Steps
1. Listed the folders with `ls` and found a folder named `inhere`.
2. Used `cd inhere"` to change current directory to the folder. 
3. Used `ls -la` to list everything and found 20 folders.
4. Used `find . -type f -size 1033c ! -perm /111` to recursively search and find the file. `-type f` was used to filter for files only, `-size 1033c` was used to only display files 1033 bytes in size and `! -perm /111` was used to exclude files with any executable permission bit set.

## Summary
This level focuses on filtering files by size and permissions.