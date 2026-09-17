# F-14 — Web Directory and Application Exposure

## Severity
Low

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
HTTP — TCP/80

## Description
Web enumeration identified multiple accessible directories and applications, including documentation, testing, CGI, and phpMyAdmin-related paths.

## Evidence
- HTTP enumeration screenshot
- Gobuster directory enumeration screenshot

## Impact
Unnecessary directories and applications can expose information or increase the web application's attack surface.

## Recommendation
- Remove unnecessary directories and applications.
- Restrict administrative functionality.
- Disable directory listings where unnecessary.
- Upgrade obsolete web software.

## Status
Identified during the authorized laboratory assessment.
