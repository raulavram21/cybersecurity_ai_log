Networks Security and Devices


Network Fundamentals

    Network: The overall infrastructure that allows devices to communicate with each other. (Context: Allows an employee in San Francisco to share resources with an employee in Dublin.)

    Local Area Network (LAN): A network that spans a small area like an office building, a school, or a home.

    Wide Area Network (WAN): A network that spans a large geographical area like a city, state, or country. (Context: The internet itself is the largest WAN.)

    Network Diagram: A map that visually represents the devices on a network and how they connect. (Context: Essential for security analysts to study in order to develop and refine defense strategies for the organization's architecture.)

Core Network Devices

    MAC & IP Addresses: Unique identifiers devices use to locate each other and establish communication.

    Hub: A device that provides a common point of connection for all devices directly connected to it by repeating all information out to all ports. (Context: Think of it like a radio tower broadcasting to everyone. Highly vulnerable to eavesdropping and largely obsolete in modern enterprise networks.)

    Switch: A device that forwards packets between devices directly connected to it by analyzing the destination MAC address. (Context: Operates at the Data Link layer. Much more secure and efficient than a hub because it controls the flow of traffic to specific devices.)

    Router: A network device that connects multiple networks together and directs traffic based on the destination IP address. (Context: Operates at the Network layer. Often includes basic firewall features to block malicious traffic from entering the LAN.)

    Modem: A device that connects the router to the Internet Service Provider (ISP), converting digital signals to a format compatible with the physical connection (cable, fiber). (Context: Brings the internet access into the LAN.)

    Wireless Access Point (WAP): Sends and receives digital signals over radio waves using Wi-Fi standards. (Context: Allows wireless devices to connect to the physical routers and switches on the network.)

    Firewall: A network security device that monitors incoming and outgoing traffic. (Context: The first line of defense; typically placed between the secured internal network and the untrusted external internet.)

    Server: A device that provides information and services for other devices (clients) on the network (e.g., DNS servers, file servers).

Cloud Computing Fundamentals

    Cloud computing: The practice of using remote servers, applications, and network services that are hosted on the internet instead of on local physical devices. (Context: Helps companies reduce costs and streamline operations because online services and web applications can be used from any geographic location.)

    On-premise networks: Traditional networks where all physical devices are kept at a physical location owned by the company (e.g., in a local server room). (Context: Requires significant upfront capital expenditure (CapEx) to purchase hardware, plus ongoing costs to patch, upgrade, and manage the physical components.)

    Cloud Service Provider (CSP): A company that offers cloud computing services by owning massive data centers globally. (Context: CSPs provide technology services at such a large scale that they can sell compute power and storage for a fee, accessed via APIs or web consoles.)

Cloud Deployment Models

    Hybrid cloud environment: When an organization uses a CSP’s services in addition to their own on-premise computers, networks, and storage. (Context: The most common setup for large enterprises, allowing them to balance cost reduction with strict physical control over highly sensitive legacy systems.)

    Multi-cloud environment: When an organization uses services from more than one CSP (e.g., using both AWS and Google Cloud). (Context: Prevents "vendor lock-in" and ensures redundancy if one cloud provider experiences an outage.)

Primary CSP Service Categories

    Software as a Service (SaaS): Software suites operated entirely by the CSP that a company can use remotely without hosting or installing the software themselves. (Context: Examples include Google Workspace or Microsoft 365. The user just logs in and uses the app; the CSP handles all backend security and patching.)

    Infrastructure as a Service (IaaS): The use of virtual computer components offered by the CSP, such as virtual containers, raw storage, and virtual machines. (Context: Allows organizations to "rent" the raw hardware capabilities over the internet. Security teams must still configure the OS and application-level security.)

    Platform as a Service (PaaS): Tools and frameworks that application developers can use to design and deploy custom applications for their company. (Context: The CSP manages the underlying infrastructure (servers, storage, networking) so developers can focus solely on writing and securing their code.)

Software-Defined Networks (SDNs)

    Software-defined networks (SDNs): Networks made up of virtual devices and services that use software to perform packet routing rather than physical hardware. (Context: CSPs host these SDN tools on their servers, allowing security teams to deploy virtual switches, routers, and firewalls instantly via a web console without racking physical gear.)

Benefits of Cloud Computing & SDNs

    Reliability: Based on how consistently available cloud services are, the security of the connections, and high uptime guarantees.

    Decreased Cost: Eliminates the massive upfront cost of buying physical hardware; CSPs offer virtual devices at a fraction of the cost.

    Scalability: The ability to consume services in an elastic "utility" model. (Context: If traffic spikes, a company can instantly scale up server capacity and pay only for what they use. Security controls like WAFs or IDS/IPS can be spun up in seconds to address a sudden threat.)
