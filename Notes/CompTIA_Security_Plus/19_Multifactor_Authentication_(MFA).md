# Multifactor Authentication

## Overview

Multifactor authentication (MFA) requires a user to prove identity using two or more different factors. Using factors from different categories makes it much harder for an attacker to succeed, even if one factor is stolen.

## Authentication Factors

| Factor | Category | Examples |
|---|---|---|
| **Something you know** | Knowledge | Password, PIN |
| **Something you have** | Possession | Hard token, soft token, smart card, phone |
| **Something you are** | Biometric | Fingerprint, face, iris |
| **Something you do** | Behaviour | Typing rhythm, signature, gait |
| **Somewhere you are** | Location | IP address range, GPS location, office network |

> **Analogy:** A bank vault that needs a key you have, a combination you know, and a fingerprint you are. A thief would need to steal all three.

> [!IMPORTANT]
> **Exam clue:** Two passwords are not multifactor, because both are "something you know". MFA needs factors from different categories.

## Biometrics

Biometrics use a unique physical characteristic of the person, such as a fingerprint or face scan, to verify identity.

## Tokens

Tokens generate or store a unique value that proves possession of a device or credential.

- **Hard token:** A physical device, such as a key fob
- **Soft token:** Software on a phone or computer that generates the code

> **Analogy:** A hard token is a physical key. A soft token is a copy of that key stored on your phone.

### RSA Tokens

An RSA token shows a six digit code that changes regularly. The code is generated from a unique key, so a user must enter the current code to log in.

> [!WARNING]
> **Time sensitive:** Because the code rolls over every short period, a stolen code quickly becomes useless. Users must enter the code that is currently displayed.
