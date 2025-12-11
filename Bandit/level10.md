# Bandit Level 10

## Level Goal
The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several '=' characters.

## Commands Used
- ls
- strings
- grep

## Steps
1. Used `ls` to list files.
2. Used `strings data.txt | grep ===` to output all readable strings and filter with `=` signs.

## Summary
This level introduces extracting and printing strings.