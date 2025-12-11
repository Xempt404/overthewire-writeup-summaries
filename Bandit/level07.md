# Bandit Level 7

## Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Commands Used
- find
- cat

## Steps
1. Used `find / -type f -size 33c -user bandit7 -group bandit6` to recursively search from the root for files with a specific size and user/group ownership. Found a single file `/var/lib/dpkg/info/bandit7.password`. Optional to use `2>/dev/null` to suppress permission denied errors.
2.  Used  `cat /var/lib/dpkg/info/bandit7.password` to view the contents.

## Summary
This level introduces filtering files by user/group ownership.