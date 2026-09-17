# Metasploitable 2 Enumeration

## Target

		IP Address: 10.10.10.130

Full TCP Enumeration
  A full TCP service scan was performed to identify exposed services.

#Identified Services

| Port | Service     |
| ---: | ----------- |
|   21 | FTP         |
|   22 | SSH         |
|   23 | Telnet      |
|   25 | SMTP        |
|   53 | DNS         |
|   80 | HTTP        |
|  111 | RPCbind     |
|  139 | NetBIOS/SMB |
|  445 | SMB         |
| 1099 | Java RMI    |
| 1524 | Bind Shell  |
| 2049 | NFS         |
| 2121 | FTP         |
| 3306 | MySQL       |
| 3632 | DistCC      |
| 5432 | PostgreSQL  |
| 5900 | VNC         |
| 6000 | X11         |
| 6667 | IRC         |
| 6697 | IRC         |
| 8009 | AJP         |
| 8180 | Tomcat      |
| 8787 | DRb         |

##Enumeration Tools

		Nmap
		Gobuster
		Netcat
		Metasploit Framework
		Service-specific enumeration utilities

The identified services were subsequently reviewed for security
weaknesses and controlled exploitation opportunities.
