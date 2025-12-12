# Bandit Level 22

## Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Commands Used
- ls
- cat

## Steps
1. Checked cron job definitions `ls /etc/cron.d`. Chose to investigate `cronjob_bandit22`.
2. Viewed contents of cron job `cat /etc/cron.d/cronjob_bandit22`. The cron job runs a script as user bandit22, and writes the output to a file in `/tmp/`.
3. Displayed the file written by the cron job `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv`. Found password.

## Summary
This level introduces inspecting cron jobs in linux.