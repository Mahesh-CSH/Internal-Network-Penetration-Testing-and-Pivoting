# F-11 — Unnecessary Network Services

## Severity
Medium

## Affected Host
Metasploitable 2 — 10.10.10.130

## Description
The target exposed numerous legacy network services, including FTP, Telnet, IRC, VNC, RPC-related services, and database services.

## Evidence
- Full TCP enumeration screenshot

## Impact
Unnecessary services increase the exposed attack surface and provide additional opportunities for unauthorized access.

## Recommendation
- Disable services that are not required.
- Restrict management services to trusted networks.
- Apply firewall rules and network segmentation.
- Maintain an approved service inventory.

## Status
Identified during the authorized laboratory assessment.
