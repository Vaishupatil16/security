# 🏢 Enterprise Security Simulation Lab  
### Red Team vs Blue Team | Cybersecurity 

<img src="https://github.com/user-attachments/assets/b41f8289-4a89-4aa9-9a72-dc59b05263a4" width="800"/>

---

## 📌 Overview
The **Enterprise Security Simulation Lab** simulates a real-world enterprise cybersecurity infrastructure by combining both **offensive (Red Team)** and **defensive (Blue Team)** operations.  

This project provides a hands-on environment to learn and practice:
- Firewall configuration
- IDS/IPS tuning
- Vulnerability exploitation
- Log monitoring and analysis (SIEM)
- Secure remote access (VPN)
- TLS and email security

The lab was fully deployed using **Oracle VirtualBox**, with multiple Linux and Windows virtual machines to closely resemble an enterprise network.

---

## 🎯 Objectives
- Simulate cyber attacks using **Kali Linux Red Team tools**
- Detect and prevent intrusions using **pfSense + Snort**
- Centralize and analyze logs using the **ELK Stack**
- Monitor system health and availability with **Nagios**
- Secure communications using **TLS and OpenVPN**
- Implement **email alerting** for security incidents

---

## 🏗️ Project Architecture

### 🔒 Firewall & Network Segmentation
- **pfSense Firewall** with:
  - WAN, LAN, and DMZ segmentation
  - Strict firewall rules for controlled traffic flow
  - Integrated **Snort IDS/IPS** for intrusion detection and prevention

### 🌐 DMZ Services
- **Debian 12 (Bookworm) Server**
  - Apache Web Server
  - Damn Vulnerable Web Application (DVWA)
  - HTTPS enabled using TLS (self-signed certificate)
- Hosted in the **DMZ** to simulate public-facing enterprise services

### ⚔️ Red Team (Offensive Security)
- **Kali Linux Attacker Machine**
- Tools used:
  - Nmap
  - Burp Suite
  - SQLmap
  - Metasploit
  - LinPEAS
- Simulated attacks:
  - Reconnaissance
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - Privilege Escalation
  - Persistence techniques

### 🛡️ Blue Team (Defensive Security)
- **Nagios**
  - Host and service availability monitoring
  - CPU, memory, disk, and service health checks
- **ELK Stack (SIEM)**
  - Elasticsearch – Log storage
  - Logstash – Log processing
  - Kibana – Dashboards and visualization
  - Filebeat – Log forwarding
- **Snort rule tuning**
- Real-time **email alerts** triggered by suspicious activity

### 🔑 Secure Remote Access
- **OpenVPN Server** integrated with pfSense
- Encrypted and authenticated client access to internal LAN resources

### 🌍 Additional Hardening
- **Bastion Host** for controlled and audited SSH access
- Network isolation to limit lateral movement

---

## 🚀 Features Implemented
- ✅ pfSense firewall with Snort IDS/IPS integration
- ✅ Public DMZ hosting DVWA for attack simulations
- ✅ Centralized monitoring and alerting using ELK Stack
- ✅ System and service monitoring with Nagios
- ✅ OpenVPN for secure remote connectivity
- ✅ Email alerting for security events
- ✅ Red Team vs Blue Team practical simulations
- ✅ HTTPS enabled using TLS

---

## 📊 Learning Outcomes
- Designed and defended an **enterprise-grade security infrastructure**
- Gained hands-on experience in **Red Team and Blue Team operations**
- Implemented **SIEM concepts** using ELK Stack
- Learned practical **incident detection, analysis, and response**
- Applied network hardening techniques (Firewall, TLS, VPN, Email Security)

---

## 🧪 Technologies & Tools Used
- pfSense
- Snort (IDS/IPS)
- Kali Linux
- Debian 12 (Bookworm)
- Apache Web Server
- DVWA
- ELK Stack (Elasticsearch, Logstash, Kibana, Filebeat)
- Nagios
- OpenVPN
- Oracle VirtualBox
- Windows 11

---

## 🔮 Future Enhancements
- Integrate **Wazuh** for host-based intrusion detection (HIDS)
- Add **Cuckoo Sandbox** for malware analysis
- Extend lab to **cloud environments** (AWS / Azure)
- Implement **container security** using Docker and Falco

---

## ✅ Conclusion
The **Enterprise Security Simulation Lab** demonstrates a full-scale cybersecurity environment that closely aligns with real-world enterprise and SOC practices.  

By combining **offensive attack simulations** with **defensive monitoring and response**, this project serves as a strong foundation for:
- Cybersecurity careers
- SOC Analyst roles
- Advanced security research

---
