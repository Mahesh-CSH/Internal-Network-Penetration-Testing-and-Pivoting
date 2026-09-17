# F-05 — Weak PostgreSQL Credentials

## Severity
High

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
PostgreSQL — TCP/5432

## Description
PostgreSQL authentication was successfully validated using weak laboratory credentials. Database access and version information were obtained.

## Evidence
- PostgreSQL authentication screenshot
- PostgreSQL database/version enumeration screenshot

## Impact
Weak database credentials can expose databases and sensitive information and may provide additional avenues for compromise depending on account privileges.

## Recommendation
- Replace weak credentials.
- Enforce strong password policies.
- Restrict PostgreSQL access to authorized hosts.
- Apply least-privilege database permissions.
- Upgrade obsolete PostgreSQL versions.

## Status
Successfully validated in the authorized laboratory environment.
