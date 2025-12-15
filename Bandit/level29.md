# Bandit Level 29

## Level Goal
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28. Clone the repository and find the password for the next level.

## Commands Used
- mkdir
- git
- cd
- ls
- cat

## Steps
1. Created new directory `mkdir temp` and navigated to it.
2. Clone repo with `git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo`.
3. Ran `cd repo` and `ls` to list files.
4. Read only file present `cat README.md` and found credentials with password censored.
5. Ran `git log` to check for previous commits and found `b0354c7 fix info leak`.
6. Investigated with `git show b0354c7` and found the password.

## Summary
This level introduces recovering sensitive info from Git history.