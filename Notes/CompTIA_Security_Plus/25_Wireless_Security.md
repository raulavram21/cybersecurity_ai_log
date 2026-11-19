# Wireless Security

## Overview

Wireless signals travel through the air, so anyone within range can receive them. Wireless security protocols encrypt that traffic and control who can join the network.

> **Analogy:** A wired network is a private conversation in a closed room. A wireless network is the same conversation held in an open field, so it needs a code that only the right listeners understand.

## Protocol Evolution

| Protocol | Status | Key point |
|---|---|---|
| **WEP** (Wired Equivalent Privacy) | Broken and obsolete | Aimed to give wireless the privacy of a wired network, but has cryptographic flaws that make it easy to break |
| **WPA** (Wi-Fi Protected Access) | Replaced | Introduced to replace WEP |
| **WPA2** | Widely used, but being phased out | Uses AES encryption with the CCMP protocol |
| **WPA3** | Current standard | Adds stronger protections and easier secure joining, such as QR code connection |

> [!WARNING]
> **Exam clue:** WEP is the insecure one. WPA2 is built from AES and CCMP, and the exam may give you two of the three components and ask for the third.

## Remembering AES and CCMP

The video uses a memory aid: "entertaining system equals a computer". The first letters of "entertaining system" give AES, and "equals a computer" gives CCMP.

## Authentication Modes

| Mode | Used by | How it works |
|---|---|---|
| **Personal (PSK)** | Home and small offices | Everyone shares one pre-shared key (PSK) |
| **Enterprise** | Organizations | Each user authenticates with their own credentials, usually through an authentication server |

> [!IMPORTANT]
> **Exam clue:** PSK means one shared password for everyone. Enterprise modes give each user separate credentials, so they suit organizations where one shared password is a risk.

> **Analogy:** Personal mode is a single key to the office that everyone shares. Enterprise mode gives each employee their own key card, which can be revoked individually when someone leaves.

## Site Survey

A site survey measures wireless activity across an office to plan coverage. Surveyors walk the space while recording signal strength.

- **Heat map:** A visual map showing where coverage is strong, weak, or missing
- **Gaps:** Areas with weak coverage show where another access point or a repositioned one is needed
