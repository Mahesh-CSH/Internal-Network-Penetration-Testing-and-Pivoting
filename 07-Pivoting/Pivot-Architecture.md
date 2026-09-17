# Pivot Architecture

## Objective

Demonstrate controlled access from Kali Linux to an isolated internal
network through a dual-homed Windows 10 pivot host.

## Network Path

		Kali Linux
		192.168.88.1xx
		      |
		      | Attacker Network
		      v
		Windows 10
		192.168.88.136
		10.10.10.128
		      |
		      | Internal Network
		      v
		Metasploitable 2
		10.10.10.130
