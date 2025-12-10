# Bandit Level 1

## Level Goal
The password for the next level is stored in a file called `-` located in the home directory

## Commands Used
- cd
- pwd
- ls
- cat

## Steps
1. Ensured I was in the home directory using `cd ~` and confirmed with `pwd`.
2. Listed the files with `ls` and found a file named `-`.
3. Used `cat ./-` to view the contents. The `./` is necessary because `-` would otherwise be interpreted as an option by `cat`.

## Summary
This level introduces how to handle files with special characters in Linux, which might be mistaken for command options.