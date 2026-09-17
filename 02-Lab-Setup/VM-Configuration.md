# Virtual Machine Configuration

## Kali Linux

**Role:** Attacker

- Operating System: Kali Linux
- Hypervisor: VMware
- Network: NAT
- IP: `192.168.88.1xx`

## Windows 10 Client

**Role:** Pivot Host

- Operating System: Windows 10
- Hypervisor: VMware
- Network Adapter 1: NAT
- NAT IP: `192.168.88.136`
- Network Adapter 2: Internal / VMnet2
- Internal IP: `10.10.10.128`

## Metasploitable 2

**Role:** Internal Target

- Operating System: Metasploitable 2
- Hypervisor: VMware
- Network: Internal / VMnet2
- IP: `10.10.10.130`

## VMware Network

The internal laboratory network used:

		VMnet2
		10.10.10.0/24
