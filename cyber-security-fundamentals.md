# Cybersecurity Fundamentals

Notes compiled from Security module (BTEC Level 5) and Advanced Cyber
Security module CET324 (BSc Computer Systems Engineering, University
of Sunderland) — Amir Maharjan

---

## 1. The CIA Triad — Foundation of Information Security

The CIA Triad is the core model that guides information security policy
and practice worldwide.

### Confidentiality
Ensuring that information is accessible only to those authorised to
access it.

- Prevents unauthorised disclosure of sensitive information
- Implemented through encryption, access controls, and authentication
- Example: Patient medical records accessible only to authorised
  healthcare staff
- Threats: Eavesdropping, man-in-the-middle attacks, data breaches,
  insider threats

### Integrity
Ensuring that information is accurate, complete, and has not been
tampered with by unauthorised parties.

- Data must remain unaltered during storage, transmission, and processing
- Implemented through hashing, digital signatures, and checksums
- Example: Financial transaction records that cannot be modified after
  being recorded
- Threats: Data tampering, man-in-the-middle attacks, malware, SQL
  injection

### Availability
Ensuring that information and systems are accessible to authorised
users when needed.

- Systems must be operational and responsive at required times
- Implemented through redundancy, backups, and disaster recovery planning
- Example: Online banking systems available 24 hours a day
- Threats: Denial of service attacks, ransomware, hardware failure,
  natural disasters

---

## 2. Types of Security Threats

### Malware
Malicious software designed to disrupt, damage, or gain unauthorised
access to systems.

| Type | Description | Example |
|------|-------------|---------|
| Virus | Attaches to legitimate files and spreads | Infects executable files |
| Worm | Self-replicates across networks without user action | WannaCry |
| Trojan | Disguised as legitimate software | Fake antivirus software |
| Ransomware | Encrypts files and demands payment | LockBit, REvil |
| Spyware | Secretly monitors user activity | Keyloggers |
| Adware | Displays unwanted advertisements | Browser hijackers |

### Network Attacks
- **Denial of Service (DoS):** Overwhelming a system with traffic to
  make it unavailable
- **Distributed DoS (DDoS):** Same as DoS but using multiple compromised
  systems simultaneously
- **Man in the Middle (MitM):** Intercepting communication between two
  parties without their knowledge
- **Packet Sniffing:** Capturing network traffic to extract sensitive data
- **DNS Spoofing:** Redirecting domain name queries to malicious IP
  addresses
- **ARP Poisoning:** Linking attacker MAC address with legitimate IP
  address on local network

### Social Engineering Attacks
Manipulating people into divulging confidential information or performing
actions that compromise security.

- **Phishing:** Fraudulent emails impersonating legitimate organisations
- **Spear Phishing:** Targeted phishing aimed at specific individuals
- **Vishing:** Voice phishing — fraudulent phone calls
- **Smishing:** SMS phishing — fraudulent text messages
- **Pretexting:** Creating fabricated scenarios to extract information
- **Baiting:** Leaving infected USB drives or using fake download links
- **Quid Pro Quo:** Offering a service in exchange for information

*Personal note: My wife was the victim of an online financial scam
using social engineering techniques. This personal experience directly
motivates my commitment to cybersecurity specialisation and public
awareness.*

---

## 3. Risk Management

### Risk Assessment Process
1. **Asset identification** — What needs to be protected?
2. **Threat identification** — What could cause harm?
3. **Vulnerability identification** — Where are the weaknesses?
4. **Risk calculation** — Risk = Likelihood x Impact
5. **Risk treatment** — Accept, mitigate, transfer, or avoid

### Risk Treatment Options
| Option | Description |
|--------|-------------|
| Accept | Acknowledge the risk and do nothing — low impact risks |
| Mitigate | Implement controls to reduce likelihood or impact |
| Transfer | Shift risk to third party — insurance, outsourcing |
| Avoid | Eliminate the activity that causes the risk |

---

## 4. Security Policies and Frameworks

### Common Security Frameworks
- **ISO 27001** — International standard for information security
  management systems
- **NIST Cybersecurity Framework** — US framework covering Identify,
  Protect, Detect, Respond, Recover
- **CIS Controls** — Prioritised set of actions to protect against
  cyber attacks
- **GDPR** — European data protection regulation affecting any
  organisation handling EU citizen data

### Key Security Policies Every Organisation Needs
- Acceptable use policy
- Password policy
- Access control policy
- Incident response policy
- Data backup and recovery policy
- Bring your own device (BYOD) policy

---

## 5. Cryptography Basics

### Symmetric Encryption
- Same key used for both encryption and decryption
- Fast and efficient for large amounts of data
- Key distribution is a challenge — both parties must securely share
  the key
- Examples: AES (Advanced Encryption Standard), DES, 3DES

### Asymmetric Encryption
- Uses a pair of keys — public key and private key
- Public key encrypts, private key decrypts
- Solves the key distribution problem
- Slower than symmetric encryption
- Examples: RSA, ECC (Elliptic Curve Cryptography)

### Hashing
- One-way function — converts data into fixed length string
- Cannot be reversed — used for verification not encryption
- Used for password storage, file integrity verification, digital
  signatures
- Examples: MD5 (weak — deprecated), SHA-256, SHA-3

### Digital Signatures
- Combines asymmetric encryption and hashing
- Verifies authenticity and integrity of a message or document
- Sender signs with private key, recipient verifies with public key

---

## 6. Access Control Models

### Types of Access Control
| Model | Description | Example |
|-------|-------------|---------|
| DAC (Discretionary) | Owner controls access to their resources | File permissions on personal computer |
| MAC (Mandatory) | System enforces access based on classification labels | Government classified documents |
| RBAC (Role-Based) | Access based on user's role in organisation | Employee access based on job title |
| ABAC (Attribute-Based) | Access based on attributes of user, resource, environment | Time-based or location-based access |

### Authentication Factors
- **Something you know** — Password, PIN, security question
- **Something you have** — Smart card, token, mobile phone
- **Something you are** — Fingerprint, face recognition, iris scan
- **Multi-Factor Authentication (MFA)** — Combining two or more factors

---

## 7. Incident Response

### Incident Response Phases
1. **Preparation** — Policies, tools, and team in place before incident
2. **Identification** — Detecting and confirming an incident has occurred
3. **Containment** — Limiting the damage and preventing spread
4. **Eradication** — Removing the threat from the environment
5. **Recovery** — Restoring systems to normal operation
6. **Lessons Learned** — Reviewing the incident to improve future response

---

## 8. Nepal-Specific Cybersecurity Context

Nepal's digital economy is growing rapidly with increasing adoption of:
- Mobile payment platforms — eSewa, Khalti, FonePay
- Online banking and digital wallets
- Social media for business — Facebook, Instagram, TikTok
- Government digital services

Key cybersecurity challenges in Nepal:
- Low cybersecurity awareness among general population
- Limited availability of trained cybersecurity professionals
- Small businesses operating with minimal digital security
- Growing incidents of online financial fraud and social engineering
- Insufficient regulatory framework for cybersecurity enforcement

This context directly motivates my goal of returning to Nepal after
completing the Master of Information Technology at the University of
Waikato to contribute to building Nepal's cybersecurity capability.

---

*Last updated: May 2026*
*Amir Maharjan — Kathmandu, Nepal*
