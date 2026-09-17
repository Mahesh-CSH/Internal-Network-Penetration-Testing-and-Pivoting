
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
                        192.168.88.xxx
                             |
                             |
                         NAT Network
                       192.168.88.0/24
                             |
                             v
                      WINDOWS 10 CLIENT
                         Pivot Host
                       192.168.88.136
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



