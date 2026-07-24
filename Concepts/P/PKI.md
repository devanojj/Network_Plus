#domain/4-0-Network-Security

==**Public Key Infrastructure**==

It is a complete system for the creation, management, storage, distribution, and revocation of digital certificates
- Public/private key pairs
- Certificate revocation mechanisms 

**Digital Certificate:** An electronic document that proves the ownership of a public key. It binds a public key to an identity (like a person or a server).
**[[CA]]**
**RA (Registration Authority):** An entity that verifies the identity of users requesting a certificate from the CA. (Not needed)
**[[CSR]]** (Not needed)
**[[CRL]]** (Not needed)



**Asymmetric encryption** (surface level only) — Uses a key pair: public key encrypts, private key decrypts. What PKI is built on. Slower but solves the key-sharing problem.

**Symmetric encryption** — Uses a **single shared key** to both encrypt and decrypt. Both sender and receiver must have the same key.
- Faster than asymmetric
- Main problem: how do you securely share the key in the first place?

