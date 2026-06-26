Network Communication and IPs


Network Communication Basics

    Network Communication: The transfer of data from one point to another over a network.

        (Context: While essential for operations, communication makes network attacks more likely because it gives a malicious actor an opportunity to take advantage of vulnerable devices and unprotected networks.)

    Data Packet: A small unit of data transferred over a network.

        (Context: Packets contain a header that includes the IP address, MAC address of the destination device, and a protocol number that tells the receiving device what to do with the information.)

    Bandwidth: The amount of data a device receives every second.

    Speed: The rate at which data packets are received or downloaded.

        (Context: Security personnel monitor bandwidth and speed because irregularities—like unexplained spikes or drops—are often clear indicators of an active network attack.)

    Packet sniffing: The practice of capturing and inspecting data packets across the network.

    Port: A software-based location within an operating system that organizes the sending and receiving of data.

        (Context: Port numbers allow computers to split network traffic and prioritize operations. Common examples include Port 25 (email), Port 443 (secure internet/HTTPS), and Port 20 (file transfers).)

IPv4 Packet Structure

An IPv4 packet consists of a Header (20–60 bytes) and Data (payload, up to 65,535 bytes total). The header dictates routing, while the data contains the actual message (website content, email text).

    13 Header Fields:

        Version (VER): Tells receiving devices which IP protocol is in use.

        Header Length (IHL): Indicates where the header ends and the data segment begins.

        Type of Service (ToS): Helps routers prioritize packet delivery for quality of service.

        Total Length: Size of the entire IP packet.

        Identification, Flags, & Fragmentation Offset: Manage the fragmentation/reassembly of large packets that exceed network size limits.

        Time to Live (TTL): A counter that prevents packets from looping indefinitely; routers decrement it, and discard the packet if it reaches zero.

        Protocol: Tells the receiving device which protocol governs the data portion.

        Header Checksum: Used to detect header corruption during transit.

        Source/Destination IP Address: Identifies the sending and receiving devices.

        Options: Optional field for security or specialized routing.

IPv4 vs. IPv6

    IPv4 Address: Four decimal numbers (0-255) separated by dots (e.g., 198.51.100.0). Limited to 4.3 billion addresses, leading to exhaustion.

    IPv6 Address: Eight hexadecimal numbers separated by colons (e.g., 2002:0db8::ff21:0023:1234). Allows for 340 undecillion addresses to mitigate exhaustion.

        (Context: The "::" shorthand replaces consecutive sets of zeros to simplify long addresses.)

The TCP/IP Model (4 Layers)

The standard framework for visualizing network communication.

    1. Network Access Layer: Deals with data packet creation and physical transmission (hubs, modems, cabling).

    2. Internet Layer: Attaches IP addresses to packets for routing between different networks (IP, ICMP).

    3. Transport Layer: Controls traffic flow and delivery (TCP for reliable connections, UDP for speed).

    4. Application Layer: Protocols for network requests/responses (HTTP, SMTP, SSH, FTP, DNS).

The OSI Model (7 Layers)

A standardized conceptual framework used by security professionals to pinpoint where problems or threats occur.

    Layer 7: Application Layer: User-facing processes (web browsers, email).

    Layer 6: Presentation Layer: Data translation, compression, and encryption (SSL/TLS).

    Layer 5: Session Layer: Manages connections, authentication, and session checkpoints.

    Layer 4: Transport Layer: Segmentation, flow control, and speed (TCP/UDP).

    Layer 3: Network Layer: Logical addressing and routing across networks (Routers/IP).

    Layer 2: Data Link Layer: Local network addressing and switching (MAC addresses/Switches).

    Layer 1: Physical Layer: Raw transmission of bits over cables, fiber, or radio waves.
