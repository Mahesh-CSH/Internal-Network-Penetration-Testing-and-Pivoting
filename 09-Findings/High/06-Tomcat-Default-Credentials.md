# F-06 — Tomcat Default Credentials

## Severity
High

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
Apache Tomcat — TCP/8180

## Description
Tomcat administrative functionality was identified during web enumeration. Default laboratory credentials were successfully validated against the administrative interface.

## Evidence
- Tomcat web enumeration screenshot
- Tomcat administrative login screenshot

## Impact
Unauthorized access to a Tomcat management interface can provide significant control over deployed applications and server functionality.

## Recommendation
- Remove all default credentials.
- Use strong, unique administrative credentials.
- Restrict management interfaces to authorized administrators.
- Remove unnecessary example applications.
- Upgrade obsolete Tomcat versions.

## Status
Successfully validated in the authorized laboratory environment.
