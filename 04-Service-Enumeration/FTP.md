# FTP Enumeration

## Target

`10.10.10.130`

## Ports

- TCP/21 — FTP
- TCP/2121 — ProFTPD

## Findings

The FTP service on TCP/21 was identified as vsftpd 2.3.4.
Anonymous FTP access was verified.

The service was reviewed for known vulnerabilities during the
vulnerability assessment phase.

A separate ProFTPD service was identified on TCP/2121 and was
enumerated independently.

## Security Considerations

- Disable anonymous access when not required.
- Upgrade obsolete FTP software.
- Prefer secure file-transfer protocols.
