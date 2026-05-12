# 💻 System / Host Based Attacks

---

# 📖 Introduction

System or Host Based Attacks are attacks that are specifically targeted towards a particular system or host running a specific operating system.

### 🎯 Examples

```text
• Windows
• Linux
```

These attacks mainly focus on exploiting vulnerabilities present within the target operating system.

---

# 🛡️ What Are System/Host Based Attacks?

System or host based attacks usually come into play after an attacker has already gained access to a target network.

Once inside the network, the attacker may target:
- Servers
- Workstations
- Laptops
- Internal systems

to further expand access or gain higher privileges.

---

# 🎯 Main Objective

The primary objective of these attacks is to exploit:

```text
• Inherent operating system vulnerabilities
• Weak configurations
• Misconfigured services
• Weak file permissions
• Exposed credentials
```

These attacks may also involve exploiting:
- Default configurations
- Weak security settings
- Unpatched systems
- Improperly configured services

within the target operating system.

---

# 📚 Topics Covered

---

# 🪟 Windows Based Attacks

## 🔹 Overview of Windows Vulnerabilities

Understanding common vulnerabilities found in Windows operating systems such as:
- SMB vulnerabilities
- Weak permissions
- Outdated services
- Misconfigured settings

---

## 🔹 Exploiting Windows Vulnerabilities

Techniques used to gain access to Windows systems by exploiting:
- Vulnerable applications
- Services
- Misconfigurations
- Security weaknesses

---

## 🔹 Windows Privilege Escalation

Methods used to increase privileges after gaining initial access.

### 📌 Goal

```text
• Gain Administrator privileges
• Gain SYSTEM level access
```

---

## 🔹 Windows File System Vulnerabilities

Focuses on exploiting weaknesses related to:
- File permissions
- Writable directories
- Shared folders
- Sensitive files

---

## 🔹 Windows Credential Dumping

The process of extracting credentials from a compromised Windows system.

### 📌 Common Targets

```text
• SAM database
• LSASS process
• Cached credentials
```

---

## 🔹 Windows Lateral Movement

Techniques used to move from one compromised system to another inside the network.

### 📌 Common Methods

```text
• SMB
• PsExec
• RDP
• WMI
```

---

# 🐧 Linux Based Attacks

## 🔹 Overview of Linux Vulnerabilities

Understanding vulnerabilities commonly found in Linux systems such as:
- Weak file permissions
- Vulnerable services
- Misconfigured applications
- Outdated software

---

## 🔹 Exploiting Linux Vulnerabilities

Techniques used to compromise Linux systems through:
- Vulnerable services
- Misconfigurations
- Weak SSH configurations
- Exploitable applications

---

## 🔹 Linux Privilege Escalation

Methods used to gain higher privileges or root access on Linux systems.

### 📌 Common Techniques

```text
• SUID binaries
• Weak sudo permissions
• Writable cron jobs
• Kernel exploits
```

---

## 🔹 Linux File System Vulnerabilities

Focuses on exploiting:
- Weak permissions
- Sensitive configuration files
- Writable directories
- Insecure services

---

## 🔹 Linux Credential Dumping

The process of extracting password hashes or credentials from Linux systems.

### 📌 Common Targets

```text
• /etc/passwd
• /etc/shadow
• SSH keys
```

---

# ⚠️ Disclaimer

This content is intended for:
- Educational purposes
- Ethical hacking labs
- Authorized penetration testing only

> Do not exploit systems without proper authorization.
