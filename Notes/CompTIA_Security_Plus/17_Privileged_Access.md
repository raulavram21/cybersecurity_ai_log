# Privileged Access

## Overview

Users should only have the access they need. Privileged access is the level beyond what normal users have, and it carries higher risk for both the organization and the user holding it.

## Privileged Users

Privileged users are typically system administrators, network administrators, and security administrators.

> **Analogy:** A normal user has a key to their own office. A privileged user has a master key that opens every office in the building, so it must be used carefully and only when needed.

## Time Bound Access

Privileged permissions are granted for a session and revoked when the user logs out. The clock starts at login and stops at logout.

## Password Vaulting

Password vaulting stores privileged credentials in a secure vault. Users retrieve them when needed rather than knowing them directly, which limits who can see or reuse them.

> **Analogy:** A safe deposit box. The keys stay locked away, and you collect them only for the task in hand.

## Vendor and Third Party Access

Vendors or service providers who work on site need controlled access too.

- **Restricted workstation:** The vendor works from a specific machine in a specific location
- **Single target:** The account can only connect to the one system the vendor needs
- **Time window:** The account is active only during agreed hours, such as 8:00 AM to 4:00 PM, and is disabled after that

> [!IMPORTANT]
> **Exam clue:** Vendor accounts should be limited by system, location, and time. Anything broader is a risk.
