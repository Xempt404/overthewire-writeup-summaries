# Bandit Level 23

## Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Commands Used
- ls
- cat
- echo
- md5sum

## Steps
1. Listed cron job entries `ls /etc/cron.d`. Found the relevant file `cronjob_bandit23`.
2. Looked for script `cat /etc/cron.d/cronjob_bandit23`. Found `/usr/bin/cronjob_bandit23.sh` running as bandit23.
3. Viewed script contents `cat /usr/bin/cronjob_bandit23.sh` and noticed `myname=$(whoami)`, `mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)` and `cat /etc/bandit_pass/$myname > /tmp/$mytarget` are being used to construct a hashed filename.
4. Recreated the hash manually `echo I am user bandit23 | md5sum | cut -d ' ' -f 1` and returned `8ca319486bfbbc3663ea0fbe81326349`.
5. Used the string from previous step to find password `cat /tmp/8ca319486bfbbc3663ea0fbe81326349`.

## Summary
This level introduces variables and hashing in cron jobs.