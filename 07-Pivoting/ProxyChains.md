# ProxyChains Internal Network Validation

## Objective

Validate access to the internal Metasploitable 2 system through the
established pivot.

## Target

        10.10.10.130

#Validation

ProxyChains was used to route Nmap traffic through the pivot.

The internal target was successfully reached and multiple services
were identified, including:

21/tcp   FTP
22/tcp   SSH
23/tcp   Telnet
80/tcp   HTTP
139/tcp  NetBIOS
445/tcp  SMB
3306/tcp MySQL
5432/tcp PostgreSQL
8180/tcp HTTP


##Result

The test demonstrated that Kali could access the internal target
through the Windows pivot rather than through a direct internal
network interface.
