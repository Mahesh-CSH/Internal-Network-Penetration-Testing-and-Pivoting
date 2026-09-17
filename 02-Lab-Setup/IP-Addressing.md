# IP Addressing

|     Machine      |  Network | IP Address     | Purpose                   |
|------------------|----------|----------------|---------------------------|
| Kali Linux       | NAT      | 192.168.88.1xx | Attacker                  |
| Windows 10       | NAT      | 192.168.88.136 | Attacker-facing interface |
| Windows 10       | Internal | 10.10.10.128   | Pivot interface           |
| Metasploitable 2 | Internal | 10.10.10.130   | Internal target           |

## Internal Network

		Network: 10.10.10.0/24
		Windows Pivot: 10.10.10.128
		Metasploitable 2: 10.10.10.130
		
		
Pivot Path

		192.168.88.1xx
		      |
		      v
		192.168.88.136
		Windows 10
		10.10.10.128
		      |
		      v
		10.10.10.130
		Metasploitable 2
