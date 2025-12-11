# Bandit Level 12

## Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Commands Used
- ls
- cat
- tr

## Steps
1. Used `ls` to list files.
2. Used `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'` to output the data and shift each letter 13 spaces to reverse the rot13.

## Summary
This level introduces translating characters in linux.