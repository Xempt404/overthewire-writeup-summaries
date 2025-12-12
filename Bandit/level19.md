# Bandit Level 19

## Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Commands Used
- ssh
- ls
- cat

## Steps
1. Connected with `ssh bandit18@bandit.labs.overthewire.org -p 2220` and got logged out instantly.
2. Tried `ssh bandit18@bandit.labs.overthewire.org -p 2220 "ls"` and got output of home directory with 1 file called `readme`.
3. Viewed contents of file using `ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"`

## Summary
This level introduces running commands on a remote server via SSH without opening a terminal.