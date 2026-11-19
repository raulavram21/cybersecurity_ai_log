# Intrusion Detection and Prevention Systems (IDS and IPS)

## Overview

Detecting suspicious or malicious activity is vital to an organization's security. Intrusion detection systems (IDS) and intrusion prevention systems (IPS) watch network traffic for threats. The key difference is what they do when they find one.

> **Analogy:** A security camera system watches the building and raises an alarm when something looks wrong. A security guard who sees a break in does more than report it, and steps in to stop it.

## IDS vs IPS

| System | Position | Response | Analogy |
|---|---|---|---|
| **IDS** | Outside the data stream, monitoring a copy of traffic | Detects and alerts, but does not stop the traffic | A camera watching from a distance |
| **IPS** | Inline, so all traffic passes through it | Detects and actively blocks or corrects the threat | A guard who stops the intruder |

> [!IMPORTANT]
> **Exam clue:** An IDS detects and alerts. An IPS detects and acts. If a question describes a system that blocks threats in real time, it is an IPS.

## Network and Host Variants

- **Network IDS (NIDS):** Monitors traffic across a network segment. In the typical placement, it sits behind the firewall and watches traffic reaching the servers and hosts
- **Network IPS (NIPS):** The inline version, placed where it can block traffic before it reaches the hosts
- **Host-based IDS (HIDS):** Installed on a single device, monitoring its logs, files, and activity
- **Host-based IPS (HIPS):** Installed on a device, blocking malicious activity on that device

## Detection Methods (Extra Context)

| Method | How it works | Weakness |
|---|---|---|
| **Signature based** | Compares traffic against a database of known attack patterns | Cannot detect new attacks that have no signature |
| **Anomaly based** | Learns normal behaviour and flags deviations | Can produce false positives when normal behaviour changes |

## Tuning and False Results (Extra Context)

- **False positive:** A harmless event flagged as an attack
- **False negative:** A real attack that goes unnoticed

> [!WARNING]
> **Balancing an IPS:** An overly aggressive IPS may block legitimate users, causing outages, while a lenient one may miss attacks. Tune it carefully and review its alerts regularly.
