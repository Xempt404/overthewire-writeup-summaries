# Bandit Level 16

## Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## Commands Used
- echo
- ncat or openssl

## Steps
1. Ran `echo {Current_Password} | ncat --ssl 127.0.0.1 30000` to send the current level’s password to the specified port using SSL. `ncat` was used instead of `nc` because `ncat` supports SSL.

## Summary
This level introduces transmitting input through netcat with SSL encryption.