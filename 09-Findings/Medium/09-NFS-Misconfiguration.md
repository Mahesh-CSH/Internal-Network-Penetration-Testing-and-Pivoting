# F-09 — NFS Access-Control Misconfiguration

## Severity
Medium

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
NFS — TCP/2049

## Description
The NFS configuration exposed the root filesystem with read/write access and `no_root_squash`.

## Evidence
- NFS export enumeration screenshot
- NFS configuration screenshot

## Impact
Improper NFS export configuration can allow unauthorized users to access or modify files with excessive privileges.

## Recommendation
- Restrict NFS exports to required hosts.
- Remove `no_root_squash` where unnecessary.
- Use least-privilege permissions.
- Restrict NFS access using network controls.

## Status
Configuration weakness identified during the authorized laboratory assessment.
