### Security Control Types
Security controls protect organizations from various vulnerabilities. They are categorized by how they handle threats:

*   **Deterrent Controls:** Designed to discourage malicious actors from attempting an attack. They don't stop the action, but serve as a warning.
    *   *(Context: Warning signs, banners like "No Parking" or "No Trespassing".)*
*   **Preventative Controls:** Designed to physically or technically stop an unauthorized action from happening in the first place.
    *   *(Context: Locking doors, fencing, computer logins, user training to prevent social engineering.)*
*   **Detective Controls:** Designed to identify and record that an attack or unauthorized event has occurred, allowing you to "play detective" after the fact.
    *   *(Context: Security cameras, door alarms, checksums, Intrusion Detection Systems (IDS).)*
*   **Corrective Controls:** Designed to mitigate a materialized risk and restore systems back to their original, secure state after an incident.
    *   *(Context: Restoring lost or encrypted data from backups after a ransomware attack.)*
*   **Compensating Controls:** Designed to serve as a backup or bridge a coverage gap when a primary security control has shortcomings or cannot provide sufficient protection on its own.
    *   *(Context: Implementing Multi-Factor Authentication (MFA) to compensate for users creating weak passwords.)*
*   **Directive Controls:** Designed to enforce rules of behavior and specify how individuals should interact with a system or facility.
    *   *(Context: Corporate policies, Standard Operating Procedures (SOPs), disciplinary procedures.)*

---

### Identity and Access Management (IAM)
The core framework for managing user access, often referred to as IAAA (or just AAA):

*   **Identification (I):** Stating your identity. It is simply who you claim to be to the system.
    *   *(Context: A username or user ID number.)*
*   **Authentication (A):** Proving your identity. Validating that you are who you claim to be.
    *   *(Context: Passwords, PIN numbers, or Multi-Factor Authentication (MFA).)*
*   **Authorization (A):** Gaining access. Determining what resources (files, folders, computers) you are allowed to use once your identity is proven.
    *   *(Context: Granting access strictly based on assigned roles and least-privilege boundaries.)*
*   **Accounting (A):** Keeping track. Logging and recording who has authenticated and what actions they took while logged in.
    *   *(Context: Maintaining audit trails for monitoring, compliance, and incident forensics.)*

---

### The 3 States of Data
Data within an organization exists in one of three states, each requiring different protection methods:

*   **Data-in-Transit (Data-in-Motion):** Any data currently being sent across a network or transmitted over a distance.
    *   *(Context: Protected using transport encryption protocols such as TLS/HTTPS or VPN tunnels.)*
*   **Data-at-Rest:** Any data currently being stored.
    *   *(Context: Protected primarily via cryptographic file and disk encryption on hard drives, databases, or backup media.)*
*   **Data-in-Use:** Any data being actively processed, read, or updated by a system or application.
    *   *(Context: Resides in system memory/RAM or CPU registers while being computed.)*

---

### Zero Trust Framework
A modern security model focused on removing inherent trust from networks, systems, and users.

*   **Core Principle:** "Never trust, always verify."
    *   *(Context: Replaces traditional perimeter-based security where internal network traffic was implicitly trusted.)*
*   **No Implicit Trust:** Access and trust are not automatically granted based on a user's physical or network location.
    *   *(Context: Plugging a laptop directly into an internal corporate network does not grant automatic access.)*
*   **Continuous Validation:** Requires strictly verifying and validating trust at every single step of a digital interaction, regardless of where the request originates.
    *   *(Context: Continuously assesses device health, user identity, and session telemetry across every resource boundary.)*
