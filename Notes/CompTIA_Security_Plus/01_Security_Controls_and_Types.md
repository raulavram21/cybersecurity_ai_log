Security Control Types
Security controls are strategic safeguards deployed to neutralize vulnerabilities and mitigate risk, categorized by their operational role in addressing threats:

Deterrent Controls: Proactively discourage adversaries from attempting an intrusion by signaling active monitoring or consequences.

Context: They do not physically block activity, but function as psychological obstacles or clear warnings.

Examples: Warning banners (e.g., login consent banners, "No Trespassing" signs), visible perimeter cameras, guard posts.

Preventative Controls: Mechanically, technically, or procedurally block unauthorized actions before execution occurs.

Context: Designed to reduce the attack surface and deny direct access.

Examples: Biometric or keycard door locks, security fencing, strict login authentication mechanisms, role-based access lists, anti-phishing user training.

Detective Controls: Identify, alert, and log security events, malicious anomalies, or unauthorized activities during or after they happen.

Context: Provide visibility so security analysts can investigate events post-facto.

Examples: Closed-circuit television (CCTV), physical door sensors, cryptographic file checksums, Intrusion Detection Systems (IDS), honeypots.

Corrective Controls: Contain damage, remediate active flaws, and return systems to an authentic, secure baseline after an incident occurs.

Context: Directly preserve system Availability and Integrity following a compromise.

Examples: Restoring encrypted volumes from offline backups following a ransomware event, terminating malicious processes, applying hotfix patches.

Compensating Controls: Alternate safeguards deployed to bridge security gaps or mitigate risk when primary controls are unfeasible or compromised.

Context: Provide an equivalent level of defense around structural limitations.

Examples: Enforcing Multi-Factor Authentication (MFA) to bolster systems with weak password capabilities, network segmentation around unpatchable legacy hardware.

Directive Controls: Define behavioral expectations, enforce procedural compliance, and structure administrative workflows.

Context: Dictate human behavior across organizational environments through established standards.

Examples: Acceptable Use Policies (AUP), Standard Operating Procedures (SOPs), onboarding requirements, disciplinary frameworks.

Identity and Access Management (IAM)
The foundational access governance framework, structured around the IAAA model:

Identification (I): The assertion of an identity.

Context: Declaring who or what claims to be interacting with the system.

Examples: Usernames, employee identification numbers, account handles, system service IDs.

Authentication (A): The technical proof of that claimed identity.

Context: Validating whether credentials match the claimed identity before granting entry.

Examples: Passwords/passphrases, PINs, Multi-Factor Authentication (MFA) one-time codes, hardware security keys, biometrics.

Authorization (A): The allocation of permissions and resource entitlements.

Context: Enforcing the Principle of Least Privilege by determining the exact files, applications, networks, or databases an authenticated identity is permitted to access.

Examples: Access Control Lists (ACLs), Role-Based Access Control (RBAC), file read/write/execute permissions.

Accounting (A): Auditing, tracking, and logging interaction history.

Context: Creating an unalterable operational record of user logins, resource modifications, and privilege adjustments for forensic investigations and compliance audits.

Examples: SIEM ingestion logs, authentication attempt timestamps, command execution histories.

The 3 States of Data
Data requires specialized defensive controls depending on its active processing and physical lifecycle state:

Data-in-Transit (Data-in-Motion): Information actively traversing internal networks or public communication routes.

Context: Highly vulnerable to active packet sniffing and interception; protected through network tunneling and transport encryption.

Primary Controls: Transport Layer Security (TLS/HTTPS), IPsec VPNs, SSH, Secure File Transfer Protocol (SFTP).

Data-at-Rest: Information residing persistently in non-volatile storage media.

Context: Susceptible to physical theft or unauthorized device exposure; protected through cryptographic file and disk encryption.

Primary Controls: Full-disk encryption (AES-256), encrypted database tables, access permissions, physical server-rack locking mechanisms.

Data-in-Use: Information loaded into memory, cache, or CPU registers while being actively computed, read, or modified.

Context: Vulnerable to memory-scraping malware and side-channel exploits; difficult to protect without hardware-level safeguards.

Primary Controls: Hardware Trusted Execution Environments (TEEs), secure enclaves, memory-space isolation, strict identity boundary controls.

Zero Trust Architecture (ZTA)
A security paradigm that eliminates perimeter-based implicit trust, requiring continuous validation across all entities, devices, and sessions.

Core Tenet: "Never trust, always verify."

Elimination of Implicit Trust: Physical or logical network proximity (e.g., an internal corporate LAN or physical office subnet) no longer assumes trusted status. All access attempts are treated as originating from an untrusted public network.

Continuous Dynamic Validation: Every access request, session state, and resource transaction must be explicitly authenticated, authorized, and monitored in real time, independent of previous authentications.

Micro-Segmentation: Breaking internal environments into isolated zones to limit lateral attacker movement if a single endpoint or credential is compromised.

Explicit Context Evaluation: Access decisions evaluate multiple real-time indicators—device health posture, user geographic context, anomalous behavior, and least-privilege role boundaries—before granting entry.
