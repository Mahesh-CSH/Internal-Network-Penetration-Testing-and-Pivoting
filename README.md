# Internal Network Penetration Testing & Pivoting Lab

## Overview

A practical internal network penetration testing lab demonstrating reconnaissance,
service enumeration, vulnerability assessment, exploitation, Windows pivoting,
internal network access, remediation, and retesting.

The assessment was performed in an isolated VMware lab environment using Kali Linux,
Windows 10 Client, and Metasploitable 2.

---

## Objectives

- Perform network reconnaissance
- Enumerate exposed services
- Identify security weaknesses
- Validate selected vulnerabilities through controlled exploitation
- Establish a Windows pivot
- Access an isolated internal network through the pivot
- Document security findings
- Apply remediation recommendations
- Perform retesting

---

## Lab Architecture

    Kali Linux


			      192.168.88.129
				     |
				     |
			      Windows 10 Client
			      192.168.88.136
			      10.10.10.128
				     |
				Windows Pivot
				     |
			     10.10.10.0/24
				     |
				     |
			    Metasploitable 2
			      10.10.10.130
			      
		      
  Methodology   
		  
		  
			Reconnaissance
			      ↓
			Service Enumeration
			      ↓
			Vulnerability Assessment
			      ↓
			Controlled Exploitation
			      ↓
			Pivoting
			      ↓
			Internal Network Validation
			      ↓
			Findings   
			      ↓
			Remediation
			      ↓       
			Retest               
		  
	Key Technologies              
	
			Kali Linux
			VMware Workstation
			Nmap
			Metasploit Framework
			Meterpreter
			ProxyChains
			SMB
			FTP
		        SSH
			Telnet
			HTTP
			MySQL
			PostgreSQL
			NFS
			Tomcat  
			
			
| Finding                          | Category               | Status     |
| -------------------------------- | ---------------------- | ---------- |
| SMB Usermap Script Vulnerability | Remote Code Execution  | Validated  |
| Java RMI Exposure                | Remote Code Execution  | Validated  |
| Unauthenticated Bind Shell       | Unauthorized Access    | Validated  |
| Weak/Default Credentials         | Authentication         | Validated  |
| NFS Misconfiguration             | Access Control         | Identified |
| SMTP User Enumeration            | Information Disclosure | Identified |
| Internal Network Exposure        | Network Security       | Validated  |

Pivoting Demonstration

A Windows 10 client was used as the pivot host to access the isolated
10.10.10.0/24 network.

The internal target 10.10.10.130 was successfully reached through
the pivot using ProxyChains.

Evidence

Evidence is organized under:

08-Evidence/Recon
08-Evidence/Enumeration
08-Evidence/Exploitation
08-Evidence/Pivoting

See 08-Evidence/Evidence-Index.md for the complete mapping.

Remediation

Recommended controls include:

Remove vulnerable/obsolete services
Patch exposed services
Replace default credentials
Restrict unnecessary network access
Apply network segmentation
Harden SMB configuration
Review NFS exports and access controls
Disable unnecessary enumeration services
Monitor lateral movement and suspicious authentication activity
Retest

After remediation, affected services and attack paths should be retested
to verify that the identified weaknesses are no longer exploitable.

Disclaimer

This project was performed in a controlled, isolated lab environment for
educational and cybersecurity portfolio purposes.



### Step 2

After creating `README.md`, create these folders:

```text
01-Project-Overview
02-Lab-Setup
03-Reconnaissance
04-Service-Enumeration
05-Vulnerability-Assessment
06-Exploitation
07-Pivoting
08-Evidence
09-Findings
10-Remediation
11-Retest
12-Reporting

