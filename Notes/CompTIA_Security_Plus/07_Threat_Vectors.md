# Threat Vectors

## Overview

A threat vector is the route an attacker uses to reach an organization. Attacks can arrive through messages, files, removable media, vulnerable software, wireless networks, open ports, weak credentials, or suppliers.

## Message-Based Attacks

Attacks delivered through messages that trick the recipient into acting.

| Type | Channel | Example |
|---|---|---|
| **Phishing** | Email | A fake invoice or password reset link |
| **Smishing** | SMS and text messages | A fake parcel delivery alert |
| **Vishing** | Phone calls | A caller pretending to be Microsoft support or the tax authority |

> **Analogy:** A fake delivery driver who knocks on the door with a clipboard, hoping you will open it without checking who they are.

## File-Based Attacks

Malicious content carried inside files.

- **Steganography:** Hiding a file or malware inside another file, such as an image
- **Malware launched by another process:** A hidden payload inside an image that is triggered by something else on the system
- **Fileless malware:** Runs in memory without leaving a file behind, which makes it harder to detect

> **Analogy:** Fileless malware is like a burglar who leaves no fingerprints. The crime still happened, but there is no obvious evidence left to find.

## Removable Media

Mass storage devices, such as USB drives, are used to move data and malware. This is a key risk for air gapped systems, which are isolated from networks and rely on removable media to transfer data.

> [!WARNING]
> **Air gap risk:** An air gap is not absolute. A single infected USB drive can bypass it entirely.

## Software and Systems

- **Vulnerable software:** Unpatched applications that attackers can exploit
- **Unsupported systems:** Legacy systems and applications that no longer receive security updates, sometimes installed on the network without the organization's choice

## Wireless and Network

- **Wireless networks:** Signals travel beyond the building, so anyone nearby can receive them. Intercepting wireless traffic is a common attack.
- **Bluetooth:** Built into most mobile devices and many computers, so it is another wireless entry point.
- **Open network ports:** Unnecessary open ports give attackers a way into systems.

> **Analogy:** A wireless network is like speaking in a room with open windows. Anyone outside can hear the conversation.

## Credentials

- **Weak credentials:** Easy to guess passwords
- **Default credentials:** Factory settings such as "admin" and "admin" that are never changed
- **Well known credentials:** Passwords that appear on public lists and are tried first by attackers

> [!IMPORTANT]
> **Default credentials:** Changing them on installation is one of the simplest ways to close an attack vector.

## Supply Chain

Attacks that come through vendors or suppliers with trusted access to the organization.

> **Analogy:** A burglar who does not break your door but uses a key you gave to your cleaner.
