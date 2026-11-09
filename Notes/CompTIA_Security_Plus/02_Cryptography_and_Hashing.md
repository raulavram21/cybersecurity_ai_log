Cryptography: One of the main security controls used to protect information online by transforming data into a form that unintended recipients cannot understand.


    Operates as a two-step process involving encryption to encode cleartext and decryption to decode ciphertext, directly safeguarding data privacy, confidentiality, and integrity against traffic sniffing.

Algorithm: A structured set of mathematical rules or logic designed to solve a technical problem.

  Cipher: A specialized cryptographic algorithm used to actively encode or encrypt information.

  Caesar's Cipher: A simple historical substitution algorithm that works by shifting letters in the alphabet forward by a fixed number of spaces.

For example, an algorithm with a shift of 3 converts 'A' into 'D'. Because alphabets have limited characters, it remains highly vulnerable to rapid trial-and-error brute force attacks.

Cryptographic Key: A distinct functional mechanism used by an encryption algorithm to lock cleartext data or decrypt ciphertext.

Modern technical security relies entirely on keeping the key secure, rather than trying to hide the open design of the algorithm itself.

Symmetric Encryption: A cryptographic approach that involves the use of a single secret key to both encrypt and decrypt shared information.

Senders and receivers must securely share the exact same key beforehand. It offers exceptionally fast computing speeds but introduces a major key-management vulnerability if an attacker intercepts the key during distribution.

Asymmetric Encryption: A cryptographic framework that utilizes a public and private key pair for the encryption and decryption of data.

The public key is openly shared to encrypt data into a secure container, while only the authorized recipient holds the corresponding private key required to unlock it, completely neutralizing the key-sharing dilemma.

Key Length: The total size of a cryptographic key measured in digital bits, where longer key lengths mean more possibilities that an attacker needs to try to break a system.

Longer keys directly insulate ciphers against brute force attacks but demand slower computer processing times, creating a balancing act between data velocity and secure asset protection.

Triple DES (3DES): A symmetric block cipher algorithm that converts plaintext into ciphertext blocks by applying the historic Data Encryption Standard (DES) cipher three separate times using three different 56-bit keys.

Generates an effective key length of 168 bits. It is currently being phased out due to structural data capacity limits but remains in active deployment to maintain backwards compatibility.

Advanced Encryption Standard (AES): One of the most secure symmetric cryptographic algorithms today, generating highly robust keys that are 128, 192, or 256 bits in length.

Keys of this magnitude are entirely safe from brute force attacks; breaking a 128-bit AES key would take a modern computer billions of years to compute.

Rivest Shamir Adleman (RSA): One of the first asymmetric algorithms that produces a mathematically linked public and private key pair, scaling to key sizes of 1,024, 2,048, or 4,096 bits.

Employs massively long key lengths to isolate and protect highly sensitive data transformations and corporate authorization transactions.

Digital Signature Algorithm (DSA): A standard asymmetric algorithm introduced by NIST that generates key lengths of 2,048 bits.

Deployed heavily across public networks as a foundational technical complement to RSA within public key infrastructure environments.

OpenSSL: An open-source command-line tool commonly used by endpoints to generate public/private key pairs and verify active digital certificates.

In 2014, a massive memory-exposure vulnerability known as the Heartbleed bug was disclosed in OpenSSL, emphasizing why defenders must patch assets and enforce up-to-date software updates.

Kerckhoff's Principle: A core cryptographic design rule stating that a system must remain completely secure even if all the operational details of an algorithm are public knowledge, provided the secret private key remains hidden.

True security depends on the secrecy of the key, not the algorithm. Relying on an algorithm's obscurity fails because custom, hidden ciphers are historically cracked once exposed.

Public Key Infrastructure (PKI): An encryption framework that completely automates and secures the exchange of online information by establishing digital trust across computer networks.

PKI eliminates the manual key-sharing vulnerability by authenticating endpoint public keys through a decentralized system of verified digital certificates.

Digital Certificate: A cryptographically signed file issued by a trusted third-party authority that validates and verifies the true identity of a public key holder.

Browsers check these files to confirm a website's public key is authentic, preventing on-path threat actors from substituting spoofed data-capture boxes.

Hash Function: A mathematical algorithm that takes an input string and produces a unique, fixed-length digital fingerprint or code that cannot be decrypted or reversed.

Used to verify data integrity and secure data-at-rest. If so much as one line of code or text character is altered in the original file, it will produce a completely different hash value, instantly flagging unauthorized manipulation.

Hash Collision: A cryptographic vulnerability that occurs when two completely different data inputs pass through a hash function and accidentally output the exact same signature code.

Threat actors exploit collisions to bypass code checks—such as generating malware that matches a trusted software hash. Legacy algorithms like MD5 are retired due to collision flaws.

Secure Hashing Algorithms (SHAs): A family of NIST-approved hash functions (comprising SHA-1, SHA-224, SHA-256, SHA-384, and SHA-512) engineered to maintain advanced collision resistance.

Numbers indicate the size of the digest value in bits. SHA-1 generates a 160-bit digest but is no longer recommended for high-security applications due to legacy collision risks.

Database Storage Hardening: The defensive practice of mapping usernames to un-reversible cryptographic hash values within authentication databases instead of storing passwords in vulnerable cleartext formats.

If an adversary breaches the password database, they capture non-invertible digests rather than usable cleartext strings, protecting credentials from lateral exploitation.

Rainbow Table Attack: A specialized dictionary exploit where an attacker uses a pre-generated file of known plaintext strings and their associated hash values to instantly compromise stolen databases.

If an attacker steals a hashed password log, they run an automated script to map the database strings against the rainbow table dictionary to reverse weak passwords instantly.

Salting: An additional safeguard used to strengthen hash functions by appending a completely unique, random string of characters to user plaintext data before it is hashed.

Distorts the final digest signature, making identical cleartext entries completely distinct. This renders standard pre-compiled rainbow tables entirely useless and forces attackers to calculate individual hashes manually.
