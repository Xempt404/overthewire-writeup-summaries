# Bandit Level 24

## Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Commands Used
- ls
- cat
- mkdir & mktemp
- nano
- chmod

## Steps
1. Listed cron job entries `ls /etc/cron.d`. Found the relevant file `cronjob_bandit24`.
2. Looked for script `cat /etc/cron.d/cronjob_bandit24`. Found `/usr/bin/cronjob_bandit24.sh` running as bandit24.
3. Noticed it executes all scripts owned by bandit23 located in `/var/spool/bandit24/foo` every 60 seconds.
4. Checked folder permissions `ls -la /var/spool/bandit24/` and noticed write permissions.
5. Created temp folder `/tmp/tmp.LWOEkGMmAa` for script with `mktemp -d`.
6. Made a script `nano /tmp/tmp.LWOEkGMmAa/script.sh` that outputs bandit24's password to a shared folder between both users. `cat /etc/bandit_pass/bandit24 > /tmp/bandit24.password`.
7. Made it executable `chmod +x /tmp/tmp.LWOEkGMmAa/script.sh` and added to required folder `cp /tmp/tmp.LWOEkGMmAa/script.sh /var/spool/bandit24/foo/script.sh`.
8. Waited 60 seconds and checked for file `ls /tmp/bandit24.password` and found password.

## Summary
This level introduces running cron scripts as other users.