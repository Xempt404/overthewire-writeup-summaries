# Bandit Level 28

## Level Goal
There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27. Clone the repository and find the password for the next level.

## Commands Used
- mkdir
- cd
- git
- ls
- cat

## Steps
1. Created new directory `mkdir temp` and navigated to it.
2. Clone repo with `git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo`.
3. Ran `cd repo` and `ls` to list files.
4. Read only file present `cat README` and found password.

## Summary
This level introduces cloning GitHub repositories through SSH.