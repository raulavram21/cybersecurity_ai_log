# Enterprise Security Controls

## Overview

Enterprise security controls protect data across the whole organization. They include separating networks, limiting what can run, keeping systems patched, encrypting data, and securing remote and email traffic.

## Network Segmentation

Network segmentation divides the corporate network into smaller, manageable pieces. If one segment is compromised, only a small number of users are affected.

> **Analogy:** A ship with watertight compartments. A breach floods one compartment, but the rest of the ship stays afloat.

### VLANs

A virtual local area network (VLAN) separates segments logically on a shared network. At layer 3, where IP addresses live, the network can determine which VLAN an address belongs to.

### Physical Segmentation

Physical segmentation uses separate physical networks. For example, US government and Department of Defense networks use NIPRNet for unclassified traffic and SIPRNet for classified traffic.

### Isolation

Isolation stops an infected device from spreading its communications to other devices on the network.

## Access Control Lists

Application control limits which programs can run on a system.

| Approach | How it works | Trade off |
|---|---|---|
| **Allow list** | Only approved programs can run | Most secure, but needs more maintenance |
| **Block list** | Specific programs are blocked, and everything else can run | More flexible, but blocks only known threats |

> [!IMPORTANT]
> **Exam clue:** An allow list is the more restrictive option. A block list permits more applications because it only limits a small set.

## Patching

Patching keeps systems secure by fixing known vulnerabilities. It is a core part of maintaining security across a corporate network.

## Encryption at Rest

Full disk and file system encryption protects stored files if a device is lost or stolen.

- **BitLocker:** Full disk encryption on Windows
- **FileVault:** Full disk encryption on macOS

## VPN

A virtual private network (VPN) uses encryption to protect data travelling across an open public network.

> **Analogy:** A sealed armoured tunnel through a busy public street, so no one on the street can see what is being carried.

## Email Security

Email is insecure by default when sent over the open Internet. Additional measures are needed to protect its content and sender identity.

## Secure Configuration Guides

Vendors and best practice bodies publish secure configuration guides. Following them reduces the chance of misconfigured systems.
