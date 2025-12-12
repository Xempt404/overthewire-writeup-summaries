# Bandit Level 21

## Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

## Commands Used
- ls
- tmux
- nc

## Steps
1. Ran `ls` to list files.
2. Launched `tmux` and created 2 panes (optional). 
3. Started a lsitener in terminal using `nc -l -p 9293`.
4. Ran the suid binary `./suconnect 9293` in the other.
5. Switched to the listener terminal and typed password and pressed enter.
6. Password for next level revealed.

## Summary
This level introduces using netcat to interact with a setuid binary.