# Bandit Level 14

## Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

## Commands Used
- ls
- scp
- chmod (icacls for windows)
- ssh

## Steps
1. Used `ls` to list the file `sshkey.private`.
2. Exited the ssh terminal.
3. Used `scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .` to copy the file to my host machine.
4. Ran `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220` but got error 'permissions too open'.
5. Reduced permissions using `chmod 600 sshkey.private` and tried again successfully.
6. Used `cat /etc/bandit_pass/bandit14` to get the password for the level.

## Summary
This level introduces SSH key-based authentication.