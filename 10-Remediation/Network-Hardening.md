# Network Hardening

## Network Segmentation

Separate user, server, database, and management networks where possible.

## Firewall Controls

Allow only required communication between network segments.

Example:


		Internet / User Network
			|
	            Firewall
			|
		   Server Network
			|
		     Database


#Internal Services

Restrict access to:

		SMB
		SSH
		FTP
		Telnet
		Databases
		Tomcat Manager
		Java RMI
		NFS
                Administrative interfaces

Only authorized hosts should be able to communicate with these services.

##Lateral Movement Protection

		Segment critical systems.
		Restrict SMB between workstations.
		Disable unnecessary administrative protocols.
		Monitor authentication activity.
		Use strong privileged-account controls.
		Implement endpoint detection and response.
		
##Monitoring

Monitor:

		Failed authentication
		Successful privileged authentication
		New services
		Unusual network connections
		Suspicious PowerShell activity
		Remote administration
		Lateral movement attempts
		
# Security Hardening Checklist

## Windows

- [ ] Windows fully patched
- [ ] Windows Firewall enabled
- [ ] Defender enabled
- [ ] Real-time protection enabled
- [ ] Unnecessary services disabled
- [ ] Strong passwords configured
- [ ] Least privilege enforced
- [ ] Unnecessary ports closed

## Linux / Metasploitable-style Services

- [ ] Anonymous FTP disabled
- [ ] Telnet disabled
- [ ] Unnecessary services removed
- [ ] Bind shells removed
- [ ] NFS exports restricted
- [ ] `no_root_squash` removed where unnecessary
- [ ] Database access restricted

## Databases

- [ ] Strong PostgreSQL credentials
- [ ] Strong MySQL credentials
- [ ] Remote database access restricted
- [ ] Privileged accounts protected
- [ ] Database services patched

## Web Services

- [ ] Tomcat updated
- [ ] Default credentials removed
- [ ] Manager interface restricted
- [ ] Test applications removed
- [ ] Directory listing disabled

## Network

- [ ] Network segmentation implemented
- [ ] Firewall rules reviewed
- [ ] Internal lateral movement restricted
- [ ] Administrative services restricted
- [ ] Unnecessary ports closed

## Monitoring

- [ ] Authentication logging enabled
- [ ] Endpoint monitoring enabled
- [ ] Network monitoring enabled
- [ ] Security events reviewed regularly
