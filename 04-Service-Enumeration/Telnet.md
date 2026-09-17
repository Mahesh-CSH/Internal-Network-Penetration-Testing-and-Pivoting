# Telnet Enumeration

## Target

`10.10.10.130`

## Service

- TCP/23 — Telnet

## Findings

Telnet was exposed and valid laboratory credentials were used to
obtain a shell during controlled testing.

## Security Considerations

Telnet transmits credentials and session data without modern
encryption.

- Disable Telnet.
- Replace it with SSH.
- Restrict remote administration access.
