# 02 Cryptography and Hashing

## Cryptography Fundamentals

Cryptography is a main security control. It transforms data into a form that unintended recipients cannot understand, protecting privacy, confidentiality, and integrity against traffic sniffing.

| Term | Meaning | Context |
|---|---|---|
| **Encryption** | Encodes cleartext into ciphertext. | Locking data |
| **Decryption** | Decodes ciphertext back into cleartext. | Unlocking data |
| **Algorithm** | A structured set of mathematical rules or logic that solves a technical problem. | The lock design |
| **Cipher** | A specialized cryptographic algorithm used to encode or encrypt information. | A specific lock design |
| **Cryptographic Key** | The mechanism an algorithm uses to lock or unlock data. | The physical key |

> **Analogy:** The algorithm is the lock design, and the key is what opens it. Security depends on keeping the key secret, not the lock design.

**Caesar's Cipher:** A simple historical substitution cipher that shifts letters forward by a fixed number. A shift of 3 turns 'A' into 'D'. With only 26 letters, it is easy to crack by trying every shift (brute force).

> [!IMPORTANT]
> **Kerckhoff's Principle:** A system must stay secure even if everything about the algorithm is public, as long as the private key stays hidden. Hidden custom ciphers have historically been cracked once exposed.

## Encryption Types

| Type | How it works | Strengths | Weaknesses |
|---|---|---|---|
| **Symmetric** | One secret key both encrypts and decrypts. | Very fast | Sender and receiver must share the key beforehand, so an attacker who intercepts it breaks the system |
| **Asymmetric** | A public key encrypts, and only the matching private key decrypts. | Solves the key sharing problem | Slower than symmetric |

> [!IMPORTANT]
> **Symmetric vs Asymmetric:** Symmetric uses one shared key, while asymmetric uses a public and private key pair. Questions often hinge on the key sharing problem, which only asymmetric solves.

> **Analogy:** Symmetric is a shared house key, where everyone needs a copy. Asymmetric is a mailbox with a public slot: anyone can post a letter, but only the owner holds the key to open it.

## Key Length and Algorithms

**Key Length:** The size of a key in bits. Longer keys mean more possibilities an attacker must try, which resists brute force but slows processing. This is a balance between speed and protection.

| Algorithm | Type | Key Length | Notes |
|---|---|---|---|
| **Triple DES (3DES)** | Symmetric block cipher | Effective 168 bits | Applies the older DES cipher three times with three 56 bit keys. Being phased out due to data capacity limits, but kept for backwards compatibility. |
| **AES** | Symmetric | 128, 192, or 256 bits | Highly secure. A 128 bit key would take a modern computer billions of years to brute force. |
| **RSA** | Asymmetric | 1,024, 2,048, or 4,096 bits | One of the first asymmetric algorithms. Used to protect highly sensitive data and transactions. |
| **DSA** | Asymmetric | 2,048 bits | Introduced by NIST. Works alongside RSA in public key infrastructure. |

> **Analogy:** Key length is like the number of combinations on a padlock. Each extra digit multiplies the attempts a thief needs.

## Public Key Infrastructure (PKI)

**PKI:** A framework that automates and secures the exchange of information by establishing digital trust across networks. It removes the manual key sharing problem by verifying public keys through digital certificates.

**Digital Certificate:** A signed file issued by a trusted third party that verifies the identity of a public key holder. Browsers check it to confirm a website is genuine and not a spoofed copy sitting on the path between you and the server.

**OpenSSL:** An open source command line tool used to generate key pairs and verify certificates.

> [!WARNING]
> **Heartbleed (2014):** A memory exposure vulnerability in OpenSSL. It shows why patching and keeping software up to date matters.

> **Analogy:** A certificate is like a passport issued by a government. Your browser trusts the issuer, so it trusts the identity printed on the document.

## Hashing

**Hash Function:** Takes an input and produces a unique, fixed length fingerprint that cannot be reversed. Used for data integrity and protecting data at rest. Changing one character produces a completely different hash, which flags tampering immediately.

**Hash Collision:** When two different inputs produce the same hash. Attackers exploit collisions to make malware match a trusted software hash. MD5 is retired because of collision flaws.

**Secure Hashing Algorithms (SHAs):** A NIST approved family (SHA 1, 224, 256, 384, 512). The number is the digest size in bits. SHA 1 is no longer recommended for high security use.

> [!IMPORTANT]
> **Encryption vs Hashing:** Encryption is reversible with the right key, so data can be recovered. Hashing is one way, so the original data cannot be recovered from the hash.

| Concept | What it is | Why it matters |
|---|---|---|
| **Database Storage Hardening** | Storing hashes of passwords instead of cleartext. | A stolen database yields digests, not usable passwords |
| **Rainbow Table Attack** | A dictionary of pre computed plaintext and hash pairs. | Lets attackers reverse weak hashed passwords instantly |
| **Salting** | Adding a unique random string to each password before hashing. | Makes identical passwords produce different hashes, so pre computed tables are useless |

> [!IMPORTANT]
> **Hash vs Salt:** A hash is the one way output itself. A salt is a random value added before hashing, so identical passwords produce different hashes.

> **Analogy:** Salting is like adding a unique secret ingredient to each dish. Someone with a cookbook of pre made dishes can no longer match yours.

> **Real world:** In 2012, LinkedIn suffered a breach in which millions of unsalted password hashes were leaked, and many were later cracked. It shows why salting matters.
