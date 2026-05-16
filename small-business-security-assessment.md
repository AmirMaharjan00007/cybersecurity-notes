# Small Business Cybersecurity Assessment — Angels Inc

**Conducted by:** Amir Maharjan  
**Role:** Business Manager and IT Professional  
**Business:** Angels Inc — Cosmetics, Accessories, Footwear and 
Clothing Store  
**Location:** Mahalaxmi Municipality-6, Siddhipur, Lalitpur, Kathmandu  
**Date:** May 2026  
**Assessment Type:** Self-conducted internal security assessment  

---

## Executive Summary

Angels Inc is a family-owned retail business operated by two people —
myself and my wife, Rabina Maharjan, who is the registered proprietor.
The business processes transactions through cash, eSewa, and FonePay
digital payment platforms and maintains an active presence on Facebook
and Instagram.

This assessment identifies current cybersecurity vulnerabilities across
the business's digital operations. It is conducted from the perspective
of an IT Systems Administrator with a BSc (Hons) Computer Systems
Engineering (First Class Honours) and six months of professional IT
experience, who manages the business daily and has direct knowledge
of its technology environment.

This assessment is also deeply personal in its motivation. My wife —
the registered proprietor of Angels Inc — was the victim of an online
financial scam. That experience exposed with direct and painful clarity
exactly how vulnerable ordinary people and small businesses are in
Nepal's rapidly digitising economy. Understanding and addressing these
vulnerabilities is not an academic exercise for me. It is a personal
and professional mission.

---

## Business Technology Profile

| Component | Current Status |
|-----------|---------------|
| Payment platforms | eSewa, FonePay, Cash |
| Devices used | Personal laptops and mobile phones |
| Business/personal separation | None — shared devices |
| Data storage | Personal laptops and physical paper records |
| Cloud backup | None |
| Social media | Facebook and Instagram — active |
| WiFi | Personal home WiFi network |
| Staff | No staff — owner operated |
| Security training | None formal |
| Security policy | None documented |

---

## Vulnerability 1 — Digital Payment Platform Security

### Current Situation
Angels Inc processes a significant portion of transactions through
eSewa and FonePay digital payment platforms. These platforms are
accessed through personal mobile phones used for both business
and personal purposes simultaneously.

### Identified Vulnerabilities

**Shared device risk:**
Payment platform credentials are stored on personal devices that
are also used for personal browsing, social media, app downloads,
and other activities. A single malicious app or phishing link
accessed during personal use could compromise business payment
credentials on the same device.

**No credential rotation policy:**
Payment platform passwords have not been formally reviewed or
rotated on a scheduled basis. Static credentials increase risk
of compromise over time.

**OTP vulnerability:**
One Time Passwords for payment authentication are received on
personal mobile phones. If the device is compromised or if a
social engineering attack successfully manipulates the account
holder into sharing an OTP — as has occurred with my wife
previously — the financial consequences are direct and immediate.

**No two factor authentication audit:**
While eSewa and FonePay offer security features, no formal audit
has been conducted to confirm all available security features
are properly configured and enabled on our accounts.

### Risk Rating: HIGH

### Recommended Remediation
- Designate one specific device exclusively for business payment
  platform access
- Enable all available security features on eSewa and FonePay
  accounts — verify two factor authentication is active
- Implement quarterly password rotation for all payment accounts
- Never share OTP codes with anyone regardless of claimed identity
- Register payment platforms with a dedicated business email
  address separate from personal email

---

## Vulnerability 2 — Device Security and Business-Personal Separation

### Current Situation
All business operations — inventory management, financial record
keeping, social media management, payment processing, and
communication — are conducted on personal laptops and mobile
phones used interchangeably for business and personal purposes.

### Identified Vulnerabilities

**No data separation:**
Business financial records, customer information, payment credentials,
and operational data exist on the same devices as personal photos,
personal emails, personal social media accounts, and personal
applications. A compromise of the personal environment immediately
exposes the business environment.

**Uncontrolled application installation:**
Personal devices have no restrictions on application installation.
Malicious applications installed for personal use could access
business data stored on the same device.

**No device encryption confirmed:**
Full device encryption has not been formally verified on laptops
storing business financial records. If a laptop is lost or stolen,
business data would be accessible without encryption protection.

**No mobile device management:**
No formal policy exists for how devices used for business purposes
should be configured, secured, or managed.

**Single point of failure:**
If either of the two personal devices used for business is damaged,
lost, or stolen, significant business data and operational capability
is lost with no recovery pathway.

### Risk Rating: HIGH

### Recommended Remediation
- Enable full device encryption on all laptops — BitLocker on Windows,
  FileVault on Mac
- Enable screen lock with strong PIN or password on all mobile devices
- Consider dedicated low-cost device for business operations only
- Implement strong screen lock timeout — maximum 2 minutes
- Regularly review installed applications on business-use devices
- Document which devices are authorised for business use

---

## Vulnerability 3 — Data Storage and Backup

### Current Situation
Business records are maintained across personal laptops in digital
format and physical paper documents. No formal backup system exists
for either format.

### Identified Vulnerabilities

**No digital backup:**
All digital business records — financial data, inventory information,
supplier contacts, transaction history — exist only on personal
laptops with no backup copy. Hardware failure, theft, accidental
deletion, or ransomware infection would result in permanent and
total loss of all digital business records.

**Physical records vulnerability:**
Paper-based records are vulnerable to physical damage — fire, flood,
water damage — and loss or theft. No digital backup of physical
records exists.

**No data retention policy:**
No formal policy exists defining how long records should be kept,
where they should be stored, who can access them, and how they
should be securely disposed of when no longer needed.

**Ransomware exposure:**
Without offline backups, Angels Inc would have no recovery option
in the event of a ransomware attack encrypting business data.
Ransomware attacks on small businesses in Nepal are increasing.

### Risk Rating: HIGH

### Recommended Remediation
- Implement automated cloud backup — Google Drive or similar —
  for all business documents
- Maintain offline backup on external hard drive updated weekly
- Photograph or scan critical paper documents for digital backup
- Follow 3-2-1 backup rule — 3 copies, 2 different media types,
  1 offsite copy
- Document data retention and disposal policy
- Test backup restoration regularly — a backup never tested
  is not a reliable backup

---

## Vulnerability 4 — Social Media Account Security

### Current Situation
Angels Inc maintains active business presence on Facebook and
Instagram for customer engagement, product promotion, and
business visibility. These accounts are critical to the
business's marketing and customer relationships.

### Identified Vulnerabilities

**Account hijacking risk:**
Social media business account hijacking is one of the most
frequently reported cybercrimes affecting small businesses
in Nepal. Attackers who gain access to business accounts use
them to scam followers — posting fraudulent offers, requesting
payments, or spreading malware links — causing severe
reputational and financial damage.

**Shared access credentials:**
Business social media accounts accessed from multiple personal
devices increases the attack surface and makes it difficult
to identify unauthorised access.

**No incident response plan:**
No documented procedure exists for responding to social media
account compromise. In the event of hijacking, response would
be delayed and disorganised.

**Personal email linked to business accounts:**
Business social media accounts linked to personal email addresses
mean that compromise of the personal email provides direct access
to business social media accounts.

**No monitoring for unauthorised access:**
Account login activity is not regularly reviewed for suspicious
access from unrecognised devices or locations.

### Risk Rating: HIGH

### Recommended Remediation
- Enable two factor authentication on all social media accounts
  immediately — this is the single most impactful action available
- Create dedicated business email address for all business
  social media accounts
- Review account login activity regularly for unrecognised access
- Document account recovery procedures and keep recovery codes
  securely stored offline
- Review which devices and applications have account access —
  remove any unrecognised or unnecessary access
- Educate on recognising phishing attempts targeting social media
  account credentials

---

## Vulnerability 5 — Network Security

### Current Situation
All business operations are conducted over personal home WiFi
networks. No formal network security assessment has been conducted.

### Identified Vulnerabilities

**No business network separation:**
Business payment processing, financial data access, and sensitive
communications occur over the same network as personal devices,
smart TVs, and any guest devices. A compromised personal device
on the same network could intercept business traffic.

**Router security not audited:**
Default router settings are often insecure. Router firmware
update status and security configuration have not been formally
reviewed.

**No network monitoring:**
No monitoring of network traffic exists to detect unusual activity
that could indicate a compromised device or active attack.

**Public WiFi risk:**
Business operations conducted outside the home — using mobile
data or public WiFi — occur without VPN protection, exposing
business data to potential interception.

### Risk Rating: MEDIUM

### Recommended Remediation
- Change default router admin password immediately
- Ensure router firmware is updated to latest version
- Use WPA3 or WPA2 with AES encryption — not WEP or WPA
- Create separate guest WiFi network for non-business devices
- Consider VPN for business operations conducted outside home
- Review devices connected to network regularly

---

## Vulnerability 6 — Human Factor and Security Awareness

### Current Situation
Angels Inc has two operators — myself and my wife. No formal
cybersecurity awareness training has been completed by either
party. My wife, as the primary customer-facing operator, has
direct exposure to social engineering attempts targeting
the business and its customers.

### Personal Context
My wife was the victim of an online financial scam using social
engineering techniques. This experience demonstrated that even
a well-intentioned, intelligent person can be manipulated by
a well-crafted attack — particularly when urgency, authority,
and trust are exploited simultaneously.

This vulnerability is classified as the highest priority because
no technical control can fully compensate for a successful
social engineering attack that results in an operator voluntarily
providing credentials, OTPs, or financial access to an attacker.

### Identified Vulnerabilities

**No formal security awareness training:**
Neither operator has completed formal training on recognising
and responding to phishing, vishing, smishing, and other
social engineering attacks.

**OTP sharing risk:**
The most common attack vector targeting eSewa and FonePay users
in Nepal involves manipulating account holders into sharing OTP
codes. Without formal training on why OTPs must never be shared,
this remains a critical vulnerability.

**Fake notification risk:**
Fraudulent notifications impersonating eSewa, FonePay, banks,
and government agencies are common in Nepal. Without training
on identifying fake notifications, both operators are vulnerable.

**No incident reporting procedure:**
No clear procedure exists for what to do if either operator
suspects they are being targeted or have been compromised.

### Risk Rating: CRITICAL

### Recommended Remediation
- Complete formal cybersecurity awareness training — available
  through online platforms
- Establish clear rule — OTP codes are NEVER shared with anyone
  for any reason regardless of claimed identity
- Establish verification procedure for any unusual financial
  request — always verify through a second independent channel
- Document what to do if attack is suspected — who to contact,
  what to do immediately, how to report
- Regularly discuss emerging scam tactics targeting small
  businesses in Nepal
- Subscribe to Nepal Police cybercrime awareness updates

---

## Overall Risk Summary

| Vulnerability | Risk Rating | Priority |
|---------------|-------------|----------|
| Human factor and security awareness | CRITICAL | 1 |
| Digital payment platform security | HIGH | 2 |
| Device security and data separation | HIGH | 3 |
| Data storage and backup | HIGH | 4 |
| Social media account security | HIGH | 5 |
| Network security | MEDIUM | 6 |

---

## Remediation Roadmap

### Immediate Actions — This Week
- Enable two factor authentication on all social media accounts
- Enable two factor authentication on all payment platform accounts
- Change all account passwords to strong unique passwords
- Change router admin password
- Enable device screen locks on all devices

### Short Term — This Month
- Enable full device encryption on laptops
- Set up cloud backup for business documents
- Create dedicated business email address
- Complete basic cybersecurity awareness review with wife
- Document OTP and verification procedures

### Medium Term — Next Three Months
- Set up external hard drive backup routine
- Review and update router firmware
- Create dedicated device for payment platform access
- Document basic security policy for the business
- Review all social media account access and connected applications

### Long Term — After Completing Master's Degree
- Implement comprehensive security framework appropriate for
  small retail business
- Deploy proper backup and recovery solution
- Implement network monitoring
- Conduct formal penetration test of business digital environment
- Develop cybersecurity awareness programme applicable to similar
  small businesses in Nepal

---

## Conclusion

This assessment identifies six vulnerability areas across Angels Inc's
digital security posture. None of these are unusual for a small
family-operated retail business in Nepal — they reflect the typical
gap between the rapid pace of digital adoption and the availability
of cybersecurity knowledge for ordinary small business owners.

The most critical finding is the human factor vulnerability. Technical
controls are important but secondary to ensuring that both operators
understand the social engineering tactics being used against small
businesses in Nepal daily and know exactly how to respond.

Addressing these vulnerabilities comprehensively requires the advanced
cybersecurity knowledge I am pursuing through the Master of Information
Technology at the University of Waikato. The skills developed in
network security, information systems security, security risk
management, and digital forensics will allow me to implement proper
security controls in this business and to contribute to the broader
cybersecurity resilience that Nepal's growing community of small
digital businesses urgently needs.

This assessment is not theoretical. Every vulnerability identified
here exists in a real business that my wife and I manage daily. The
remediation roadmap is not an academic exercise — it is a practical
plan I intend to implement, beginning immediately with the quick wins
and progressing to comprehensive security architecture after completing
my postgraduate studies.

---

*Assessment conducted: May 2026*  
*Assessor: Amir Maharjan*  
*BSc (Hons) Computer Systems Engineering — First Class Honours*  
*University of Sunderland, ISMT Kathmandu Campus*  
*IT Systems Administrator — Addon Engineering Solutions (2024-2025)*  
*Kathmandu, Nepal*
