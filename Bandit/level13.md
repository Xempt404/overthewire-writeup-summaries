# Bandit Level 13

## Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Commands Used
- mktemp
- cp
- file
- xxd
- mv
- gunzip
- bunzip2
- tar

## Steps
1. Created a temporary working directory and copied `data.txt` into it.
2. Used `xxd -r` to reverse the hexdump into a binary file.
3. Used `file` repeatedly to identify the compression format at each stage.
4. Decompressed layers using `gunzip`, `bunzip2`, and `tar`, renaming files as needed.
5. Continued this process through multiple nested layers until the final ASCII text file was revealed.

## Summary
This level introduces hexdumps, identifying file types and handling multiple compression formats in sequence.