# Pivot Route Configuration

## Internal Network

		Network: 10.10.10.0/24
		Netmask: 255.255.255.0

#Route

The internal network route was added through the active Meterpreter
session.

##The route was verified as:

10.10.10.0/24
Gateway: Meterpreter Session 2


##Result

Traffic destined for the internal 10.10.10.0/24 network could be
routed through the Windows pivot host.
