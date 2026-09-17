# F-03 — Java RMI Remote Code Execution

## Severity
High

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
Java RMI — TCP/1099

## Description
The Java RMI service exposed on TCP/1099 was identified and successfully exploited in the authorized laboratory environment. A Meterpreter session was obtained on the target.

## Evidence
- Java RMI service enumeration screenshot
- Java RMI exploitation screenshot
- Meterpreter session verification screenshot

## Impact
Successful exploitation can allow remote code execution on the target system and unauthorized access to the underlying host.

## Recommendation
- Disable Java RMI if it is not required.
- Restrict TCP/1099 to trusted hosts.
- Apply security updates to Java and related applications.
- Use network segmentation and firewall rules.
- Monitor exposed Java RMI services and unexpected remote connections.

## Status
Successfully exploited and validated in the authorized laboratory environment.
