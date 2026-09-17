# Lab Architecture

## Network Diagram

                    Kali Linux
                  192.168.88.129
                         |
                         |
                  Windows 10 Client
                  192.168.88.136
                   10.10.10.128
                         |
                    Pivot Host
                         |
                  10.10.10.0/24
                         |
                         |
                 Metasploitable 2
                   10.10.10.130
                   
                   
Network Interfaces

		Kali Linux
			NAT: 192.168.88.129
			Internal network: 10.10.10.129
		Windows 10 Client
			NAT: 192.168.88.136
			Internal network: 10.10.10.128
		Metasploitable 2
			Internal network: 10.10.10.130
			
Pivot Path

		Kali
		  ↓
		Windows 10
		  ↓
		10.10.10.0/24
		  ↓
		Metasploitable 2
		
		
	
