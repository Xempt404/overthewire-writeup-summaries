# Natas Level 10

## Steps
1. Opened the level page in the browser.
2. Encountered input box to search for words in a dictionary.
3. Checked source code and saw input being evaluated by the shell `passthru("grep -i $input dictionary.txt");`. However noticed input sanitizing `preg_match('/[;|&]/',$key)`.
4. Used `-f /etc/natas_webpass/natas11 /etc/natas_webpass/natas11` to get grep to return the file and password.

## Summary
Introduces argument injection attacks.
