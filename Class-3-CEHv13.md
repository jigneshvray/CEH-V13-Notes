# CEHv13 Class 3 Notes

## Tools and Frameworks
- **Sherlock**: "Elon Musk" (Tool for reconnaissance).
- **Recon-ng**: Reconnaissance framework.
- **ShellGPT**: AI-based tool for automation and analysis.

---

## Scanning

### System Identities
- **IP Address**: Unique identifier for a device on a network.
- **MAC Address**: Hardware address of a device.

### Spoofing Techniques
1. **IP Spoofing**:
   - Example IPs:
     - `49.43.231.62`
     - `216.250.127.219`
     - `79.142.66.7`
   - Tools and Resources:
     - [NordVPN - What is My IP?](https://nordvpn.com/what-is-my-ip/)
     - [Psiphon](https://psiphon.ca/en/download.html?psiphonca)

2. **MAC Spoofing**:
   - Tools:
     - [Technitium MAC Address Changer](https://technitium.com/tmac/)
     - SMAC

---

### Web Layers
- **Surface Web**: Publicly accessible websites.
- **Deep Web**: Non-indexed content (e.g., private databases).
- **Dark Web**: Encrypted and anonymous content.
  - Example: [Hidden Wiki](http://zqktlwiuavvvqqt4ybvgvi7tyo4hjl5xgfuvpdf6otjiycgwqbym2qad.onion/wiki/index.php/Main_Page)

---

## Network Scanning

### Tools
- [Shodan](https://www.shodan.io/)
- [Censys](https://censys.io/)
- [Nmap](https://nmap.org/)
- [Zenmap](https://nmap.org/zenmap/)

### Key Concepts
- **Open Ports**: Entry points for communication.
- **Port Ranges**:
  - **0-1023**: Well-known ports.
  - **1024-65535**: Dynamic/private ports.

### Nmap Commands
- `nmap 10.10.1.1-255`: Scan hosts and open ports.
- `nmap -sn 10.10.1.1-255`: Host discovery only.
- `nmap -sU <IP/Domain>`: UDP scan.
- `nmap -p- <IP/Domain>`: Scan all 65,535 ports.
- `nmap -p 21,22,23,25,3389 <IP/Domain>`: Scan specific ports.
- `nmap -O <IP/Domain>`: OS detection.
- `nmap -A <IP/Domain>`: Aggressive scan.

### TCP Flags
- **SYN (S)**, **ACK (A)**, **RST (R)**, **PSH (P)**, **URG (U)**, **FIN (F)**

### Advanced Scanning
- **hping3**:
  - `hping3 -8 1-1000,3389,1433 <IP/Domain> -S`
    - `-8`: Port scanning.
    - `-S`: SYN flag.

---

## Penetration Testing Methodologies
1. **Black Box**: No information provided.
2. **White Box**: Full information provided (e.g., OS, ports, configurations, architecture).
3. **Grey Box**: Partial information provided.

---

## Module 4: Enumeration

### Overview
Enumeration involves extracting detailed information about:
- Usernames
- User groups
- Network shares
- Network resources
- Applications running
- Networks users are connected to

---

### Enumeration Techniques

#### NetBIOS Enumeration
- **NetBIOS**: Network Basic Input/Output System.
  - Used for file and printer sharing.
  - Identifies unique computer names.
- **Ports**: 137, 138, 139.
- **Commands**:
  - `nbtstat -a <IP>`: Displays NetBIOS name table.
  - `nbtstat -c`: Displays NetBIOS cache.
  - `net use`: Lists shared files, paths, and folders.

---

#### SNMP Enumeration
- **SNMP**: Simple Network Management Protocol.
  - Protocol: UDP.
  - Port: 161.
- **Purpose**: Maintains and monitors network devices.
- **Commands**:
  - `nmap -sU -p 161 <IP>`: Scan for SNMP.
  - `snmp-check <IP>`: Perform SNMP enumeration.

---

#### LDAP Enumeration
- **LDAP**: Lightweight Directory Access Protocol.
  - Protocol: TCP.
  - Port: 389.
- **Purpose**: Gather information about:
  - Usernames
  - Addresses
  - Departmental details
  - Server names

---

### Additional Resources
- [VMware Workstation and Fusion](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
- [Parrot Security OS](https://parrotsec.org/download/)
- [Nmap Cheat Sheet](https://www.stationx.net/nmap-cheat-sheet/)
- [YouTube: Ethical Hacking Tutorials](https://www.youtube.com/watch?v=CwDjQZ9b-FQ)




















