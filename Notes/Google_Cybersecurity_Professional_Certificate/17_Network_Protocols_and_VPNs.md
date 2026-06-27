Network Protocols and VPNs


Protocol Fundamentals

Network Protocol: A set of rules used by two or more devices on a network to describe the order of delivery and the structure of data.

    (Context: Serves as a common language inside packet headers. Analysts must understand them because attackers exploit flawed or unencrypted protocols to intercept information.)

Transport Layer Protocols

Transmission Control Protocol (TCP): A connection-oriented transport protocol that allows two devices to form a reliable connection and stream data.

    (Context: Enforces a strict three-way handshake (SYN -> SYN-ACK -> ACK) to verify endpoints and retransmits any data segments lost or corrupted in transit.)

User Datagram Protocol (UDP): A connectionless transport protocol that transmits data packets rapidly without establishing a pre-verified connection.

    (Context: Used for performance-sensitive, real-time transmissions like video streaming or fast DNS queries, offering no tracking or recovery.)

Application Layer Protocols & Port Registries

HTTP (Port 80 TCP): An application layer communication protocol that provides a method of communication between clients and website servers.

    (Context: Insecure because it transmits data in plaintext, making it a primary target for packet sniffing and credential harvesting.)

HTTPS (Port 443 TCP): A secure version of HTTP that provides a safe method of communication between clients and website servers.

    (Context: Encrypts transmissions using SSL/TLS to protect data in transit from being read, though it does not conceal source or destination IPs.)

DNS (Port 53 UDP/TCP): A network protocol that translates human-readable domain names into IP addresses.

    (Context: Uses UDP by default but switches to TCP for large payloads. Threat actors exploit it via cache poisoning to divert legitimate traffic to malware sites.)

SFTP (Port 22 TCP): A secure protocol used to transfer files from one device to another over a network.

    (Context: Runs over an encrypted SSH session utilizing AES to secure data-in-transit, making it the standard choice for cloud storage file syncs.)

SSH (Port 22 TCP): An application layer protocol used to create a secure, encrypted connection with a remote system.

    (Context: Provides a safe command-line interface for remote configuration and acts as a replacement for less secure cleartext protocols.)

Telnet (Port 23 TCP): An application layer protocol used to connect with a remote system.

    (Context: Obsolete and highly insecure because it transmits all command prompts and administrative credentials in plaintext.)

SMTP (Port 25 TCP): Used to transmit and route email from a sender to a recipient's address.

    (Context: Targeted heavily by high-volume spam; mail transfer agents use its routing rules to filter and regulate traffic surges.)

SMTPS (Port 587 TCP): A secure implementation of email transmission using the TLS protocol.

    (Context: Enforces encryption on routing paths to protect the confidentiality of email content between mail servers.)

POP3 (Port 110 / 995 TCP): An application layer protocol used to manage and completely retrieve email from a remote mail server onto a local device.

    (Context: Unencrypted traffic uses Port 110, while SSL/TLS uses Port 995. Because data downloads locally, it does not guarantee sync across multiple devices.)

IMAP (Port 143 / 993 TCP): An application layer protocol used to download email headers and sync message states directly on a mail server.

    (Context: Unencrypted traffic uses Port 143; encrypted traffic uses Port 993 over TLS. Keeps mail on the server to allow multi-device syncing.)

SNMP (Port 161/162 UDP): A network protocol used for monitoring and managing infrastructure devices.

    (Context: Allows administrators to fetch bandwidth consumption statistics, alter device baselines, or change configurations remotely.)

DHCP (Port 67/68 UDP): An application layer management protocol used on a network to configure devices.

    (Context: Automatically leases a unique private IP address, default gateway, and DNS mapping to client terminals. Servers use Port 67; clients use Port 68.)

Network Address Translation (NAT) & Local Protocols

Network Address Translation (NAT): A process where a router or firewall replaces local private source IP addresses with a single public-facing IP address for internet traffic.

    (Context: Bridges communication between local private ranges—which are free and non-routable—and globally unique public spaces leased from ISPs.)

Address Resolution Protocol (ARP): A network access layer protocol used to translate logical IP addresses into permanent physical MAC addresses on a local network.

    (Context: Devices store these matches in a local ARP cache table. Because it lacks authentication ports, it is inherently vulnerable to local ARP spoofing.)

Wireless Security Protocols (802.11 / Wi-Fi)

Wired Equivalent Privacy (WEP): An obsolete 1999 wireless security protocol designed to provide users with the same privacy as a wired connection.

    (Context: Relies on short, weak encryption keys that modern tools can crack in minutes, representing a high-risk security vulnerability if left as a default.)

Wi-Fi Protected Access (WPA): A transitional 2003 protocol developed to improve upon WEP by using TKIP and message integrity checks.

    (Context: Weakened by Key Reinstallation Attacks (KRACK), where an attacker manipulates the handshake process to force an all-zero encryption key.)

WPA2 (802.11i Standard): A robust wireless protocol released in 2004 that improves upon WPA by using Advanced Encryption Standard (AES) with CCMP.

    Personal Mode (WPA2-PSK): Employs a single global pre-shared passphrase across all hosts, making it ideal for home networks but unmanageable for companies.

    Enterprise Mode (WPA2-802.1X): Offers individualized, centralized control via an authentication server (like RADIUS), letting admins revoke access without exposing keys.

WPA3: A secure Wi-Fi protocol developed in 2018 to natively resolve WPA2 authentication handshake vulnerabilities to KRACK attacks.

    (Context: Uses Simultaneous Authentication of Equals (SAE) to execute a password-authenticated key agreement, blocking offline handshake brute-forcing.)

Firewalls

Firewall: A network security device that monitors incoming and outgoing traffic to allow or block it based on defined security rules.

    (Context: Acts as an organization's first line of defense, sitting between a controlled internal network and untrusted external spaces like the internet.)

Port Filtering: A core firewall security feature that blocks or allows traffic based on specific port numbers to limit unwanted communication.

    (Context: Configured via rules to explicitly allow critical operations—such as Port 443 for HTTPS—while systematically dropping all other unapproved ports.)

Hardware vs. Software Firewalls: Hardware firewalls are standalone physical appliances that protect a perimeter network boundary. Software firewalls perform the identical filtering logic but are non-physical programs installed on servers or hosts. Software options typically cost less, consume no extra physical space, and protect all devices connected to the server they reside on.

Cloud-Based Firewalls: Software firewalls hosted and maintained by a cloud service provider (CSP) to filter traffic before it reaches virtual cloud networks.

Stateful vs. Stateless Inspection:

    Stateful Firewalls: An advanced class of firewall that keeps track of the state of active connections passing through it to proactively filter out threats.

    Stateless Firewalls: A class of firewall that evaluates data packets individually based on static rules without storing or tracking connection history, making them less secure.

Next-Generation Firewalls (NGFW): High-performance security appliances that combine traditional stateful inspection with deep packet inspection (DPI) and intrusion protection systems (IPS).
Virtual Private Networks (VPNs)

Virtual Private Network (VPN): A network security service that extends a private network over public infrastructure to change the path of data and preserve confidentiality.

    (Context: Protects private traffic from unencrypted packet sniffing by building an encrypted tunnel between an endpoint—any connected computer, mobile device, or server—and a central VPN server.)

Remote Access vs. Site-to-Site Topologies:

    Remote Access VPN: Establishes a secure connection between an individual user's personal device and a corporate VPN server over the internet.

    Site-to-Site VPN: Connects entirely distinct branch office networks to a primary corporate network, though configuring them is highly complex.

VPN Protocols: A set of rules and instructions determining how data moves and encrypts across endpoints inside secure tunnels.

    IPSec VPN: An early industry protocol widely integrated across operating systems. It encrypts and authenticates data packets, making it the traditional choice for site-to-site tunnels due to its extensive security testing, though it is highly complex.

    WireGuard VPN: A modern, high-speed, open-source protocol built using fewer lines of code to achieve enhanced performance and simpler setup. It supports both remote and site-to-site links, utilizing advanced encryption to accelerate processes like streaming or massive file transfers.

Subnetting & Network Segmentation

Subnetting: The process of taking one large network and dividing it into several smaller, organized groups called subnets.

    (Context: Uses network bandwidth more efficiently. Defined by a unique combination of IP addresses and network masks to create a network within a network.)

Classless Inter-Domain Routing (CIDR): A flexible method of assigning subnet masks to IP addresses to replace classful addressing and expand available spaces.

    (Context: Formatted with a trailing slash and prefix length (e.g., 198.51.100.0/24). It maps address chunks to reduce routing table sizes.)

Network Segmentation & Security Zones: Subnetting lets defenders isolate an architecture into distinct security zones using firewalls and custom routing.

    Uncontrolled Zone: Any network completely outside the organization's administrative boundary, such as the public internet.

    Controlled Zone: Internal networks protected from the uncontrolled zone, containing subnets like the Demilitarized Zone (DMZ) which houses public-facing servers as a perimeter, and the Restricted Zone which completely isolates confidential data. If an asset on a guest or student subnet gets contaminated with malware, administrators can instantly isolate it, keeping the core network clean.

Proxy Servers

Proxy Server: A dedicated system that explicitly sits between the internet and the internal network to handle requests on behalf of clients.

    (Context: Uses temporary cache memory to store regularly requested data to optimize speed, and enforces corporate policy by blocking unsafe websites.)

Forward vs. Reverse Proxies:

    Forward Proxy: Regulates and restricts internal users. It receives outgoing traffic from an employee, approves it, and forwards it to the internet.

    Reverse Proxy: Regulates and restricts internet traffic trying to access an internal web server. It balances incoming traffic load and filters out spam by validating headers.
