# Internal Network Penetration Testing & Pivoting Lab

> A hands-on cybersecurity laboratory demonstrating internal network reconnaissance, service enumeration, vulnerability assessment, exploitation, Windows pivoting, lateral movement, evidence collection, and remediation planning.

---

## 📌 Project Overview

This project simulates an internal network penetration test against intentionally vulnerable systems in an isolated VMware laboratory.

The assessment demonstrates how an attacker can:

- Perform network reconnaissance
- Identify exposed services
- Enumerate vulnerable services
- Validate security weaknesses
- Exploit vulnerable services in a controlled environment
- Compromise an intermediate Windows host
- Establish a network pivot
- Access an isolated internal network
- Enumerate internal services through the pivot
- Document security findings
- Develop remediation recommendations

---

## 🎯 Objectives

- Identify exposed internal services
- Assess service configurations and authentication controls
- Validate exploitable vulnerabilities
- Demonstrate a realistic internal attack path
- Demonstrate network pivoting
- Assess lateral movement opportunities
- Collect reproducible evidence
- Document security findings and remediation

---

## 🏗️ Lab Architecture

```text
                         KALI LINUX
                       Attacker Machine
                        192.168.xx.xx
                             |
                             |
                         NAT Network
                       192.168.xxx.0/24
                             |
                             v
                      WINDOWS 10 CLIENT
                         Pivot Host
                       192.168.xx.xx
                             |
                             |
                        Pivot Tunnel
                             |
                             v
                      Internal Network
                        10.10.10.0/24
                             |
                             v
                      METASPLOITABLE 2
                        10.10.10.130

```
### Network Interfaces

| System           | Interface | IP Address     | Role            |
| ---------------- | --------- | -------------- | --------------- |
| Kali Linux       | NAT       | 192.168.xx.xx  | Attacker        |
| Windows 10       | NAT       | 192.168.xx.xx  | Pivot Host      |
| Windows 10       | Internal  | 10.10.10.128   | Internal Access |
| Metasploitable 2 | Internal  | 10.10.10.130   | Target          |


### Demonstrated Attack Path

```
       ┌──────────────┐
       │ Kali Linux   │
       │   Attacker   │
       └──────┬───────┘
              │
              │ Initial Access
              ▼
     ┌────────────────────┐
     │ Windows 10         │
     │ Pivot Host         │
     │ 192.168.88.136     │
     └────────┬───────────┘
              │
              │ Meterpreter
              │ Route
              │ + ProxyChains
              ▼
     ┌────────────────────┐
     │ Internal Network   │
     │ 10.10.10.0/24      │
     └────────┬───────────┘
              │
              ▼
     ┌────────────────────┐
     │ Metasploitable 2   │
     │ 10.10.10.130       │
     └────────┬───────────┘
              │
    ┌────┼───────────────┐
    ▼    ▼       ▼       ▼
   SMB  RMI   PostgreSQL Tomcat
   RCE  RCE      Access   Access

```
### 🔎 Methodology

 The assessment followed a structured penetration-testing workflow:
 ```
1. Reconnaissance
       ↓
2. Port Scanning
       ↓
3. Service Enumeration
       ↓
4. Vulnerability Assessment
       ↓
5. Exploitation
       ↓
6. Windows Host Compromise
       ↓
7. Pivot Configuration
       ↓
8. Internal Network Enumeration
       ↓
9. Findings & Evidence
       ↓
10. Remediation Planning

 ```

### 🛠️ Tools & Technologies

Reconnaissance & Enumeration

     - Nmap
     - Gobuster
     - Netcat
     - SMB enumeration tools
     - SMTP enumeration
     - NFS enumeration

Exploitation

     - Metasploit Framework
     - Meterpreter
     - SMB exploitation
     - Java RMI exploitation
     - Bind shell
     - PostgreSQL authentication testing
     - Tomcat authentication testing

Pivoting
    
     - Meterpreter routing
     - ProxyChains
     - SOCKS proxy
     - Internal network enumeration

Platforms
 
     - Kali Linux
     - Windows 10
     - Metasploitable 2
     - VMware Workstation

### 🔬 Assessment Coverage

Network Reconnaissance

     - Performed network discovery and full-port scanning against the lab systems.

Service Enumeration

Services assessed included:

     -  FTP
     - SSH
     - Telnet
     - SMTP
     - DNS
     - HTTP
     - SMB
     - NFS
     - MySQL
     - PostgreSQL
     - IRC
     - Java RMI
     - Tomcat

Vulnerability Assessment

    Security weaknesses identified included:

     - Remote code execution 
     - Weak credentials
     - Default credentials
     - Anonymous access
     - Network service exposure
     - NFS configuration weaknesses
     - Legacy/insecure protocols
     - Unnecessary services
     - Information disclosure

### 💥 Exploitation Highlights

SMB

    A vulnerable SMB configuration was successfully exploited in the controlled laboratory environment, resulting in root-level access on Metasploitable 2.

Java RMI

    The exposed Java RMI service was successfully exploited and a Meterpreter session was obtained.

Bind Shell

    An exposed bind shell was successfully accessed, resulting in root-level shell access.

PostgreSQL

    Weak database credentials were successfully used to authenticate to PostgreSQL.

Tomcat

    Default Tomcat credentials were successfully identified and used to access the management interface.

Telnet

    Authenticated shell access was successfully demonstrated.

   
### 🔀 Pivoting Demonstration

The project demonstrates a practical internal-network pivot.

Step 1 — Windows Compromise

    A Meterpreter session was established on the Windows pivot host.

Step 2 — Internal Route

    A route to the internal network was configured through the Windows Meterpreter session.
    10.10.10.0/24
    
Step 3 — SOCKS Proxy

    A SOCKS proxy was configured through the compromised host.

Step 4 — ProxyChains

    ProxyChains was used to route traffic through the Windows pivot.

Step 5 — Internal Enumeration

    Internal services on:
    10.10.10.130

were successfully accessed and enumerated through the pivot.

### 💡 Skills Demonstrated

```text

Internal Network Penetration Testing
Network Reconnaissance
Port Scanning
Service Enumeration
Vulnerability Assessment
Exploitation
Metasploit Framework
Meterpreter
Windows Security Assessment
Linux Security Assessment
SMB Security
Web Security
Database Security
Network Pivoting
SOCKS Proxy
ProxyChains
Lateral Movement Concepts
Evidence Collection
Security Reporting
Remediation Planning

```
### ⚠️ Disclaimer

This project was performed exclusively in an isolated, authorized laboratory environment using intentionally vulnerable systems.

The techniques demonstrated in this repository are intended for cybersecurity education, authorized penetration testing, and security research.

Do not use these techniques against systems or networks without explicit authorization.


Save `README.md`.

Then your GitHub front page will immediately show the **architecture + attack path + methodology + technical work + findings + remediation**, instead of just a folder list.

**Next step after saving:** we should do a **final project cleanup/check before pushing to GitHub** — especially `.gitignore`, sensitive files, screenshots, and folder contents.
