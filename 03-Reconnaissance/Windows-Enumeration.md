# Windows 10 Enumeration

## Target
		NAT IP:      192.168.88.136
		Internal IP: 10.10.10.128

##Port Scan
A full TCP scan was performed against the Windows 10 laboratory system.

##Identified Services
|        Port | Service / Function |
| ----------: | ------------------ |
|         135 | MSRPC              |
|         139 | NetBIOS            |
|         445 | SMB                |
|        5040 | Unknown service    |
| 49664-49670 | Windows RPC        |
|       58293 | Windows RPC        |

#SMB Enumeration

SMB was identified on TCP/445.

The Windows host was identified as Windows 10 / Windows Server
build 19041 during service enumeration.

SMB 1 was not enabled.

SMB signing was identified as enabled but not required.

#Pivot Role
The Windows system was configured with two network interfaces:

		192.168.88.136
		10.10.10.128

This dual-homed configuration allowed the system to act as the
controlled pivot between the attacker-facing network and the
isolated internal network.
