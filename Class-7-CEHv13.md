# CEHv13 Class 7 Notes

# Phishing & Malware

## Phishing - Email as Medium

### Types of Phishing

1. **Email Phishing Scam**
2. **Spear Phishing** - Targeted (e.g., Organizations, Applications)
   - Simplilearn
   - PayPal
3. **Whaling**
   - Targeting high-ranking individuals like CEO, CTO, CISO, Senior Managers

- [VinciWorks Phishing Awareness Course](https://lms.vinciworks.com/review/CourseLaunch/Courseplayer.aspx?queryStringMain=9idBs03r6T8RTjYeCDLdZAAyLoyR1AQwc5X0PESPKvWxCi/o1oaH79ADIeN59Mmf)
- [Google Phishing Quiz](https://phishingquiz.withgoogle.com/)

### Malware Example
- njRAT

---

# DoS and DDoS Attacks

### TCP Flags
- SYN, ACK, RST, PSH, FIN, URG

### Types of Attacks
1. **Bandwidth** - Consuming bandwidth (e.g., 2TB)
2. **Flood** - Overload with multiple requests
3. **Land Attack** - Same source and destination IP
4. **PDOS** - Permanent DoS (e.g., damage for 24 hours or 10,000 requests)
   - Affects CPU, Memory

### Flood Types
- SYN Flood
- ACK Flood
- ICMP Flood (Ping of Death)

### Tools & Commands

```bash
hping -1 <target> --flood        # ICMP Flood
hping3 -S <target> --flood       # SYN Flood
hping3 -R <target> --flood       # RST Flood
```

- [GitHub DDoS via Memcached - Wired](https://www.wired.com/story/github-ddos-memcached/)

### Prevention Techniques
1. **CDN** - Cloudflare, AWS CloudFront
2. **Load Balancer** - [F5 Networks](https://www.f5.com/glossary/load-balancer)
3. **Web-based Protections** - Filter by Ports (80, 443) and Geo-location
4. **Traffic Monitoring** - Wireshark, NSM, Colasoft Capsa
5. **System Updates**

---

# Session Hijacking

### Concept
- Hijacking valid TCP sessions and HTTP requests
- Identity theft via session IDs

### Labs
- [ECCouncil Lab 1](https://eccouncil.learnondemand.net/Lab/44229?instructionSetLang=en)
- [ECCouncil Lab 2](https://eccouncil.learnondemand.net/Lab/33229?instructionSetLang=en)
- [ECCouncil Lab 3](https://eccouncil.learnondemand.net/Lab/22229?instructionSetLang=en)
- [Lab Client](https://labclient.labondemand.com/LabClient/40ec70d7-c159-4b05-a48c-5366b255167f)

### Tools: Bettercap, Hetty

```bash
sudo su
bettercap -h
ifconfig
ip route eth0, wlan0, en0
bettercap -iface wlan0

# Inside Bettercap
> help
> net.probe on
> net.recon on
> set http.proxy.sslstrip true
> set arp.spoof.internal true
> set arp.spoof.targets 10.10.1.11
> http.proxy on
> net.sniff on
> arp.spoof on
```

### Captured Info
1. All URLs
2. HTTP Session Requests

### Prevention
1. VPN
2. Personal Hotspot
3. SIEM, SOC Monitoring (e.g., ARP packets, Promiscuous mode detection)

---

# Hacking the Web Server

### Communication Process
- Request and Response

### Server Technologies
- IIS (Internet Information Services)
- Apache
- Tomcat
- Databases: MySQL, MSSQL, Oracle, MongoDB

### Common Ports
- HTTP/HTTPS: 80, 443
- SSH: 22
- Telnet: 23
- RDP: 3389
- FTP: 21

### Cloud-Based Attacks
- SSH, Telnet, FTP, RDP Bruteforce

### Scanning & Brute-force

```bash
nmap -p 21,22,23,3389 <target>

hydra -L "Username.txt" -P "Password.txt" ftp://<Target>
```