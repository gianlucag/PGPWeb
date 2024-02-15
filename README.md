# PGPWeb

A pure JavaScript single-page application designed to encrypt and decrypt PGP ASCII-armored messages directly within the browser.

## Rationale behind PGPWeb

Many PGP programs are tightly integrated with email clients, limiting users to specific mail clients for managing PGP messages. PGPWeb, however, is a standalone webpage solely focused on encrypting and decrypting PGP messages. It does not handle email functionalities. Users can easily copy and paste messages between their preferred mail client (or any other program) and PGPWeb.

## How to Use PGPWeb

Simply double click on `pgpweb.html`, copy and paste your PGP credentials (which are stored locally and never leave your device), then either encrypt a message using a recipient's public key or decrypt a message intended for you using your registered PGP private key.

## Key Formats

PGPWeb exclusively accepts ASCII-armored PGP keys. Here's an example of a public key:

```
-----BEGIN PGP PUBLIC KEY BLOCK-----

mQINBGTCe3UBEADCKrG4LdNAROF4EpHQSqlQom88WxFaJjgBPgbFgHHRN8M7VGnA
pVoJTBtKFGq1n8vK9c8tYm5pcwtf11rvutDmcwMYF1mS7em7vha3/eJs14iWv2ku
...
lJrBTVT+l5OYFBGLyDSHlk1bcUWbu/Zbzo3B5EXEsWcEJylDqIXyTRpvlqqvFtYr
FwmCfhAj4+Rz6JJRKLo2eyI3H8yX5l3FLgR5kyPuSI09Dssp8obKpi5Bcg==
=YpDI
-----END PGP PUBLIC KEY BLOCK-----
```

## Message Formats

PGPWeb exclusively handles ASCII-armored PGP messages, using the same format as the keys.

## Security

PGPWeb securely stores public and private PGP keys in the local storage area of the browser, ensuring keys never leave the device. The private key passphrase is not stored and must be entered manually when decrypting a PGP message.

## Future Improvements

- Signing and verifying functionalities are currently absent.
- Exploration of handling binary files (such as local file upload), not limited to ASCII messages.
- Copy&paste buttons on the textareas
