# Natas Level 7

## Steps
1. Opened the level page in the browser.
2. Observed the query parameter `?page=`.
3. Tested a non-existent value `page=dskjsd` and received PHP warnings revealing that page is passed directly to `include()`. This confirmed a Local File Inclusion (LFI) vulnerability.
4. Using the LFI, accessed the file containing the next level’s password `page=/etc/natas_webpass/natas8` and retrieved the password.

## Summary
Introduces Local File Inclusion (LFI) vulnerability.
