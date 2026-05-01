# 🔎 Active Information Gathering

---

# 🌐 DNS Zone Transfer

## 📖 What is DNS?

> **DNS (Domain Name System)** is a protocol used to resolve domain names or hostnames into IP addresses.

---

# 🧾 DNS Record Types

```text
A      → Resolves a hostname/domain to an IPv4 address
AAAA   → Resolves a hostname/domain to an IPv6 address
NS     → Name Server record
MX     → Mail Server record
CNAME  → Domain alias record
TXT    → Stores text information
HINFO  → Host information
SOA    → Start of Authority
SRV    → Service records
PTR    → Resolves IP address to hostname
```

---

# 🛰️ DNS Interrogation

> DNS Interrogation is the process of enumerating DNS records for a specific domain.

### 🎯 Information Gathered
- Subdomains
- Mail servers
- Name servers
- Internal infrastructure
- Service information

---

# 🔄 DNS Zone Transfer

DNS administrators may copy or transfer zone files from one DNS server to another.

This process is known as a **Zone Transfer**.

If DNS servers are:
- Misconfigured
- Unsecured
- Publicly accessible

Attackers can abuse this feature to obtain the complete DNS zone file.

---

## ⚠️ Exposed Information

```text
• Internal hostnames
• Server IP addresses
• Mail infrastructure
• Network layout
• Development systems
```

---

# ⚡ DNS Enumeration Commands

## 🔹 Basic DNS Lookup

```bash
dig zonetransfer.me
```

---

## 🔹 Query Specific Name Server

```bash
dig @nsztm1.digi.ninja zonetransfer.me
```

---

## 🔹 Perform DNS Zone Transfer

```bash
dig axfr @nsztm1.digi.ninja zonetransfer.me
```

---

## 🔹 DNS Enumeration Using dnsenum

```bash
dnsenum zonetransfer.me
```

---

# 🖥️ Host Discovery With Nmap

## 📖 What is Nmap?

> **Nmap (Network Mapper)** is an open-source tool used for:
- Network exploration
- Host discovery
- Port scanning
- Security auditing

---

# 🔍 Host Discovery Commands

## 🔹 Discover Live Hosts

```bash
sudo nmap -sn 192.168.2.0/24
```

### 📌 Flag Explanation

```text
-sn   → Ping scan (host discovery only)
```

---

# 🌐 Host Discovery With Netdiscover

```bash
netdiscover -i eth0 -r 192.168.2.0/24
```

### 📌 Flag Explanation

```text
-i    → Network interface
-r    → IP range
```

---

# 🚪 Port Scanning With Nmap

## 🔹 Default Nmap Scan

```bash
nmap 10.4.19.218
```

### 📌 What It Does

```text
• Scans top 1000 TCP ports
• Performs basic service detection
```

---

## 🔹 Scan Without Host Discovery

```bash
nmap -Pn 10.4.19.218
```

### 📌 Flag Explanation

```text
-Pn   → Skip host discovery
```

### ✅ Useful When

```text
• ICMP is blocked
• Firewall blocks ping packets
```

---

## 🔹 Scan All Ports

```bash
nmap -p- 10.4.19.218
```

### 📌 Flag Explanation

```text
-p-   → Scan all 65535 TCP ports
```

---

## 🔹 Scan Specific Port Range

```bash
nmap -Pn -p1-4500 10.4.19.218
```

### 📌 Flag Explanation

```text
-p1-4500   → Scan ports from 1 to 4500
```

---

## 🔹 UDP Port Scan

```bash
nmap -Pn -sU 10.4.19.218
```

### 📌 Flag Explanation

```text
-sU   → UDP scan
```

---

## 🔹 Fast Scan + Service Detection

```bash
nmap -Pn -F -sV 10.4.19.218
```

### 📌 Flag Explanation

```text
-F    → Fast scan
-sV   → Service/version detection
```

---

# 📚 Summary

## 🛠️ DNS Enumeration Tools

```text
• dig
• dnsenum
```

---

## 🛠️ Network Discovery Tools

```text
• nmap
• netdiscover
```

---

# 📌 Common Nmap Flags

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

This content is intended for:
- Educational purposes
- Ethical hacking labs
- Authorized penetration testing only

> Do not scan or enumerate systems without proper authorization.
