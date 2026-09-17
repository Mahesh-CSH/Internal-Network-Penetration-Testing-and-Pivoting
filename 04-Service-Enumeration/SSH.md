# SSH Enumeration

## Target

`10.10.10.130`

## Service

- TCP/22 — OpenSSH 4.7p1

## Findings

An SSH service running an obsolete OpenSSH version was identified.

## Security Considerations

- Upgrade OpenSSH.
- Disable weak authentication methods.
- Restrict SSH access to authorized hosts.
