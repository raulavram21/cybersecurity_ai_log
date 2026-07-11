Network Traffic and Packet Inspection


Network Protocol Analyzer (Packet Sniffer): A tool designed to capture and analyze data traffic within a network.

        (Context: Analysts use these tools to troubleshoot network issues, inspect packet headers, and identify malicious activity hidden in network flows.)

    Packet Sniffing: The practice of capturing and inspecting data packets across a network.

        (Context: Requires intercepting traffic streams, often demanding root or sudo elevated permissions to access network interfaces.)

    tcpdump: A command-line network protocol analyzer pre-installed on many Linux distributions used to capture network traffic.

        (Context: Because it relies on a CLI, tcpdump is extremely fast for rapid packet capture and filtering directly from a terminal. Captured traffic can be saved into a p-cap file for later analysis.)

    Packet Capture (p-cap): A file containing data packets intercepted from an interface or network.

        (Context: P-cap files act as the physical evidence of network events, storing raw communication bytes that can be analyzed long after the traffic was generated.)

    tcpdump Syntax Structure: The standard format for executing a capture is sudo tcpdump [-i interface] [option(s)] [expression(s)].

        (Context: sudo provides necessary elevated privileges. -i specifies the target network interface (e.g., -i any captures from all interfaces). Options modify command execution, and expressions isolate specific network traffic.)

    tcpdump Core Options (Flags): Command-line arguments used to alter the execution and output of a tcpdump capture.

        -w: Writes or saves the sniffed network packets directly to a specified packet capture file instead of printing them in the terminal (e.g., sudo tcpdump -i any -w capture.pcap).

        -r: Reads and prints a previously saved packet capture file (e.g., sudo tcpdump -r capture.pcap).

        -v, -vv, -vvv: Controls verbosity, increasing the level of detailed packet information printed out.

        -c: Controls the exact count of packets tcpdump will capture before stopping (e.g., -c 10 stops after 10 packets).

        -n: Disables automatic name resolution.

        (Context: By default, tcpdump translates IPs into domain names and ports into associated services. This can cause reverse DNS lookups, potentially alerting an attacker. Using -n ensures accurate, stealthy numerical analysis.)

    tcpdump Expressions: Filters used to isolate specific network packets based on protocols, IPs, or Boolean operators (and, or, not).

        (Context: For example, sudo tcpdump -r capture.pcap -n 'ip and port 80' explicitly filters for IPv4 traffic operating on port 80.)

    IPv4 Header Format: The standard 32-bit IP protocol containing 13 distinct data fields.

        (Context: Key fields include Time to Live (TTL), which limits how long a packet can circulate to prevent endless routing loops, and fragmentation fields, which ensure large packets are broken down and reassembled correctly.)

    IPv6 Header Format: The updated 128-bit IP protocol containing 8 distinct data fields.

        (Context: Includes Version, Traffic Class, Flow Label, Payload Length, Next Header, and Hop Limit, providing a larger address space and more efficient packet routing compared to IPv4.)

    Wireshark Display Filters: Graphical interface tools used to locate specific header fields and values within large p-cap files.

        (Context: Uses comparison operators (==, !=, >, <) and logical Boolean grouping to isolate traffic streams. Examples: ip.addr == 172.21.224.2 filters by IP, and udp.port == 53 filters by UDP port.)

    Wireshark 'Follow Streams': A feature that reassembles the data transferred in a single session/conversation back into a readable format.

        (Context: Highly useful for examining the exact payload contents of an HTTP conversation or an unencrypted TCP session exchange.)

    Technical / CLI Execution: (Blank - Awaiting your hands-on vulnerability testing and DAST pipeline labs)

    Automation Blueprint: (Blank - Awaiting your hands-on vulnerability testing and and DAST pipeline labs)
