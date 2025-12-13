# Bandit Level 25

## Level Goal
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

## Commands Used
- echo
- nc
- seq

## Steps
1. Tested the daemon response at 30002 with `echo "{bandit24_pass} 1234" | nc localhost 30002` and got response.
2. Used a loop with `seq` to iterate through all 4 digit numbers form `0000 - 9999` and piped into `| grep -v Wrong` to skip all unsuccessful tries and speed up output.
3. Found password with `for pin in $(seq -w 0000 9999); do echo "{bandit24_pass} $pin"; done | nc localhost 30002 | grep -v Wrong`

## Summary
This level introduces brute‑forcing a network daemon.