# Image Encrypter

A Python command-line tool that encrypts and decrypts image files with a password. It uses AES-256 with a key derived from the password (PBKDF2, 100,000 iterations).

## Use it

```sh
pip install cryptography
python ImageEncrypter.py encrypt photo.png
python ImageEncrypter.py decrypt photo_encrypted.png
```

It asks for the password when it runs. The encrypted file is written next to the original with `_encrypted` in the name, and decrypting writes a `_decrypted` copy. The originals are not changed.

## Limitations

This is a learning project. The salt is fixed and the same password produces the same starting state for encryption. There is no check for tampered files or a wrong password. The password is visible while you type it. Do not rely on this tool to protect anything sensitive. Use simple filenames without extra dots in a folder without dots in its path, as the output naming replaces every dot.
