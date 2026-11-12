# Cryptographic Attacks

## Overview

Adversaries often target protected data by attacking the cryptography itself or the passwords that guard it. Password attacks are the most common form.

## Password Attacks

| Attack | How it works | Key point |
|---|---|---|
| **Brute force** | Tries every possible combination | Simplest method, but very slow |
| **Dictionary** | Cycles through a list of known and previously used passwords | Works well when users reuse passwords |
| **Password spraying** | Tries one common password across many users | Avoids locking out any single account |

> **Analogy:** Brute force is trying every key on a ring. A dictionary attack tries the keys people usually hide under the mat. Password spraying tries one popular key on every door in the building.

## Birthday Attack

A birthday attack uses probability to find a collision faster than expected. In a group of just 23 people, there is a better than even chance two share a birthday, even though there are 365 possible dates.

> **Analogy:** Shrinking a large pool of possibilities to a small group where a match is likely.

Recall that a collision is when two different inputs produce the same hash digest.

## Known Plaintext Attack

The attacker already knows some plaintext and its matching ciphertext, then uses that pair to work out the key. The Enigma machine began to be broken when codebreakers recognised messages that repeated the same content.

> **Analogy:** A crossword where you already know some of the answers, which helps you solve the rest.

## Rainbow Table Attack

A rainbow table is a precomputed list of inputs and their hash values, used to reverse hashed passwords quickly.

> [!IMPORTANT]
> **Rainbow tables need the right system:** The attacker must know which hash function was used to create the stored password. Salting defeats rainbow tables.
