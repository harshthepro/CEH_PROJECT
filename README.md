# 🛡️ Network Penetration Testing with Real-World Exploits & Security Remediation

Welcome to my cybersecurity project where **real-world network attack scenarios** meet **ethical defense strategies**. Built entirely within a **safe virtual lab**, this project explores how to identify, exploit, and secure vulnerable systems using powerful tools like **Kali Linux**, **Metasploitable 2**, **Nmap**, **Metasploit**, and **John the Ripper**.

---

## 🎯 Objectives

- 🔍 Simulate real-world network attacks
- 🧠 Understand vulnerabilities and system weaknesses
- 🛠️ Learn scanning, enumeration, and exploitation techniques
- 🔓 Crack password hashes with John the Ripper
- 🔧 Recommend security remediations for outdated services

---

## 💻 Lab Environment

| Component         | Details               |
|------------------|------------------------|
| Attacker Machine | Kali Linux             |
| Target Machine   | Metasploitable 2       |
| Network Type     | Host-only (Isolated)   |

---

## 🛠️ Tools & Technologies Used

- **Nmap** – Port, OS & Service Scanning
- **Metasploit** – Exploitation Framework
- **John the Ripper** – Password Cracking
- **Linux Commands** – User Enumeration & Management

---

## 🚀 Tasks Performed

### 🔍 Network Scanning

| Command                      | Description                      |
|-----------------------------|----------------------------------|
| `nmap -v IP`                | Basic connectivity and port scan |
| `nmap -v -p- IP`            | Full port scan (1–65535)         |
| `nmap -sV IP`               | Service version detection        |
| `nmap -O IP`                | OS fingerprinting                |

✅ **Hidden ports discovered:** `8787`, `36588`, `53204`, and more.

---

### 📡 Enumeration

- OS Detected: **Linux 2.6.x (Metasploitable)**
- Open Services: **vsftpd**, **OpenSSH**, **Apache**, **MySQL**, **Samba**
- Vulnerable Ports:
  - **21 (FTP)** – backdoored vsftpd
  - **445 (SMB)** – vulnerable to RCE
  - **512–514 (R Services)** – plaintext credentials

---

### 💥 Exploitation

- 📌 **vsftpd 2.3.4** – Backdoor access (CVE-2011-2523)
- 📌 **SMB 3.0.20-Debian** – Exploited using Metasploit
- 📌 **Rexec/Rlogin/Rsh** – Script-based credential theft

---

### 👑 Privilege Escalation

- 🔐 Created root-level user: `rahul`
- 🧩 Extracted `/etc/shadow` hash and cracked it using **John the Ripper**
- 🧠 Gained full access to the system

---

## 🔧 Security Remediation

| Service     | Vulnerability                | Suggested Fix                          |
|-------------|------------------------------|----------------------------------------|
| vsftpd      | Backdoor (CVE-2011-2523)     | Upgrade to `v3.0.5` or switch to SFTP  |
| SMB         | RCE, Null Sessions           | Upgrade to Samba `v4.20.1`             |
| R Services  | Plaintext credentials        | Disable and replace with SSH           |

---

## 📚 Major Learnings

- How to **detect, exploit, and defend** vulnerable systems
- Usage of **Nmap** for deep enumeration (e.g., `-sV`, `-O`, `-p-`)
- Cracking password hashes with **John the Ripper**
- Understanding of **outdated service risks** and how to patch them
- Hands-on practice with **Metasploit modules** for real-world CVEs

---

## ⚠️ Disclaimer

This project was created **strictly for educational purposes**. All actions were conducted in a **safe, offline lab environment**. Do **not** use these techniques on real-world systems without **explicit legal permission**.

---

## 📎 References

- CVE-2011-2523 (vsftpd Backdoor)
- Metasploit Framework Documentation
- John the Ripper Official Guide
- Exploit Database
- Apache and SMB Vulnerability Wikis

---

> 🔐 _"Attack like a hacker. Think like a defender."_  
> _— This project was a bridge between theory and hands-on offensive security._

---

© 2025 — Developed by [Your Name] | Cybersecurity Project | Kali + Metasploitable 2
