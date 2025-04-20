# CEHv13 Class 1 Notes

## Types of Participants
1. **Type 1**: Experienced in Cyber Security with 2+ years / Completed Security+
2. **Type 2**: No experience in Cyber Security but 2+ years in other IT domains
3. **Type 3**: Fresher / New to the domain with no experience

---

## Cyber Security Resources
- [CEH Learning Framework](https://www.eccouncil.org/cybersecurity-exchange/ethical-hacking/ceh-learning-framework/)
- **CEH Kit**:
  - [Aspen](https://aspen.eccouncil.org/MyCourses): Certification Status, Slides, Lab Manuals
  - [iLabs](https://ilabs.eccouncil.org/): Cloud-Based Labs (6 Months Access)
- [Parrot Security OS](https://www.parrotsec.org/download/)

---

## Information Security
- **Key Concepts**: Passwords, Firewalls

---

## System & Networking Overview

### OSI Model Layers
1. **Physical Layer**: Hardware Layer
   - Components: Cables, Connectors, NIC Cards
   - Data Unit: Bits
2. **Data Link Layer**:
   - **MAC Address**: Media Access Control / Hardware Address / Physical Address
     - Example: `30-E3-7A-B0-45-C3`
     - Vendor Identification: [MAC Vendors Lookup](https://macvendors.com/)
   - Commands:
     - `getmac`
     - `ipconfig /all`
3. **Network Layer**:
   - **IP Address**: Internet Protocol / Logical Address
     - IPv4 Example: `49.43.231.55`
     - IPv6 Example: `2405:201:c015:302c:2d38:10b3:9828:58d1`
   - ISP: Internet Service Provider
4. **Transport Layer**:
   - **TCP**: Transmission Control Protocol (Connection-Oriented, Reliable)
   - **UDP**: User Datagram Protocol (Connectionless, Unreliable)
5. **Session, Presentation, Application Layers**:
   - Example Scenario: If a 1GB download is interrupted at 80%, TCP resumes from 80%, while UDP restarts from 0%.

---

## IP Addressing

### IPv4
- **Characteristics**:
  - 32-bit Address
  - Range: `0-255`
  - Total: 4 Billion Addresses
- **Classes**:
  - Class A: `0-127` (e.g., `49.43.231.55`)
  - Class B: `128-191` (e.g., `149.43.231.55`)
  - Class C: `192-223` (e.g., `199.43.231.55`)
  - Class D: `224-239` (e.g., `229.43.231.55`)
  - Class E: `240-255` (e.g., `249.43.231.55`)
- **Limitations**: No built-in IP security

### IPv6
- **Characteristics**:
  - 128-bit Address
  - Example: `2405:201::302c::10b3:9828:58d1`
  - Range: `0-9` and `a-f`
  - Total: 340+ Billion Addresses
- **Features**:
  - Classless IP Addressing
  - IPSec Protocol for Encryption

---

## Network Ports
- **Total Ports**: 65,535
- **Well-Known Ports**: 0-1024
  - HTTP: `80`
  - HTTPS: `443`
  - FTP: `21`
  - SMTP: `25`
  - SSH: `22`

---

## Module 1: Introduction to Ethical Hacking

### Concepts of Information Security
- **CIA Triad**:
  - **Confidentiality**: Ensuring data is private
  - **Integrity**: Ensuring data is accurate
  - **Availability**: Ensuring data is accessible
- **Non-Repudiation**:
  - Example: Internet banking transaction with a unique transaction ID ensures the sender cannot deny the transaction.

### Vulnerabilities
- **Definition**: Weakness, loophole, or flaw in an application, OS, or human behavior
- **Solutions**: Updates, fixes, patches
- **Zero-Day Vulnerabilities**: Bugs or weaknesses with no available solution
  - [Patch Tuesday](https://en.wikipedia.org/wiki/Patch_Tuesday)

---

## Additional Resources
- [LastPass Security Incident](https://blog.lastpass.com/posts/notice-of-recent-security-incident)
- [Capital One Data Breach](https://www.capitalone.com/digital/facts2019/)




























