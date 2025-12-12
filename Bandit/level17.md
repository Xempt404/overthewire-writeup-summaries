# Bandit Level 17

## Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Commands Used
- nmap
- echo
- openssl
- icacls or chmod
- ssh
- cat

## Steps
1. Ran an `nmap` scan on the port range with `nmap -p31000-32000 localhost` and found 5 open ports.
2. Checked the ports for SSL with `nmap -p31046,31518,31691,31790,31960 --script ssl-enum-ciphers localhost` and found 2 ports speaking SSL/TLS.
3. Tried sending current level password to both ports. `echo {Current_Password} | openssl s_client -connect localhost:{port} -quiet`. 31518 was unsuccessful but 31790 provided SSH private key.
4. Copied the private key to host machine and reduced permissions with `icacls key.txt /inheritance:r /grant:r "$($env:USERNAME):(R)"` for windows. `chmod 600 key.txt` for linux.
5. Logged into next level `ssh -i key.txt bandit17@bandit.labs.overthewire.org -p 2220`.
6. Got the password for bandit17 using `cat /etc/bandit_pass/bandit17`.

## Summary
This level introduces nmap host and service scanning.