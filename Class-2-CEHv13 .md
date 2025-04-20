# CEHv13 Class 2 Notes

## Introduction to Ethical Hacking

### CIA Triad
1. **Confidentiality**: Authorized users will have access to data.
2. **Integrity**: Authorized users can modify or make changes to data.
3. **Availability**: Data is accessible 24/7, 365 days whenever needed.
4. **Non-Repudiation**: Ensures that an activity cannot be denied.

---

### Hacking Concepts
- **Hacking**: Gaining unauthorized access to systems or data.
- **Ethical Hacking**: Identifying vulnerabilities with permission.
  - **Scope**: Internal infrastructure, IoT infrastructure.
  - **Limitations**: Cannot prevent DoS/DDoS attacks.

---

### AI-Driven Ethical Hacking
- **AI Tools**:
  - ShellGPT (`sgpt`) by OpenAI
  - HackerGPT, PentestGPT, h4ckGPT
- **Capabilities**:
  - Perform port scans.
  - Report writing.
  - Identify new protocols, ports, process names, OS, and vulnerabilities.
  - Use natural language processing for automation.
- **Average Time to Hack an Organization**: 3-6 months.

---

## Reconnaissance (Info Gathering / Footprinting)

### Types of Reconnaissance
1. **Active Reconnaissance**: Direct interaction (e.g., email, phone, SMS).
2. **Passive Reconnaissance**: Indirect interaction (e.g., internet search, social media).

### Cyber Kill Chain
- Framework to understand and prevent cyberattacks.
- **MITRE ATT&CK Framework**: Provides tactics and techniques for defense.

### Defense in Depth
- Layers of security:
  - Data → Application → Host → Internal Network → Perimeter → Physical → Policies and Procedures.

---

## Risk Management
- **Risk**: Degree of uncertainty, probability, or likelihood of an event.
- **Risk Management**: Vulnerability management (VM).
- **Compliance Impact**:
  - ISO 27000: Information Security Standards.

---

## Module 2: Footprinting and Reconnaissance

### Information to Gather
1. **Organization Information**.
2. **Network Information**.
3. **System Information**.

### Lab Setup
- Tools: VMware, Kali Linux, or Parrot OS.
- Lab Manual: Available in Aspen.

---

### Reconnaissance Techniques

#### Passive Reconnaissance
- Avoid familiar sites.
- Example targets: `doordash.com`, `bricmor.com`.

#### Active Reconnaissance
- **Ping**:
  - Check system status.
  - Retrieve IP address.
  - Identify the target OS.
- **ICMP**: Internet Control Message Protocol.
- **DNS Lookups**:
  - Forward DNS Lookup: Domain name → IP address (e.g., `bricmor.com → 94.136.170.143`).
  - Reverse DNS Lookup: IP address → Domain name.
- **Traceroute**: Trace the network path to a target (e.g., `tracert bricmor.com`).

---

### Commands (Kali/Parrot OS)
- `ifconfig`: Display IP address.
- `ping <target>`: Check system status.
- `traceroute <target>`: Trace the network route.

---

### Useful Tools and Websites
- [Shodan](https://www.shodan.io/)
- [Censys](https://search.censys.io/hosts/)
- [Whois](https://whois.domaintools.com/)
- [Netcraft](https://sitereport.netcraft.com/)
- [Wayback Machine](https://web.archive.org/)
- [Hacker Target](https://hackertarget.com/find-dns-host-records/)
- [Have I Been Pwned](https://haveibeenpwned.com/)

---

## Google Dorks (Advanced Google Hacking Techniques)

### Common Operators
- **`inurl`**: Search for specific terms in the URL.
- **`intext`**: Search for specific terms in the page text.
- **`site:<domain>`**: Search within a specific domain.
- **`intitle`**: Search for specific terms in the page title.
- **`cache:<URL>`**: View the cached version of a webpage.
- **`allinurl`**: Restrict results to pages containing all query terms in the URL.
- **`allintitle`**: Restrict results to pages containing all query terms in the title.
- **`inanchor`**: Search for terms in anchor text on links.
- **`allinanchor`**: Restrict results to pages containing all query terms in anchor text.
- **`link:<URL>`**: Find pages that link to a specific URL.
- **`related:<URL>`**: Find websites similar to the specified URL.
- **`info:<URL>`**: Retrieve information about a specific webpage.
- **`location:<term>`**: Search for information related to a specific location.

### Example Queries
- `site:doordash.com intitle:passwords`
- `cache:www.eccouncil.org`
- `allinurl:EC-Council career`
- `inurl:copy site:www.eccouncil.org`
- `allintitle:detect malware`
- `Anti-virus inanchor:Norton`
- `link:www.eccouncil.org`
- `related:www.eccouncil.org`
- `info:eccouncil.org`
- `location:EC-Council`

---

## TheHarvester Tool
- **Usage**:
  - `theHarvester -h`: Display help menu.
  - `theHarvester -d simplilearn.com -l 100 -b`: Gather information about the domain `simplilearn.com`.












