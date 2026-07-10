Security Control Types

Security controls protect organizations from various vulnerabilities. They are categorized by how they handle threats:

Deterrent Controls: Designed to discourage malicious actors from attempting an attack. They don't stop the action, but serve as a warning. Example: Warning signs, banners (e.g., "No Parking" or "No Trespassing").

Preventative Controls: Designed to physically or technically stop an unauthorized action from happening in the first place. Example: Locking doors, fencing, computer logins, user training to prevent social engineering.

Detective Controls: Designed to identify and record that an attack or unauthorized event has occurred, allowing you to "play detective" after the fact. 
Example: Security cameras, door alarms, checksums, Intrusion Detection Systems (IDS).

Corrective Controls: Designed to mitigate a materialized risk and restore systems back to their original, secure state after an incident. Example: Restoring lost or encrypted data from backups after a ransomware attack.

Compensating Controls: Designed to serve as a backup or bridge a coverage gap when a primary security control has shortcomings or cannot provide sufficient protection on its own. Example: Implementing Multi-Factor Authentication (MFA) to compensate for users creating weak passwords.

Directive Controls: Designed to enforce rules of behavior and specify how individuals should interact with a system or facility. Example: Corporate policies, Standard Operating Procedures (SOPs), disciplinary procedures.

Identity and Access Management (IAM)

The core framework for managing user access, often referred to as IAAA (or just AAA):

Identification (I): Stating your identity. It is simply who you claim to be to the system. Example: A username or user ID number.

Authentication (A): Proving your identity. Validating that you are who you claim to be. Example: Passwords, PIN numbers, or Multi-Factor Authentication (MFA).

Authorization (A): Gaining access. Determining what resources (files, folders, computers) you are allowed to use once your identity is proven.

Accounting (A): Keeping track. Logging and recording who has authenticated and what actions they took while logged in.

The 3 States of Data

Data within an organization exists in one of three states, each requiring different protection methods:

Data-in-Transit (or Data-in-Motion): Any data currently being sent across a network or transmitted over a distance.

Data-at-Rest: Any data currently being stored. This is generally protected via encryption. Example: Information saved on a hard drive, in memory, in databases, or on backup tapes.

Data-in-Use: Any data being actively processed, read, or updated by a system or application.

Zero Trust Framework

A modern security model focused on removing inherent trust from networks, systems, and users.

Core Principle: "Never trust, always verify."
No Implicit Trust: Access and trust are not automatically granted based on a user's physical location (e.g., being inside the organization's building) or network location (e.g., plugging a device directly into the internal network).

Continuous Validation: Requires strictly verifying and validating trust at every single step of a digital interaction, regardless of where the request originates.