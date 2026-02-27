# 🔐 Password Manager

A simple, local, encrypted command-line password manager written in Python.

## Features

- AES-256 encryption (via `cryptography` library / Fernet)
- Master password with PBKDF2-HMAC-SHA256 key derivation (480,000 iterations)
- Add, retrieve, update, and delete entries
- Random secure password generator
- Change master password at any time
- Everything stored locally in a single `vault.enc` file

## Requirements

- Python 3.8+
- `cryptography` library

```bash
pip install cryptography
```

## Usage

```bash
python password_manager.py
```

On first run, you'll be prompted to create a master password. After that, a `vault.enc` file is created in the same directory.

## ⚠️ Security Notes

- **Don't lose your master password** — there is no recovery mechanism.
- **Back up `vault.enc`** — deleting it loses all passwords.
- **Add `vault.enc` to your `.gitignore`** — never commit it to a public repo.
- The vault file is encrypted and safe to store, but keep your master password secret.

## .gitignore

Make sure your `.gitignore` includes:

```
vault.enc
```

## License

MIT
