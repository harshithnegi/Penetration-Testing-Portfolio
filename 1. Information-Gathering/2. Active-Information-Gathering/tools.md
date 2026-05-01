
# 🛠️ Tools Used

This document contains the tools used during:
- Active Information Gathering
- DNS Enumeration
- Host Discovery
- Port Scanning
- Network Reconnaissance

---

# 🌐 DNS Enumeration Tools

## 🔹 dig

> A command-line DNS lookup utility used for querying DNS servers and retrieving DNS records.

### 📌 Usage

```bash
dig zonetransfer.me
```

### ✅ Common Uses

```text
• DNS record lookup
• Name server enumeration
• Zone transfer testing
• Troubleshooting DNS issues
```

---

## 🔹 dnsenum

> A DNS enumeration tool used for collecting DNS information and discovering subdomains.

### 📌 Usage

```bash
dnsenum zonetransfer.me
```

### ✅ Features

```text
• DNS record enumeration
• Subdomain discovery
• Zone transfer attempts
• Google scraping
• Reverse lookup
```

---

# 🖥️ Network Discovery Tools

## 🔹 Nmap

> Nmap (Network Mapper) is an open-source tool used for network discovery and security auditing.

### 📌 Usage

```bash
nmap 192.168.1.1
```

### ✅ Features

```text
• Host discovery
• Port scanning
• Service detection
• OS detection
• Script scanning
• Firewall detection
```

---

## 🔹 Netdiscover

> Netdiscover is a network address discovery tool primarily used for discovering live hosts on a local network.

### 📌 Usage

```bash
netdiscover -i eth0 -r 192.168.1.0/24
```

### ✅ Features

```text
• ARP reconnaissance
• Live host discovery
• Passive network monitoring
• LAN scanning
```

---

# 📚 Commonly Used Nmap Flags

```text
-sn   → Host discovery only
-Pn   → Skip host discovery
-p-   → Scan all ports
-sU   → UDP scan
-F    → Fast scan
-sV   → Service/version detection
```

---

# ⚠️ Disclaimer

This repository is created for:
- Educational purposes
- Ethical hacking practice
- Authorized penetration testing

Do not use these tools on systems or networks without proper authorization.
