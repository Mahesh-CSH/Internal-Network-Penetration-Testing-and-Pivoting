# Executive Summary

## Assessment

An internal network penetration testing and pivoting assessment was conducted in an isolated lab environment.

The assessment evaluated network exposure, service configuration, authentication controls, exploitation opportunities, and lateral movement through a compromised Windows pivot host.

## Environment

The lab consisted of:

- Kali Linux — Attacker
- Windows 10 — Pivot Host
- Metasploitable 2 — Internal Target

## Key Activities

- Network reconnaissance
- Full-port scanning
- Service enumeration
- Vulnerability identification
- Exploitation validation
- Windows host compromise
- Internal network pivoting
- Internal service enumeration
- Security findings documentation
- Remediation recommendations

## Major Findings

The assessment demonstrated multiple security weaknesses, including:

- SMB remote code execution
- Java RMI exposure
- Root-level bind shell access
- Weak PostgreSQL credentials
- Tomcat default credentials
- Anonymous FTP access
- NFS misconfiguration
- Database exposure
- Telnet exposure
- Unnecessary network services

## Pivoting

A compromised Windows host was successfully used as a pivot point to access the isolated internal network.

The pivot demonstrated how compromise of an intermediate host can provide access to otherwise unreachable internal services.

## Retest

A post-remediation retest was not performed as part of this lab.

## Overall Objective

The project demonstrates practical internal penetration-testing methodology, exploitation, lateral movement, pivoting, evidence collection, and security remediation planning.
