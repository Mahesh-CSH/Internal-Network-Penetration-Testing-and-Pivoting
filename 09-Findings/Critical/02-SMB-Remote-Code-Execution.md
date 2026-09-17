# F-02 — SMB Remote Code Execution

## Severity
Critical

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
SMB — TCP/139, TCP/445

## Description
The SMB service on the Metasploitable 2 host was identified as vulnerable. An SMB-based remote code execution exploit was successfully validated in the authorized laboratory environment.

## Evidence
- SMB enumeration screenshot
- SMB exploitation screenshot showing successful root shell
- PIVOT-02-SMB-Through-Pivot.png

## Impact
Successful exploitation can allow an attacker to execute commands remotely and obtain unauthorized access to the target system.

## Recommendation
- Upgrade or replace vulnerable Samba versions.
- Disable SMB services that are not required.
- Restrict SMB access using firewall rules and network segmentation.
- Monitor SMB authentication and suspicious remote command execution.
- Apply current security updates.

## Status
Successfully exploited and validated in the authorized laboratory environment.
