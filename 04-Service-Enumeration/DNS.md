# DNS Enumeration

## Target

`10.10.10.130`

## Service

- TCP/53 — BIND 9.4.2

## Findings

A legacy BIND DNS service was identified.

## Security Considerations

- Upgrade unsupported DNS software.
- Restrict zone-transfer and administrative access.
- Expose only required DNS functionality.
