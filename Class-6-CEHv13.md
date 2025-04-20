# CEHv13 Class 6 Notes

# Malware Analysis

## Dynamic Analysis

> Execute Malware / System is Infected with Malware

Tools:
- Process Explorer
- Process Monitor (ProcMON)
- Autoruns
- TCPview
- CurrPorts (Mac)

---

## Static Analysis

> Without Execution / Sample

Tools:
- Strings
- BinText
- Dependency Walker
- IDA Pro

---

## Pro in Development Applications - DLLs

**DLLs (Dynamic Linking Libraries):**

1. **Kernel32.dll** – Core functionality (Memory, Files, Hardware)  
2. **Advapi32.dll** – Windows Core Components like Service Manager & Registry  
3. **User32.dll** – User Interface: Buttons, Scrollbars, Mouse  
4. **Gdi32.dll** – Graphics  
5. **wsock32.dll / ws2_32.dll** – Networking DLLs (Network Tasks)

**Examples:**
- `Paint.exe` → Kernel32.dll, wsock32.dll  
- **Malware Dropper** → Additional Executables, TOR Browser, Data Transfer Tools like Netcat

🔗 https://any.run/malware-trends/

---

# Sniffing

## Related Topics

- Sniffing  
- Social Engineering  
- Denial of Service  

---

## Sniffing

### Packets – OSI Layer: Network

Packet Sniffing reveals:
- Source IP
- Destination IP
- Source Port
- Destination Port
- Source MAC
- Destination MAC
- Data

> Monitoring and Capturing all the Data packets.

### Sensitive Information

❌ Avoid using Public/Unknown Wi-Fi for banking and sensitive data.

### Tool: Wireshark

- Uses NIC Cards in **PROMISCUOUS MODE**  
  - Allows reading/capturing **all** network traffic.

Example IP: `192.232.210.172`

---

## Insecure Protocols (Cleartext)

- Port 23 (Telnet)  
- Port 80 (HTTP)  
- Port 143 (IMAP)  
- Port 25 (SMTP)  
- Port 21 (FTP)

---

## MITM – Man in the Middle Attacks

### ARP Poisoning

**ARP Tables** 
  – Maps IP to MAC
  ```bash
  arp -a
  ```

**ARP Table Example**

1. 10.10.1.11 : AE:ER:12
2. 10.10.1.22 : QW:RT:11

**How to Prevent from MITM**:
1. Use of Secure Protocol - 443,22 SSH, IPv6 - IPSec 
2. Use of Proxy / VPN 
3. Update Browsers 

- Router IP 10.10.1.1
- Interface Eth0
- Target IP 10.10.1.22

- echo 1 > /proc/sys/net/ipv4/ip_forward
- arpspoof -i eth0 -t 192.168.29.135 -r 192.168.49.2


## Social Engineering Attacks:

-> People / Human
-> Art of Convincing People to Reveal Confidential info

People are vulnerable to attack
1. Greed 
2. Urgency
3. Trust 
4. Scarcity 

**Impact of Attacks**:

- Economic Losses
- Loss of Privacy
- Temporary / Premenent Closure 

**Type of SE**:

- Human Based SE

1. Impersonation - Pretends to be Someone Legit
2. Dumpster Diving
3. Honey Trap
4. Shoulder Surfing
5. Eavesdropping 
6. Piggybacking 
7. Tailgating 


- Computer Based :- 
1. Phishing - Email as medium 
2. Smishing - SMS as a Medium
3. Vishing  - Voice as a Medium 
