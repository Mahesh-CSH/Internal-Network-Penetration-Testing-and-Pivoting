# F-07 — Anonymous FTP Access

## Severity
Medium

## Affected Host
Metasploitable 2 — 10.10.10.130

## Service
FTP — TCP/21

## Description
Anonymous FTP access was successfully verified on the FTP service.

## Evidence
- FTP enumeration screenshot
- Anonymous FTP access screenshot

## Impact
Anonymous access can expose files or permit unauthorized interaction with the FTP service.

## Recommendation
- Disable anonymous access unless explicitly required.
- Restrict FTP access to authorized users.
- Replace legacy FTP with secure file-transfer mechanisms.
- Upgrade obsolete FTP software.

## Status
Validated in the authorized laboratory environment.
