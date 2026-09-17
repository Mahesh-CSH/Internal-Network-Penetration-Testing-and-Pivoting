# F-08 — SMTP User Enumeration

## Severity
Medium

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
SMTP — TCP/25

## Description
SMTP VRFY functionality allowed valid usernames to be enumerated.

## Evidence
- SMTP enumeration screenshot

## Impact
Username disclosure can provide useful information for subsequent authentication attacks.

## Recommendation
- Disable VRFY/EXPN where not required.
- Restrict SMTP enumeration functionality.
- Monitor suspicious enumeration activity.

## Status
Validated in the authorized laboratory environment.
