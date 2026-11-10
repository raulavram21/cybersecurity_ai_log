## Security Control Types

Security controls protect organizations from vulnerabilities. They are grouped by how they handle threats.

| Control Type | Purpose | Examples |
|---|---|---|
| **Deterrent** | Discourage attackers. Warns rather than stops the action. | Warning signs, "No Trespassing" banners |
| **Preventative** | Stop an unauthorized action before it happens. | Locked doors, fencing, computer logins, social engineering training |
| **Detective** | Identify and record that an attack or unauthorized event occurred. | Security cameras, door alarms, checksums, Intrusion Detection Systems (IDS) |
| **Corrective** | Mitigate a materialized risk and restore systems to a secure state. | Restoring encrypted data from backups after ransomware |
| **Compensating** | Act as a backup or bridge a gap when a primary control falls short. | Multi-Factor Authentication (MFA) to offset weak passwords |
| **Directive** | Enforce rules of behavior and how people should use a system or facility. | Corporate policies, Standard Operating Procedures (SOPs), disciplinary procedures |

> **Analogy:** A house with a "Beware of Dog" sign (deterrent), a locked door (preventative), a camera (detective), an insurance payout and rebuild (corrective), a guard dog when the door lock is weak (compensating), and house rules for visitors (directive).

## Identity and Access Management (IAM)

The core framework for managing user access, often referred to as **IAAA** (or just **AAA**).

| Step | Meaning | Context |
|---|---|---|
| **Identification (I)** | Stating who you claim to be. | Username or user ID number |
| **Authentication (A)** | Proving you are who you claim to be. | Passwords, PIN numbers, MFA |
| **Authorization (A)** | Determining what you can access once your identity is proven. | Files, folders, computers |
| **Accounting (A)** | Logging who authenticated and what they did while logged in. | Audit logs |

> **Analogy:** Airport security. You show your name on a ticket (identification), show your passport (authentication), get a boarding pass for a specific gate (authorization), and your movements are logged (accounting).

## The 3 States of Data

Data exists in one of three states, and each needs different protection.

| State | Description | Context |
|---|---|---|
| **Data-in-Transit** (Data-in-Motion) | Data being sent across a network or over a distance. | Emails, web traffic |
| **Data-at-Rest** | Data being stored. Generally protected via encryption. | Hard drives, memory, databases, backup tapes |
| **Data-in-Use** | Data being actively processed, read, or updated. | Applications and systems working on data |

> **Analogy:** A letter in the post (in transit), a letter in a filing cabinet (at rest), and someone reading or editing it at a desk (in use).

## Zero Trust Framework

A modern security model that removes inherent trust from networks, systems, and users.

> [!IMPORTANT]
> **Core principle:** "Never trust, always verify."

- **No Implicit Trust:** Access is not granted automatically based on physical location (being inside the building) or network location (plugging into the internal network).
- **Continuous Validation:** Trust is verified at every step of a digital interaction, regardless of where the request comes from.

> **Analogy:** A building where every door checks your badge, even for people already inside the lobby.
