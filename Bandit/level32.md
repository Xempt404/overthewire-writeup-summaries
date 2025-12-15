# Bandit Level 32

## Level Goal
There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31. Clone the repository and find the password for the next level.

## Commands Used
- mkdir
- git
- cd
- ls
- cat

## Steps
1. Created new directory `mkdir temp` and navigated to it.
2. Clone repo with `git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo`.
3. Ran `cd repo` and `ls` to list files.
4. Read only file present `cat README.md` and found details to push a file to the remote repo with `File name: key.txt, Content: 'May I come in?', Branch: master`
5. Created the file `echo 'May I come in?' > key.txt`.
6. Staged file with `git add -f key.txt`. `-f` was needed because of `.gitignore` file.
7. Added commit messages with `git commit -m "anything"` and pushed to remote `git push -u origin master`. 

## Summary
This level introduces pushing files to remote repository.