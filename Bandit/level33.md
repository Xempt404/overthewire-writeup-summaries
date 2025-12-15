# Bandit Level 33

## Level Goal
After all this git stuff, it’s time for another escape. Good luck!

## Commands Used
- $0
- ls
- whoami
- cat

## Steps
1. Logged into Bandit Level 33 and was placed into an uppercase shell.
2. Noticed all input was automatically converted to uppercase and standard commands did not work because Linux commands are case-sensitive.
3. Typed $0, which expanded to the path of the current shell escaping the uppercase shell.
4. Listed files and permission `ls -la` and found `uppershell` owned by bandit33 and verified with `whoami` the current shell is running as bandit33.
5. Read the password file `cat /etc/bandit_pass/bandit33`.


## Summary
This level introduces escaping restricted shells using shell variable expansion.