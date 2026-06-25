OWASP Security Principles


Core OWASP Principles

    Minimize attack surface area: The practice of reducing the total number of potential vulnerabilities a threat actor could exploit. (Context: Limits the attack vectors or pathways attackers can use to penetrate defenses.)

    Principle of least privilege: Making sure that users have only the minimum level of access required to perform their everyday tasks. (Context: Prevents lower-level users from changing system permissions, limiting the blast radius if their account is compromised.)

    Defense in depth: Implementing multiple, overlapping security controls that address risks and threats in different ways. (Context: Ensures that if one layer of defense fails, others are in place to stop the attack.)

    Separation of duties: Distributing critical actions across multiple people so no single individual has absolute control. (Context: A key administrative control used to prevent individuals from carrying out fraudulent or illegal activities unilaterally.)

    Keep security simple: Avoiding unnecessarily complicated security architectures or solutions. (Context: Complexity introduces configuration errors and blind spots; simpler systems are easier to monitor, audit, and secure.)

    Fix security issues correctly: The practice of identifying the root cause, containing the impact, and conducting tests to ensure remediation is successful. (Context: Prevents the exact same vulnerability from being exploited again after an incident is "closed".)

Additional OWASP Principles

    Establish secure defaults: Ensuring that the optimal, most secure state of an application is also its default state out-of-the-box. (Context: It should require extra, deliberate work by the user to make the application insecure, rather than requiring work to make it secure.)

    Fail securely: Designing controls so that when they crash or stop working, they default to their most restrictive option. (Context: If a firewall fails, it should drop all connections and block new ones, rather than failing "open" and allowing all traffic through.)

    Don’t trust services: Operating under the assumption that third-party partners and external systems are not inherently secure. (Context: Organizations must independently validate and verify any data crossing trust boundaries instead of blindly trusting an external vendor's security policies.)

    Avoid security by obscurity: Recognizing that hiding details (like keeping source code secret) does not equate to actual security. (Context: True security relies on strong architecture, encryption, business limits, and access controls, not just hoping attackers cannot find the system.)
