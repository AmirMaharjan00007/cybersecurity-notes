# Network Security Concepts

Notes from Networking (BTEC Level 5), Network Security (BTEC Level 5),
and Advanced Cyber Security CET324 (BSc Computer Systems Engineering,
University of Sunderland) — Amir Maharjan

Practical experience from IT Systems Administrator Internship at
Addon Engineering Solutions, Kathmandu (September 2024 – February 2025)

---

## 1. Network Fundamentals Review

### OSI Model — 7 Layers
Understanding the OSI model is fundamental to understanding where
network attacks occur and how defences are applied.

| Layer | Name | Function | Example Protocols |
|-------|------|----------|-------------------|
| 7 | Application | User interface and application services | HTTP, HTTPS, FTP, SMTP, DNS |
| 6 | Presentation | Data formatting, encryption, compression | SSL/TLS, JPEG, ASCII |
| 5 | Session | Managing sessions between applications | NetBIOS, RPC |
| 4 | Transport | End-to-end communication, error recovery | TCP, UDP |
| 3 | Network | Logical addressing and routing | IP, ICMP, ARP |
| 2 | Data Link | Physical addressing, error detection | Ethernet, MAC, PPP |
| 1 | Physical | Physical transmission of raw bits | Cables, switches, hubs |

### TCP/IP Model
The practical model used on the internet — four layers:
- Application Layer — HTTP, FTP, DNS, SMTP
- Transport Layer — TCP, UDP
- Internet Layer — IP, ICMP
- Network Access Layer — Ethernet, WiFi

### Key Networking Concepts
- **IP Addressing** — IPv4 (32-bit) and IPv6 (128-bit)
- **Subnetting** — Dividing networks into smaller subnetworks
- **CIDR Notation** — Example: 192.168.1.0/24
- **MAC Address** — Physical hardware address — 48-bit hexadecimal
- **DNS** — Domain Name System — translates domain names to IP addresses
- **DHCP** — Dynamic Host Configuration Protocol — automatically
  assigns IP addresses
- **NAT** — Network Address Translation — maps private IPs to public IP

---

## 2. Network Security Threats

### Reconnaissance Attacks
Gathering information about a target before launching an attack.

- **Passive Reconnaissance** — Monitoring traffic without direct
  interaction — packet sniffing, OSINT
- **Active Reconnaissance** — Direct interaction with target —
  port scanning, ping sweeps
- **Tools used by attackers** — Nmap, Wireshark, Shodan

### Network Attack Types

#### Denial of Service (DoS) and DDoS
- Overwhelming a target with traffic to make it unavailable
- DDoS uses multiple compromised machines — botnets
- Types: Volumetric attacks, Protocol attacks, Application layer attacks
- Defence: Rate limiting, traffic filtering, CDN, anti-DDoS services

#### Man in the Middle (MitM)
- Attacker intercepts communication between two parties
- Neither party knows the attacker is present
- Types: ARP poisoning, DNS spoofing, SSL stripping, WiFi eavesdropping
- Defence: Encryption (HTTPS, TLS), certificate pinning, VPN

#### ARP Poisoning
- Attacker sends fake ARP messages linking their MAC address
  to legitimate IP address
- Allows attacker to intercept, modify, or stop data in transit
- Defence: Dynamic ARP Inspection (DAI), static ARP entries,
  network monitoring

#### DNS Spoofing and Cache Poisoning
- Corrupting DNS cache to redirect users to malicious websites
- User types legitimate URL but lands on attacker-controlled site
- Defence: DNSSEC, encrypted DNS (DoH, DoT), monitoring DNS traffic

#### Packet Sniffing
- Capturing and analysing network traffic
- Can expose unencrypted credentials, session tokens, sensitive data
- Defence: Encryption for all traffic, HTTPS, VPN, avoiding public WiFi
  for sensitive transactions

#### Port Scanning
- Identifying open ports and services on a target system
- Used by attackers for reconnaissance before exploitation
- Common tools: Nmap, Masscan
- Defence: Firewall rules, closing unnecessary ports, intrusion
  detection systems

#### Session Hijacking
- Stealing a user's session token to impersonate them
- Common in web applications without proper session management
- Defence: HTTPS, secure session tokens, short session timeouts,
  token rotation

---

## 3. Network Security Controls and Defences

### Firewalls
A firewall monitors and controls incoming and outgoing network traffic
based on predefined security rules.

| Firewall Type | Description |
|---------------|-------------|
| Packet Filtering | Inspects packets at network layer — IP, port, protocol |
| Stateful Inspection | Tracks connection state — more intelligent than packet filtering |
| Application Layer | Inspects traffic at application layer — content aware |
| Next Generation (NGFW) | Combines traditional firewall with IDS/IPS, deep packet inspection |

### Intrusion Detection and Prevention Systems

**IDS — Intrusion Detection System**
- Monitors network traffic for suspicious activity
- Alerts administrators when threat is detected
- Does not block traffic — detection only
- Types: Network-based (NIDS), Host-based (HIDS)

**IPS — Intrusion Prevention System**
- Monitors and actively blocks suspicious traffic
- Sits inline with network traffic
- Can block, drop, or reset malicious connections

**Detection Methods**
- Signature-based — matches known attack patterns
- Anomaly-based — detects deviation from normal behaviour
- Heuristic-based — uses rules and algorithms to identify threats

### VPN — Virtual Private Network
- Creates encrypted tunnel between user and network
- Protects data in transit from eavesdropping
- Commonly used for remote work and secure browsing
- Protocols: OpenVPN, IPSec, WireGuard, L2TP

### Network Segmentation and VLANs
- Dividing network into separate segments to limit attack spread
- VLANs — Virtual Local Area Networks — logical network separation
- If one segment is compromised, attacker cannot easily move laterally
- Critical systems should be on isolated network segments

### Access Control Lists (ACLs)
- Rules applied to routers and switches controlling traffic flow
- Filter traffic based on IP address, port, protocol
- Standard ACLs — filter by source IP only
- Extended ACLs — filter by source, destination, port, protocol

### Network Monitoring
- Continuous monitoring of network traffic for anomalies
- Tools: Wireshark, Nagios, PRTG, SolarWinds
- Log analysis for security events
- Baseline normal traffic patterns to identify deviations

---

## 4. Wireless Network Security

### WiFi Security Protocols
| Protocol | Status | Notes |
|----------|--------|-------|
| WEP | Broken — do not use | Easily cracked within minutes |
| WPA | Weak — avoid | Vulnerable to TKIP attacks |
| WPA2 | Acceptable | Use with AES encryption |
| WPA3 | Recommended | Strongest current standard |

### Wireless Attack Types
- **Evil Twin Attack** — Rogue access point mimicking legitimate WiFi
- **Deauthentication Attack** — Forcing devices to disconnect and
  reconnect — capturing handshake for offline cracking
- **WPA2 Handshake Capture** — Capturing authentication handshake
  for dictionary or brute force attack
- **War Driving** — Scanning for vulnerable WiFi networks while
  physically moving through an area

### Wireless Security Best Practices
- Use WPA3 or WPA2 with AES
- Strong unique WiFi passwords — minimum 12 characters
- Disable WPS — Wi-Fi Protected Setup — vulnerable to brute force
- Separate guest network from main business network
- Regularly update router firmware
- Disable remote management unless necessary
- Monitor connected devices list regularly

---

## 5. Cisco Networking — Practical Experience

During my BSc programme and internship I used Cisco Packet Tracer
for network simulation and planning.

### Key Cisco Concepts Applied
- Router and switch configuration using CLI
- VLAN configuration and inter-VLAN routing
- Access Control List implementation
- OSPF and RIP routing protocol configuration
- Network Address Translation setup
- Port security on switches
- Spanning Tree Protocol understanding

### Internship Application — Addon Engineering Solutions
During my IT Systems Administrator internship I applied networking
knowledge in a real professional environment:

- Maintained and monitored office network infrastructure
- Configured network access for new users
- Troubleshot connectivity issues across the network
- Managed network documentation
- Assisted in network security protocol implementation
- Monitored network performance and reported anomalies

---

## 6. Nepal Network Security Context

Nepal's network security landscape presents specific challenges:

### Common Threats in Nepal
- Phishing attacks targeting mobile payment platforms
  (eSewa, Khalti, FonePay)
- Social media account hijacking targeting small businesses
- Fake investment and trading platform scams
- SIM swapping attacks targeting mobile banking users
- Ransomware attacks on small and medium enterprises

### Infrastructure Challenges
- Many organisations running outdated network equipment
- Limited budget for enterprise security solutions
- Low awareness of basic network security practices
- Insufficient trained network security professionals
- Rapid digital adoption outpacing security implementation

### Relevance to My Career Goals
Understanding Nepal's specific network security challenges is central
to my motivation for pursuing the Master of Information Technology
at the University of Waikato. The knowledge gained — particularly
in network security architecture, threat detection, and security
implementation — will be directly applied to addressing these
challenges upon returning to Nepal.

---

*Last updated: May 2026*
*Amir Maharjan — Kathmandu, Nepal*
