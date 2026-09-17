# F-10 — MySQL Network Exposure

## Severity
Medium

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
MySQL — TCP/3306

## Description
The MySQL database service was directly accessible during controlled testing. Database and user enumeration were performed.

## Evidence
- MySQL version/database enumeration screenshot
- MySQL user enumeration screenshot

## Impact
Network-exposed database services increase the attack surface and can expose sensitive data if authentication or authorization controls are weak.

## Recommendation
- Restrict MySQL access to authorized hosts.
- Upgrade obsolete MySQL software.
- Remove unnecessary accounts.
- Enforce strong authentication.

## Status
Validated in the authorized laboratory environment.
