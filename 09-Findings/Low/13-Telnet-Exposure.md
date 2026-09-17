# F-13 — Telnet Service Exposure

## Severity
Low

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
Telnet — TCP/23

## Description
A Telnet service was exposed and successfully accessed during controlled testing.

## Evidence
- Telnet enumeration screenshot
- Telnet shell screenshot

## Impact
Telnet does not provide modern encrypted communication and can expose authentication and session information.

## Recommendation
- Disable Telnet.
- Replace it with SSH.
- Restrict remote administration access.

## Status
Validated in the authorized laboratory environment.
