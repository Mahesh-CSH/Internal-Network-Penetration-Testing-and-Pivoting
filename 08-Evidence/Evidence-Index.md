# Evidence Index

## Purpose

This index maps the assessment findings and attack activities to their
corresponding evidence screenshots.

---

## Reconnaissance

| ID | Evidence | Description |

| RECON-01 | `RECON-01-Metasploitable2-Full-Port-Scan.png` | Metasploitable 2 service discovery |
| RECON-02 | `RECON-02-Windows10-Full-Port-Scan.png` | Windows 10 service discovery |

---

## Enumeration

| ID | Evidence | Description |

| ENUM-01 | `ENUM-01-SMB-Enumeration.png` | SMB service and share enumeration |
| ENUM-02 | `ENUM-02-SMTP-Enumeration.png` | SMTP user enumeration |
| ENUM-03 | `ENUM-03-NFS-Exports.png` | NFS export configuration |
| ENUM-04 | `ENUM-04-MySQL-Enumeration.png` | MySQL enumeration |
| ENUM-05 | `ENUM-05-PostgreSQL-Enumeration.png` | PostgreSQL access and enumeration |
| ENUM-06 | `ENUM-06-Tomcat-Enumeration.png` | Tomcat web enumeration |
| ENUM-07 | `ENUM-07-HTTP-Gobuster.png` | Web directory enumeration |

---

## Exploitation

| ID | Evidence | Description |

| EXP-01 | `EXP-01-Samba-Root-Shell.png` | Root shell obtained through Samba exploitation |
| EXP-02 | `EXP-02-Java-RMI-Meterpreter.png` | Meterpreter session through Java RMI |
| EXP-03 | `EXP-03-Bind-Shell-Root.png` | Root shell through exposed bind shell |
| EXP-04 | `EXP-04-Telnet-Shell.png` | Telnet shell access |
| EXP-05 | `EXP-05-PostgreSQL-Access.png` | PostgreSQL authentication validation |
| EXP-06 | `EXP-06-Tomcat-Default-Credentials.png` | Tomcat administrative credential validation |

---

## Pivoting

| ID | Evidence | Description |

| PIVOT-01 | `PIVOT-01-Meterpreter-Session.png` | Windows Meterpreter session |
| PIVOT-02 | `PIVOT-02-Meterpreter-Route.png` | Internal route through Windows |
| PIVOT-03 | `PIVOT-03-Internal-Target-Through-Windows.png` | Internal target reached through pivot |
| PIVOT-04 | `PIVOT-04-SMB-Through-Windows-Pivot.png` | SMB service validated through pivot |

---

## Evidence Handling

Screenshots are provided for educational and portfolio documentation.

Sensitive credentials, session tokens, or unrelated private information
should be redacted before public repository publication.
