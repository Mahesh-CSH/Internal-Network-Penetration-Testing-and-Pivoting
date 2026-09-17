# F-04 — Exposed Bind Shell / Root Access

## Severity
High

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
TCP/1524

## Description
An exposed bind shell was identified on TCP/1524. Controlled testing successfully established a shell with root-level privileges.

## Evidence
- Bind shell connection screenshot
- Root privilege verification screenshot

## Impact
An exposed privileged shell can provide complete unauthorized control of the affected system.

## Recommendation
- Remove the bind-shell service.
- Disable unnecessary listening services.
- Restrict inbound connections with host-based firewall rules.
- Monitor unexpected listening ports.

## Status
Successfully validated in the authorized laboratory environment.
