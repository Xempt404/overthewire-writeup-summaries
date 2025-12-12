# Bandit Level 15

## Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Commands Used
- echo
- nc

## Steps
1. Ran `echo {Current_Password} | nc 127.0.0.1 30000` to send the current level’s password to the specified port using netcat.

## Summary
This level introduces transmitting input through netcat.