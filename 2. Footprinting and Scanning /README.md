
# 🔎 Footprinting & Scanning With Nmap

---

# 📖 Introduction

**Footprinting** and **Scanning** are important phases of penetration testing used to gather information about a target system or network.

These phases help identify:
- Live hosts
- Open ports
- Running services
- Operating systems
- Firewall protections
- IDS/IPS configurations

---

# 🖥️ Host Discovery

Host Discovery is used to determine whether a target system is online or reachable.

---

## 🔹 Disable Host Discovery (Treat Host As Online)

```bash
nmap -Pn 192.148.40.3
```

### 📌 Explanation

```text
-Pn   → Skip host discovery and treat target as online
```

### ✅ Useful When

```text
• ICMP packets are blocked
• Firewall drops ping requests
• Target does not respond to ping
```

---

# 🚪 Port Scanning

Port Scanning is used to identify open ports and services running on a target system.

---

## 🔹 TCP SYN Scan (Stealth Scan)

```bash
nmap -sS -Pn 192.148.40.3
```

### 📌 Explanation

```text
-sS   → TCP SYN Stealth Scan
-Pn   → Skip host discovery
```

### ✅ Features

```text
• Fast scanning
• Less detectable
• Does not complete TCP handshake
• Commonly used in penetration testing
```

---

# 💻 OS Discovery

OS Discovery helps identify the operating system running on the target machine.

---

## 🔹 Operating System Detection

```bash
nmap -O 192.148.40.3
```

### 📌 Explanation

```text
-O   → Enable operating system detection
```

### ✅ Information Gathered

```text
• OS type
• Device type
• Network distance
• TCP/IP fingerprinting
```

---

## 🔹 SMB OS Discovery Script

```bash
nmap --script=smb-os-discovery.nse 192.148.40.3
```

### 📌 Explanation

```text
--script=smb-os-discovery.nse
→ Uses NSE script for SMB OS detection
```

### ✅ Information Gathered

```text
• Operating system
• Computer name
• Domain name
• SMB version
```

---

# 🛡️ Firewall & IDS/IPS Evasion Techniques

Nmap provides several techniques to bypass:
- Firewalls
- IDS (Intrusion Detection Systems)
- IPS (Intrusion Prevention Systems)

---

## 🔹 Packet Fragmentation

```bash
nmap -sS -f 192.148.40.3
```

### 📌 Explanation

```text
-sS   → SYN scan
-f    → Fragment packets
```

### ✅ Purpose

```text
• Bypass packet filters
• Evade IDS/IPS detection
```

---

## 🔹 Source Port Manipulation

```bash
nmap -sS -Pn -g 80 192.148.40.3
```

### 📌 Explanation

```text
-g 80   → Use source port 80
```

### ✅ Purpose

```text
• Bypass poorly configured firewalls
• Make traffic appear legitimate
```

---

## 🔹 Fragmentation + Source Port Manipulation

```bash
nmap -sS -Pn -f -g 80 192.148.40.3
```

### 📌 Explanation

```text
-f      → Fragment packets
-g 80   → Use source port 80
```

### ✅ Purpose

```text
• Increased stealth
• Firewall evasion
• IDS bypass techniques
```

---

## 🔹 Decoy Scan

```bash
nmap -sS -D RND:5 192.148.40.3
```

### 📌 Explanation

```text
-D RND:5   → Use 5 random decoy IP addresses
```

### ✅ Purpose

```text
• Hide real attacker IP
• Confuse IDS/IPS logs
• Increase anonymity
```

---

## 🔹 MAC Address Spoofing

```bash
nmap -sT -Pn --spoof-mac 0 192.148.40.3
```

### 📌 Explanation

```text
-sT            → TCP Connect scan
--spoof-mac 0  → Random MAC address spoofing
```

### ✅ Purpose

```text
• Hide original MAC address
• Bypass MAC filtering
• Increase anonymity
```

---

# ⚡ Additional Useful Nmap Scans

---

## 🔹 Scan Specific Ports

```bash
nmap -p 80,443 192.148.40.3
```

### 📌 Purpose

```text
• Scan only selected ports
```

---

## 🔹 Scan All Ports

```bash
nmap -p- 192.148.40.3
```

### 📌 Purpose

```text
• Scan all 65535 TCP ports
```

---

## 🔹 UDP Scan

```bash
nmap -sU 192.148.40.3
```

### 📌 Purpose

```text
• Discover UDP services
```

---

## 🔹 Service Version Detection

```bash
nmap -sV 192.148.40.3
```

### 📌 Purpose

```text
• Detect service versions
• Identify running applications
```

---

## 🔹 Aggressive Scan

```bash
nmap -A 192.148.40.3
```

### 📌 Includes

```text
• OS detection
• Version detection
• Script scanning
• Traceroute
```

---

## 🔹 Fast Scan

```bash
nmap -F 192.148.40.3
```

### 📌 Purpose

```text
• Scan fewer common ports quickly
```

---

## 🔹 Verbose Scan

```bash
nmap -v 192.148.40.3
```

### 📌 Purpose

```text
• Show detailed scan progress
```

---

## 🔹 Save Scan Output

```bash
nmap -oN output.txt 192.148.40.3
```

### 📌 Purpose

```text
• Save normal output to a file
```

---

## 🔹 Save Output in All Formats

```bash
nmap -oA scan_results 192.148.40.3
```

### 📌 Generates

```text
• Normal output
• XML output
• Grepable output
```

---

# 📚 Commonly Used Nmap Flags

```text
-sS      → SYN Stealth Scan
-sT      → TCP Connect Scan
-sU      → UDP Scan
-sV      → Service Version Detection
-O       → OS Detection
-A       → Aggressive Scan
-Pn      → Skip Host Discovery
-p-      → Scan All Ports
-F       → Fast Scan
-f       → Fragment Packets
-g       → Source Port Manipulation
-D       → Decoy Scan
-v       → Verbose Output
-oN      → Save Normal Output
-oA      → Save All Output Formats
```

---

# ⚠️ Disclaimer

This content is intended for:
- Educational purposes
- Ethical hacking practice
- Authorized penetration testing only

> Do not scan systems or networks without proper authorization.
