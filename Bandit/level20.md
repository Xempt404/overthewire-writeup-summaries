# Bandit Level 20

## Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Commands Used
- ls
- whoami
- cat

## Steps
1. Used `ls -la` to list all files and permissions in directory. Found `bandit20-do` owned by bandit20.
2. Ran `./bandit20-do` and got the output `Run a command as another user`.
3. Ran `./bandit20-do whoami` and verified that it was running with permissions of the owner (bandit20).
4. Executed `./bandit20-do cat /etc/bandit_pass/bandit20` to reveal password.

## Summary
This level introduces setuid binaries.