# Bandit Level 3

## Level Goal
The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

## Commands Used
- pwd
- ls
- cat

## Steps
1. Ensured I was in the home directory using `pwd`.
2. Listed the files with `ls` and found a file named `--spaces in this filename--`.
3. Used `cat "./--spaces in this filename--"` to view the contents. The surrounding quotations are necessary because the filename includes spaces.

## Summary
This level introduces how to handle filenames including spaces in Linux.