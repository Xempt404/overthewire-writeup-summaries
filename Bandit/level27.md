# Bandit Level 27

## Level Goal
Good job getting a shell! Now hurry and grab the password for bandit27!

## Commands Used
-

## Steps
1. Logged into bandit26 and resized  terminal vertical length so `more` wouldn't exit instantly.
2. Once paused at `--More--` pressed `v` to open `vi` and then `ESC` and typed `:set shell=/bin/bash` followed by `:shell` to modify and launch the shell.
3. Ran `ls -la` to list all files and permissions. Spotted `bandit27-do` owned by bandit27 that when executed runs a command as bandit27.
4. Ran `./bandit27-do cat /etc/bandit_pass/bandit27` to reveal the password for next level.

## Summary
This level introduces escaping restricted shells (continued).