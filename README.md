# Internal Network Penetration Testing & Pivoting

> **Hands-on internal network penetration-testing lab demonstrating reconnaissance, service enumeration, vulnerability validation, exploitation, Windows pivoting, internal network access, evidence collection, security findings, and remediation planning.**

[![Platform](https://img.shields.io/badge/Platform-VMware-blue)](https://www.vmware.com/)
[![Focus](https://img.shields.io/badge/Focus-Internal%20Network%20Pentesting-red)](https://github.com/Mahesh-CSH/Internal-Network-Penetration-Testing-and-Pivoting)
[![Security](https://img.shields.io/badge/Domain-Cybersecurity-darkgreen)](https://github.com/Mahesh-CSH/Internal-Network-Penetration-Testing-and-Pivoting)

---

## Overview

This project is a controlled internal-network penetration-testing laboratory built with VMware, Kali Linux, Windows 10, and Metasploitable 2.

The objective was to simulate an attacker who gains access to an intermediate Windows system and then uses that system as a pivot point to reach an otherwise isolated internal network.

The assessment covered the complete workflow:

```text
Reconnaissance
      ↓
Port Scanning
      ↓
Service Enumeration
      ↓
Vulnerability Assessment
      ↓
Exploitation
      ↓
Windows Host Compromise
      ↓
Pivot Configuration
      ↓
Internal Network Access
      ↓
Internal Service Enumeration
      ↓
Evidence Collection
      ↓
Findings
      ↓
Remediation
      ↓
Technical Reporting

```

### 🎯 Objectives

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

                         ┌─────────────────┐
                         │    KALI LINUX   │
                         │    ATTACKER     │
                         │ 192.168.xx.xx   │
                         └────────┬────────┘
                                  │
                                  │ NAT
                                  │
                            192.168.xx.0/24
                                  │
                                  ▼
                    ┌────────────────────────┐
                    │      WINDOWS 10        │
                    │       PIVOT HOST       │
                    │                        │
                    │ NAT:      192.168.xx.xx│
                    │ Internal: 10.10.10.128 │
                    └───────────┬────────────┘
                                │
                                │ Pivot
                                │
                                │ 10.10.10.0/24
                                │
                                ▼
                    ┌────────────────────────┐
                    │    METASPLOITABLE 2    │
                    │    INTERNAL TARGET     │
                    │    10.10.10.130        │
                    └────────────────────────┘
    

               
```


### Network Interfaces

| System           | Network  | IP Address       | Role                   |
| ---------------- | -------- | ---------------- | ---------------------- |
| Kali Linux       | NAT      | `192.168.xx.xx`  | Attacker               |
| Windows 10       | NAT      | `192.168.xx.xx`  | Pivot host             |
| Windows 10       | Internal | `10.10.10.128`   | Internal gateway/pivot |
| Metasploitable 2 | Internal | `10.10.10.130`   | Internal target        |



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
Important Design

Kali was configured without direct access to the internal 10.10.10.0/24 network during the pivot demonstration.

This allowed the project to demonstrate genuine access to the internal network through the compromised Windows pivot host rather than simply communicating directly with Metasploitable 2.



### 🧭 Assessment Methodology

1. Reconnaissance

Initial network discovery was performed to identify accessible systems and establish the lab attack surface.

Activities included:

 - Host discovery
 - Network identification
 - Full TCP port scanning
 - Service detection
 - Version identification


2. Service Enumeration

Exposed services were individually enumerated rather than relying exclusively on automated vulnerability scanning.

Services assessed included:


| Service    |      Port | Assessment                         |
| ---------- | --------: | ---------------------------------- |
| FTP        |        21 | Anonymous access / version         |
| SSH        |        22 | Service identification             |
| Telnet     |        23 | Authentication/access              |
| SMTP       |        25 | User enumeration                   |
| DNS        |        53 | Service enumeration                |
| HTTP       |        80 | Web enumeration                    |
| SMB        |   139/445 | Share and vulnerability assessment |
| NFS        |      2049 | Export/configuration assessment    |
| MySQL      |      3306 | Authentication/exposure            |
| PostgreSQL |      5432 | Authentication                     |
| IRC        | 6667/6697 | Service assessment                 |
| Java RMI   |      1099 | Exploitation assessment            |
| Tomcat     |      8180 | Web/application assessment         |



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

  - FTP
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

 - Internal Network Penetration Testing
 - Network Reconnaissance
 - Port Scanning
 - Service Enumeration
 - Vulnerability Assessment
 - Exploitation
 - Metasploit Framework
 - Meterpreter
 - Windows Security Assessment
 - Linux Security Assessment
 - SMB Security
 - Web Security
 - Database Security
 - Network Pivoting
 - SOCKS Proxy
 - ProxyChains
 - Lateral Movement Concepts
 - Evidence Collection
 - Security Reporting
 - Remediation Planning

### ⚠️ Disclaimer

This project was performed exclusively in an isolated, authorized laboratory environment using intentionally vulnerable systems.

The techniques demonstrated in this repository are intended for cybersecurity education, authorized penetration testing, and security research.

Do not use these techniques against systems or networks without explicit authorization.
