# Bandit Level 8

## Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Commands Used
- ls
- sort
- uniq

## Steps
1. Used `ls` to list files.
2. Used `sort data.txt | uniq -u` to sort the data and `uniq -u` to display unrepeated lines.

## Summary
This level introduces sorting data and filtering adjacent lines.