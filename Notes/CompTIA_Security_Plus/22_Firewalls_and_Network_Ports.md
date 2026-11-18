# Firewalls and Network Ports

## Overview

A firewall filters traffic between networks or devices based on a set of rules. Firewall rules usually refer to network ports, which identify the service a connection is trying to reach.

## Firewall Types

| Type | Where it sits | What it does |
|---|---|---|
| **Network firewall** | At the network edge | Filters traffic between the internet and the internal network |
| **Host-based firewall** | On a single device | Monitors and controls that device's incoming and outgoing traffic |
| **Web application firewall (WAF)** | In front of a web application | Looks for injection attacks, cross site scripting, and embedded malicious requests |
| **Next-generation firewall (NGFW)** | At the network edge | Has built in logic to identify the type of traffic, not just its address or port |

> **Analogy:** A network firewall is a building's main security desk. A host-based firewall is a lock on each individual office, so a threat that gets past the desk is still stopped at the door.

> [!IMPORTANT]
> **Why host-based firewalls:** A network firewall protects the perimeter. A host-based firewall protects each device, including traffic moving between devices inside the network.

## Firewall Rules

Rules are read from top to bottom, and the first matching rule applies. A typical rule includes:

- Source IP address
- Destination IP address
- Source port number
- Destination port number
- Protocol, either TCP or UDP

### Example Rule Set

| # | Source | Destination | Protocol | Port | Access |
|---|---|---|---|---|---|
| 1 | 192.168.0.64 | ANY | TCP/UDP | 22, 3389 | ALLOW |
| 2 | ANY | 192.168.0.32 | TCP | 80, 443 | ALLOW |
| 3 | ANY | ANY | ANY | ANY | DENY |

> [!IMPORTANT]
> **Implicit deny:** The final rule denies everything not explicitly allowed above it. This is the safe default, so any traffic you did not plan for is blocked.

> **Analogy:** A guest list at a club, read from the top. Anyone on an earlier line gets in, and anyone not matched on any line is turned away at the end.

## Common Ports and Protocols

| Name | Port | Purpose |
|---|---|---|
| **HTTP** | 80 | Web traffic from client to server, unencrypted |
| **HTTPS** | 443 | Same as HTTP, but encrypted with TLS |
| **FTP** | 21 | Transfers files, unencrypted, so it is largely no longer used |
| **SSH** | 22 | Encrypted command line access to a remote system |
| **Telnet** | 23 | Unencrypted command line access to a remote system |
| **SMTP** | 25 | Transports mail from sender to the receiver's mail server |
| **DNS** | 53 | Looks up IP addresses, hostnames, and services for a domain |
| **RDP** | 3389 | Encrypted graphical remote desktop access |

> [!WARNING]
> **Plaintext protocols:** FTP and Telnet send everything unencrypted, so anyone on the path can read credentials and data. Their encrypted replacements are SFTP and SSH.

> **Analogy:** Sending a postcard versus a sealed envelope. Anyone handling a postcard can read it, which is the risk with plaintext protocols.
