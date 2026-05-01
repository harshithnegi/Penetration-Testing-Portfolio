# 🧠 Passive Information Gathering - Notes

## 📌 Introduction
Information Gathering is the first phase of penetration testing.

More information collected in this phase increases the chances of success in later stages like scanning, enumeration, and exploitation.

---

## 🔍 Types of Information Gathering

### 🟢 Passive Information Gathering
- No direct interaction with the target
- Completely stealthy
- No logs generated on target systems

### 🔴 Active Information Gathering
- Direct interaction with the target
- Can be detected and logged

---

## 🕵️ Passive Information Gathering

In passive reconnaissance, we collect information from publicly available sources without interacting directly with the target.

---

## 📊 Information That Can Be Collected

- IP Addresses
- Hidden directories (not indexed by search engines)
- Names of individuals or organizations
- Email addresses
- Phone numbers
- Physical addresses
- Web technologies used by the target

---

## 🌐 Web Recon & Footprinting (Practical)

Target example: hackersploit.org

---

## 🔎 DNS Lookup

Using host command:
- Retrieves IP address
- IPv6 address
- Mail servers

---

## 📄 robots.txt

URL:
https://hackersploit.org/robots.txt

- Defines which paths are allowed or disallowed for search engines
- Can reveal hidden or sensitive directories

---

## 🗺️ sitemap.xml

URL:
https://hackersploit.org/sitemap.xml

- Provides structure of the website
- Lists important URLs of the site

---

## 🕵️ Technology Detection

Tools used:
- BuiltWith
- Wappalyzer

Command:
- whatweb hackersploit.org

Information obtained:
- Server details
- CMS used
- Frameworks and technologies

---

## 📥 Website Cloning (HTTrack)

- Used to download an entire website locally
- Useful for offline analysis and inspection

---

## 🔎 Whois Enumeration

Command:
whois hackersploit.org

Information obtained:
- Domain registration details
- Registrar information
- Creation and expiry dates
- Name servers

---

## 🌍 Netcraft

Website:
https://www.netcraft.com

- Provides website footprinting
- Hosting and infrastructure details

---

## 🌐 DNS Enumeration

Tools:
- dnsrecon

Commands:
dnsrecon -d hackersploit.org
dnsrecon -d zonetransfer.me

Information obtained:
- A, AAAA, MX, NS, TXT records

---

## 🌐 DNS Dumpster

Website:
https://dnsdumpster.com

- Visual DNS mapping
- Subdomain discovery

---

## 🛡️ WAF Detection

Command:
wafw00f hackersploit.org

- Detects Web Application Firewall (WAF)
- Helps in attack planning

---

## 🌐 Subdomain Enumeration

Command:
sublist3r -d hackersploit.org

- Discovers subdomains
- Expands attack surface

---

## 🔍 Google Dorking

Examples:
site:ine.com inurl:forum
site:*.ine.com filetype:pdf
intitle:index of
cache:ine.com

- Used to find hidden or sensitive information

---

## 🕰️ Wayback Machine

Website:
https://archive.org/web

- Shows historical versions of websites
- Useful for finding deleted content

---

## 💥 Exploit Database

Website:
http://exploit-db.com

- Repository of known vulnerabilities and exploits

---

## 📧 Email Harvesting

Command:
theHarvester -d hackersploit.org

- Collects emails, subdomains, and IP addresses

---

## 🔐 Data Breach Check

Website:
https://haveibeenpwned.com

- Checks if email or password has been part of any breach

---

## 💡 Final Learning

- Passive reconnaissance is safe and stealthy
- No direct interaction with target
- Helps build initial understanding of target infrastructure
- Forms the foundation of penetration testing
