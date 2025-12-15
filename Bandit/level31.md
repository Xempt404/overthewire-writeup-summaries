# Bandit Level 31

## Level Goal
There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30. Clone the repository and find the password for the next level.

## Commands Used
- mkdir
- git
- cd
- ls
- cat

## Steps
1. Created new directory `mkdir temp` and navigated to it.
2. Clone repo with `git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo`.
3. Ran `cd repo` and `ls` to list files.
4. Read only file present `cat README.md` and found `just an epmty file... muahaha`.
5. Checked logs `git logs` and branches `git branch -a` and found nothing.
6. Checked tags with `git tag` and found a tag named `secret`. 
7. Displayed tag content with `git show secret` and found password.

## Summary
This level introduces recovering sensitive information from Git tags.