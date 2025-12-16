# Natas Level 4

## Steps
1. Opened the level page in the browser.
2. Noticed an error message indicating that access is restricted based on the HTTP `Referer` header.
3. Spoofed `Referer` header with `curl -H "Referer: http://natas5.natas.labs.overthewire.org/" -u natas4:{pass} http://natas4.natas.labs.overthewire.org/.
4. Server responded with password.

## Summary
Introduces spoofing the HTTP `Referer` header to bypass access restrictions.
