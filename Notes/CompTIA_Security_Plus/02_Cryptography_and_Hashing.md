Cryptography: The process of transforming information into a form that unintended readers cannot understand.
Context: Relies on complex mathematical algorithms to provide data confidentiality and integrity across networks, systems, and storage.

Hashing: A unidirectional cryptographic process that converts input data of arbitrary size into a fixed-length string (digest).
Context: Operates strictly as a one-way street where data can be hashed, but mathematically cannot be de-hashed or reversed back to its original form.

Encryption: A bidirectional cryptographic process that converts readable data (plaintext) into an unreadable format (ciphertext) using a key.
Context: Operates as a two-way street where authorized parties can encrypt plaintext and subsequently decrypt ciphertext back to plaintext using the appropriate key.

Decryption: The mathematical reversal of encryption that restores ciphertext back to human-readable or usable plaintext.
Context: Requires possession of the specific authorized cryptographic key to restore the scrambled information.

Encrypted Password Storage (Legacy): The outdated security practice of storing user credentials using two-way encryption algorithms.
Context: Considered a major architectural vulnerability because compromise of the server's central decryption key allows attackers to decrypt every user password back to cleartext.

Modern Password Hashing: The standard practice of passing passwords through one-way hashing algorithms before storing them in authentication databases.
Context: Because hash functions cannot be reversed, an attacker capturing a database dump cannot directly read the raw plaintext credentials.

One-Way Integrity Barrier: The mathematical principle ensuring that hash values cannot be decrypted or converted back to original inputs.
Context: Forces attackers to attempt discovery via trial-and-error guessing (brute force or dictionary attacks) rather than inverting the algorithm.

Salting: The practice of appending a unique, random string of characters to a password input before running it through a hashing algorithm.
Context: Changes the input string entirely, which alters the final digest output and prevents attackers from using pre-computed dictionary tables to reverse credentials.

Rainbow Table: A pre-computed dictionary file containing millions of known plaintext passwords mapped to their corresponding pre-generated hash digests.
Context: Attackers use rainbow tables to perform rapid lookup attacks against unsalted hash databases without calculating hashes in real time.

Rainbow Table Defense: The primary operational role of cryptographic salting.
Context: By forcing every password to have a unique salt, identical passwords generate entirely different hash digests, neutralizing the batch lookup efficiency of pre-computed tables.

Authentication Verification Workflow: The programmatic routine executed by a system when a user logs in.
Context: The system prompts for a username and cleartext password, retrieves the user's assigned salt from the database, appends the salt to the input password, and runs the combined string through the hash function.

Digest Comparison: The final step of the authentication check that validates identity without exposing cleartext credentials.
Context: The newly generated digest is compared against the stored digest in the database; if both strings match, access is granted, otherwise authentication is denied.

Hashing Algorithm: A mathematical one-way engine that processes input strings and outputs a fixed-length cryptographic value.
Context: Designed to be collision-resistant and non-reversible, making it computationally infeasible to invert back to the original plaintext.

Hash Digest: The fixed-length collection of letters and numbers generated as the output of a hashing algorithm when plaintext or data is processed.
Context: Appears as a seemingly random alphanumeric string; identical plaintext passed through the same hashing algorithm will always produce the exact same digest.

Hash Collision: A cryptographic vulnerability that occurs when two distinct, different inputs produce the exact same output digest.
Context: Violates the core mathematical assumption of data integrity, where every unique input must map to a unique digital fingerprint.

Broken Hashing Algorithm: A classification given to a hashing algorithm the moment researchers or adversaries prove it is capable of generating collisions.
Context: Once collisions are demonstrated, the algorithm is deprecated and retired from production environments to prevent threat actors from forging legitimate files.

Integrity Verification: The practice of hashing vendor software or files to confirm no unauthorized modifications, insertions, or malware inclusions occurred since the design was finalized.
Context: If the software is completely untampered, hashing the binary will yield the exact vendor-published hash every single time; any alteration shifts the digest entirely.

MD5 (Message Digest 5): A legacy hashing algorithm known to have documented collision vulnerabilities.
Context: Considered structurally broken and obsolete for secure hashing applications, file integrity validation, and credential storage.

SHA-256 (Secure Hash Algorithm 256-bit): A collision-resistant hashing algorithm from the SHA-2 family that produces a fixed 256-bit output digest.
Context: The current industry standard across enterprise platforms, software deployment verification pipelines, and modern security protocols.

SHA-512 (Secure Hash Algorithm 512-bit): An extended hashing algorithm from the SHA-2 family that produces an output digest twice as long as SHA-256 (512 bits).
Context: Used for high-capacity security architectures and long-term future-proofing where maximum digest length and resistance against pre-computation attacks are required.
