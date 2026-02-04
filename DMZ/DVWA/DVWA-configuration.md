# 🛡️ DMZ Web Server Setup (DVWA on Apache)

---

## 📌 Overview
This document describes the setup of a **DMZ Web Server** hosting the **Damn Vulnerable Web Application (DVWA)**.

The **DMZ (Demilitarized Zone)** is designed to isolate publicly accessible services from the internal LAN, providing **network segmentation** and **layered security**.

DVWA is an intentionally vulnerable web application and is used in this lab for:
- Penetration testing
- Vulnerability assessment
- SOC (Security Operations Center) training

---

## ⚙️ Step 1: HTTPS Certificate Configuration
The DMZ web server is secured using an **SSL/TLS certificate** issued by the internal **SecurityLab Root CA**.

### Certificate Details
- **Common Name (CN):** `192.168.20.100`
- **Organization:** SecurityLab
- **Organizational Unit (OU):** DMZ Web Server
- **Issued By:** SecurityLab Root CA

This ensures encrypted communication while maintaining full control within the lab environment.

---

## ⚙️ Step 2: DVWA Login Page
The DVWA web interface is accessible securely over HTTPS:


Users can authenticate using their assigned credentials to access the application.

---

## ⚙️ Step 3: Security Level Configuration
DVWA allows dynamic adjustment of its security level to simulate different vulnerability exposure scenarios:

- **Low** → Fully vulnerable, no security controls
- **Medium** → Basic protections, still insecure
- **High** → Stricter protections, limited vulnerabilities
- **Impossible** → Fully patched, secure mode

This feature enables testing across multiple difficulty levels.
<img width="1075" height="632" alt="image" src="https://github.com/user-attachments/assets/83ea1e88-1b2f-43a9-afc3-e4e6a56985e7" />

---

## ⚙️ Step 4: DVWA Application Dashboard
After successful authentication, the DVWA dashboard provides access to multiple vulnerable modules, including:

- SQL Injection
- Cross-Site Scripting (XSS)
  - Reflected
  - Stored
  - DOM-based
- Command Injection
- File Upload
- Cross-Site Request Forgery (CSRF)
- Weak Session IDs

These modules are used for realistic attack simulation and defensive monitoring.
<img width="787" height="762" alt="image" src="https://github.com/user-attachments/assets/6414850f-1f3c-481f-9d65-20174d365574" />

---

## ⚙️ Step 5: Web Server & Database Configuration
The DVWA environment is hosted on an **Apache Web Server** with the following configuration:

### Server Environment
- **Server IP:** `192.168.20.100`
- **Web Server:** Apache
- **PHP Version:** 8.2.29

### Database Configuration
- **Database Backend:** MySQL / MariaDB
- **Database Name:** `dvwa`
- **Database User:** `aditya`
- **Database Port:** `3306`
- 
<img width="597" height="552" alt="image" src="https://github.com/user-attachments/assets/a625ae49-6812-4ed9-bbed-32ea07960d25" />

---

## 🛡️ Security Notes
- The DVWA server is **intentionally vulnerable** and must only be deployed in **isolated lab environments**.
- Ensure **pfSense firewall rules** strictly limit access between DMZ and LAN.
- Monitor attack activity using **IDS/IPS tools** such as Snort or Suricata.
- Rotate SSL/TLS certificates periodically, even in lab environments.

---

## ✅ Summary
This DMZ Web Server setup provides a realistic and controlled environment for:

- Practicing web application attack techniques
- Testing SOC detection and response workflows
- Demonstrating how **network segmentation** and **continuous monitoring** protect internal assets from exposed services

