# Bandit Level 30

## Level Goal
There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29. Clone the repository and find the password for the next level.

## Commands Used
- mkdir
- git
- cd
- ls
- cat

## Steps
1. Created new directory `mkdir temp` and navigated to it.
2. Clone repo with `git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo`.
3. Ran `cd repo` and `ls` to list files.
4. Read only file present `cat README.md` and found `password: <no passwords in production!>`.
5. Checked for development environments with `git branch -a` and found a `dev` branch.
6. Switched to `dev` branch `git checkout dev` and listed commits `git log`. Noticed `commit eb435001e0eb0219ee071219d1f16f1cd3941a3b (add data needed for development)`.
7. Investigated commit with `git show eb435001e0eb0219ee071219d1f16f1cd3941a3b` and found the password.

## Summary
This level introduces recovering sensitive information from Git branches.