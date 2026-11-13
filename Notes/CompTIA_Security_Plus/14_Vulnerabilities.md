# Vulnerabilities

## Overview

A vulnerability is a weakness that an attacker can exploit. Organizations handle them differently, but Security+ expects you to recognise the common terms and the situations they describe.

## Zero Day

A zero day is a vulnerability that nobody has seen before, so no fix or existing defence is known.

> **Analogy:** A lock that has a flaw nobody has discovered yet. There is no key, patch, or warning, so you find out only when someone uses it.

## Misconfiguration

A misconfiguration is when a system or part of a system is set up incorrectly and leaves it open to attack.

- **Error handling:** Showing detailed error messages to users can leak information, such as system details, that helps an attacker

> **Analogy:** Leaving a spare key under the doormat, or a note on the door explaining exactly how the alarm works.

## Operating System and Driver Vulnerabilities

- **Drivers:** Software that translates signals between the operating system and hardware
- **Malicious drivers:** Protected through code signing and other controls, but a malicious driver is still an operating system vulnerability

> [!IMPORTANT]
> **Physical access:** If an attacker has physical access to a system, many other controls can be bypassed. Control physical access, and restrict removable media such as USB drives and media converters.

## Supply Chain Vulnerabilities

Weaknesses introduced through vendors, suppliers, or third party components that your organization depends on.

> **Analogy:** A bank can have perfect vault doors, but if the company that delivers its cash has weak security, that becomes the way in.

## Cryptographic Vulnerabilities

Weaknesses in the cryptography itself. An example is creating malware that produces the same MD5 hash as a legitimate executable, which lets it pass integrity checks.

> [!WARNING]
> **Retired algorithm:** MD5 is no longer secure against collisions. Do not rely on it for integrity checks.

## Mobile Device Vulnerabilities

- **Third party app stores:** Apps from unofficial sources may be untrusted or malicious
- **Side loading:** Installing an app directly onto a device, bypassing the official app store. Developers use it for testing, but it also lets unvetted apps onto a device
- **Jailbreaking (and rooting):** Gaining root level access on a device to unlock restricted features. It can disable security controls, including mobile device management (MDM) software

> **Analogy:** Side loading is like inviting a stranger into a building through a side door, bypassing the security desk.
