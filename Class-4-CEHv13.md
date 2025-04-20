# CEHv13 Class 4 Notes

## ShellGPT Integration in Parrot Security OS
- [Integration Guide (PDF)](https://labondemand.blob.core.windows.net/content/lab168799/instructions267937/Integrate%20ShellGPT%20in%20Parrot%20%20Security%20Machine.pdf)

### ShellGPT Commands
#### Footprinting
- **Traceroute**:
  ```bash
  sgpt --chat footprint --shell "Perform network tracerouting to discover the routers on the path to a target host www.certifiedhacker.com"
  ```
- **Email Harvesting**:
  ```bash
  sgpt --chat footprint --shell “Use theHarvester to gather email accounts associated with 'microsoft.com', limiting results to 200, and leveraging 'baidu' as a data source”
  ```

- **ICMP Scanning**:
  ```bash
  sgpt --chat scan --shell "Use hping3 to perform ICMP scanning on the target IP address 10.10.1.11 and stop after 10 iterations"
  ```

- **ACK Scan**:
  ```bash
  sgpt --chat scan --shell "Run a hping3 ACK scan on port 80 of target IP 10.10.1.11"
  ```

- **Nmap Scans**:
  ```bash
  1. sgpt --chat scan --shell "Use nmap to find open ports on target IP 10.10.1.11"
  2. sgpt --chat scan --shell "Use Nmap to scan open ports, MAC details, services running on open ports with their versions on target IP 10.10.1.11"
  ```

- **Enumeration**:
  ```bash
  1. NetBIOS Enumeration:
     - sgpt --shell "Perform NetBIOS enumeration on target IP 10.10.1.11"
  2. SNMP Enumeration:
     - sgpt --chat enum --shell "Perform SNMP enumeration on target IP 10.10.1.22 using SnmpWalk and display the result here"
  ```
- **Vulnerability Assessment**:
  ```bash
  sgpt --chat Vuln --shell "Perform vulnerability assessment on simplilearn.com"
  ```

# Vulnerability Analysis

## Tools and Resources
- [OpenVAS](https://www.openvas.org/)
- [Tenable Vulnerability Management](https://www.tenable.com/products/vulnerability-management)

### CVSS Score Example
- **CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C**

### OpenVAS Docker Command
```bash
docker run -d -p 443:443 --name openvas mikesplain/openvas
```

# System Hacking

## Goals
1. Gain Access to Target Machine and Maintain Access.
2. Perform Password Cracking.
3. Exploit Vulnerabilities.
4. Address Malware Threats.
5. Conduct Social Engineering.

---

## Key Techniques
- **Password Cracking of a System**
- **Password Audit**
- **Metasploit and Meterpreter**
- **Armitage**

---

## Password Cracking

### Types of Password Cracking
1. **System Password Cracking**:
   - Windows passwords.
2. **Application Password Cracking**:
   - Cracking passwords for specific applications.
3. **Remote Services**:
   - FTP, SSH, Telnet.
4. **Wi-Fi Password Cracking**:
   - Cracking wireless network passwords.

---

### Types of Password Attacks
1. **Dictionary Attack**:
   - Uses common passwords (e.g., `QWERTY`, `password123`).
   - Example: `QWERTYU`.
2. **Brute Force Attack**:
   - Tries all possible combinations (e.g., `A-Z`, `a-z`, `0-9`, `!@#$%^&*()`).
3. **Rule-Based Attack**:
   - Applies specific rules (e.g., `A-Z`, `!@#$%^&*()`).
4. **Rainbow Table Attack**:
   - Uses precomputed hash values.
   - Example:
     - Password: `QWwerty@123`
     - Hash: `123rasdfgyhgfew3456yuhgfdw34r`
5. **Pass-the-Hash (PTH) Attack**:
   - Collects and cracks password hashes.

---

## Microsoft Authentication

### Authentication Databases
1. **SAM (Security Account Manager)**:
   - Local login database.
2. **Active Directory (AD)**:
   - Network-based domain login database.

### Key Points
- Passwords are never stored in plain text.

---

### Steps to Crack Passwords
1. **Collect the Hash**:
   ```bash
   sudo responder -I eth0
   ```

2. **Crack the Hash**:
   ```bash
   john <password.txt>
   ```
3. **Other Tools**:
   ```bash
   1. ophcrack
   2. hashcat
   3. koohbot

4. **Other thing**:
   ```bash
   Password Audit - Pentest 
   lopathcrack
   ```












































