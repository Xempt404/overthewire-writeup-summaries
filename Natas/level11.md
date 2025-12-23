# Natas Level 11

## Steps
1. Opened the level page in the browser.
2. Found that user data is stored in a data cookie, which is JSON encoded, XOR encrypted with a repeating key, then base64 encoded.
3. Observed the default plaintext stored in the cookie `{"showpassword":"no","bgcolor":"#ffffff"}`.
4. Base64‑decoded the cookie and XORed it with the known plaintext to recover the repeating XOR key.
5. Crafted a new plaintext with showpassword set to yes `{"showpassword":"yes","bgcolor":"#ffffff"}`.
6. XORed the new plaintext with the recovered key and base64‑encoded the result.
7. Replaced the data cookie with the forged value and reloaded the page.
8. Retrieved password.

## Summary
Introduces XOR encryption.
