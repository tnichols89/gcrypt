# gcrypt
This project is a small encryption application that encrypts and decrypts files using the 256-bit AES block cipher for encryption, PBKDF2 for key stretching and derivation, and HMAC-SHA512 (over the ciphertext, KDF salt, and initialization vector) for file integrity and authenticity checking.

## To compile:
    $ gcc encrypt_decrypt.c -o encrypt_decrypt -lgcrypt

## Usage:
    $ ./encrypt_decrypt [encrypt|decrypt] <input file path> <output file path> <some-super-strong-password>

## Pitfalls:
Inefficient use of memory. All data to be encrypted/decrypted is loaded into memory prior to processing instead of reading and processing a file chunk-by-chunk.
