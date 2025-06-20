# AES decryption

This programm was used by me to decrypt a large repository of encrypted pdfs.
It uses a counter initialized at 1.

# Use case

The decryption of the documents via the method they were encrypted with a Simplecrypt fork (Python based) and was super slow.
The vast ammount of pdfs which I needed to decrypt accumulated over the years.
In totals it should have taken more than 100 hours using the Python tool so I figured why not port the algo to GO.

In the code you can find functions to encrypt and decrypt files using AES-256 with a xor-keystream and counter initialized at 1, pbkdf2 for key expansion and signing is done using HMAC.

There is also some unrelated stuff in there like generating paths etc. The main functionality is in encrypt/decrypt.
