Encryption Methods


Foundational Cryptography

    Cryptography: One of the main security controls used to protect information online by transforming data into a form that unintended readers cannot understand.
    (Context: Operates as a two-step process: encryption to hide cleartext into ciphertext, and decryption to restore it. It directly preserves data confidentiality and integrity against network sniffing.)

    Algorithm: A structured set of mathematical rules or logic used to solve a problem.

    Cipher: An algorithm used to actively encrypt or encode information.

    Caesar's Cipher: A simple historical substitution algorithm that works by shifting alphabet letters forward by a fixed number of spaces.
    (Context: For example, an algorithm with a shift of 3 transforms 'A' into 'D'. Because alphabets have limited characters, an adversary can easily execute a trial-and-error brute force attack to test all possibilities and crack the cipher.)

    Cryptographic Key: A distinct functional mechanism used by an algorithm to decrypt ciphertext.

Symmetric vs. Asymmetric Architectures

    Symmetric Encryption: A cryptographic model that involves the use of a single secret key to both encrypt and decrypt shared information.
    (Context: Senders and receivers must securely share the exact same key to lock or unlock the data. It offers fast processing speeds but introduces key-management risks, as intercepting the single key compromises the entire connection.)

    Asymmetric Encryption: A cryptographic model that utilizes a mathematically linked public and private key pair for the encryption and decryption of data.
    (Context: The public key is distributed openly to encrypt/lock data, while the corresponding private key remains closely guarded by the authorized recipient to decrypt/unlock it. This eliminates the key-sharing dilemma but demands longer keys and slower processing times.)

    Key Length and Trade-offs: Cryptographic bits represent the smallest unit of computer data measurement. Longer key lengths increase the mathematical possibilities an attacker must try during a brute force attack, significantly strengthening security. However, longer keys slow down compute speed, creating a delicate optimization balancing act for security analysts.

    Hybrid Implementation: Modern communication platforms merge both categories. Mobile chat applications use secure asymmetric encryption to safely exchange keys at the start of a session, then switch to fast symmetric encryption to stream user data efficiently.

Approved Cryptographic Algorithms

    Triple DES (3DES): A symmetric block cipher that processes plaintext in blocks. It applies the historical Data Encryption Standard (DES) algorithm three separate times using three different 56-bit keys. It is currently being phased out due to structural data capacity limits but remains relevant for backwards compatibility. Effective key length of 168 bits.

    Advanced Encryption Standard (AES): One of the most secure symmetric ciphers today. Generates keys that are 128, 192, or 256 bits. Keys of this magnitude are considered entirely safe from brute force attacks; testing a 128-bit AES key would require modern hardware billions of years to break.

    Rivest Shamir Adleman (RSA): One of the first asymmetric encryption algorithms to produce a public/private key pair. It generates exceptionally long key sizes of 1,024, 2,048, or 4,096 bits to protect highly sensitive enterprise data transactions.

    Digital Signature Algorithm (DSA): A standard asymmetric protocol introduced by NIST in the early 1990s that generates key lengths of 2,048 bits. It functions as a core structural complement to RSA within public key infrastructure ecosystems.

Practical Key Generation Tools & Vulnerabilities

    OpenSSL: An open-source command-line tool commonly used by systems to generate public/private key pairs and verify digital certificates within a Public Key Infrastructure (PKI).
    (Context: In 2014, OpenSSL disclosed a critical vulnerability known as the Heartbleed bug, which allowed unauthenticated actors to read sensitive data directly from the system memory of unpatched web servers. This historical incident underscores the paramount importance of keeping enterprise software updated.)

Cryptographic Governance Principles

    Kerckhoff's Principle: A core design rule stating that a cryptographic system must remain completely secure even if every detail of the encryption algorithm is public knowledge, provided the secret private key remains hidden.
    (Context: True security depends entirely on the secrecy of the key rather than the secrecy of the system. Trying to protect assets by keeping an algorithm secret violates this rule and relies on obscurity, which frequently leads to catastrophic system cracks once the algorithm is exposed or reverse-engineered.)

Data Integrity & One-Way Hashing

    Hash Function: A mathematical algorithm that takes an input string and produces a unique, fixed-length digital fingerprint or code that is mathematically impossible to reverse or decrypt.
    (Context: Used primarily to verify data integrity and secure data-at-rest. When a file or password is processed, the system stores the resulting hash value. If so much as one character or line of code is altered in the original file, it generates a completely different hash value, exposing manipulation attempts.)

    Hash Collision: A cryptographic vulnerability that occurs when two completely different inputs pass through a hash function and accidentally output the exact same signature code.
    (Context: Threat actors actively exploit collisions to bypass verification controls—for instance, replacing a legitimate software patch with malware that generates a matching signature to evade system defenses. Legacy algorithms like MD5 suffer from documented structural collision faults.)

    Secure Hashing Algorithms (SHAs): A family of NIST-approved algorithms engineered to resist hash collisions by producing longer bits and advanced digests. Except for SHA-1 (which yields a 160-bit digest and is no longer recommended due to collision vulnerabilities), the standard variants remain highly collision-resistant:

    SHA-1 (160 bits)

    SHA-224 (224 bits)

    SHA-256 (256 bits)

    SHA-384 (384 bits)

    SHA-512 (512 bits)

Secure Password Storage & Exploitations

    Database Storage Hardening: Rather than keeping authentication databases in vulnerable cleartext formats, modern databases store user entries as hash values mapped to usernames. When a login request occurs, the system hashes the inbound text and validates it against the stored value before granting access.

    Rainbow Table Attack: A specific dictionary exploit where an attacker uses a pre-compiled file containing millions of known plaintext strings and their associated pre-generated hash values to instantly crack a captured database.
    (Context: If an attacker steals a hashed password directory, they run a script to map the database codes directly against the rainbow dictionary to instantly look up corresponding weak passwords, completely bypassing the one-way barrier.)

    Salting: An additional safeguard used to strengthen hash functions and neutralize dictionary lookups.
    (Context: Enforces uniqueness by adding a random, distinct string of characters to user plaintext before it runs through the hashing algorithm. This forces the function to output a completely non-standard digest value, rendering standard pre-compiled rainbow tables entirely useless and forcing attackers to calculate individual digests manually.)


    git commit -m "study: appended symmetric/asymmetric algorithms, hashing functions, SHA family metrics, rainbow table limits, and salting defenses"

    git push origin main
