# Bandit Level 26

## Level Goal
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

## Commands Used
- ls
- cat
- scp
- ssh
- vi

## Steps
1. Used `ls` to list home directory for bandit25. Found SSH private key for bandit26.
2. Checked what shell `bandit26` uses with `cat /etc/passwd | grep bandit26` and found `/usr/bin/showtext`.
3. Examined `/usr/bin/showtext` and confirmed bandit26 is forced into a `more` pager rather than a standard shell.
4. Copied SSH key to host `scp -P 2220 bandit25@bandit.labs.overthewire.org:~/bandit26.sshkey .`, reduced permissions and logged in to bandit26.
5. Kept getting kicked immediately so reduced terminal vertical length so `more` wouldn't exit instantly.
6. Once paused at `--More--` pressed `v` to open `vi` and then `ESC` and typed `:set shell=/bin/bash` followed by `:shell` to modify and launch the shell.
7. Retrieved password with `cat /etc/bandit_pass/bandit26`.

## Summary
This level introduces escaping restricted shells.