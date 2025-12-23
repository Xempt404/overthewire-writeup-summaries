# Natas Level 8

## Steps
1. Opened the level page in the browser.
2. Encountered an input field requesting a secret code.
3. Viewed source code and noticed `$encodedSecret = "3d3d516343746d4d6d6c315669563362";` and `bin2hex(strrev(base64_encode($secret)))` being used to verify the input code.
4. Decoded the hexadecimally encoded binary string to `==QcCtmMml1ViV3b` and reversed the string to `b3ViV1lmMmtCcQ==`.
5. Decoded the base64 string into `oubWYf2kBq` and submitted the input code.
6. Access granted and received password. 

## Summary
Introduces base64 encoding, string reversal, and hex encoding.
