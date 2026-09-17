# SMTP Enumeration

## Target

`10.10.10.130`

## Service

- TCP/25 — SMTP / Postfix

## Findings

SMTP user enumeration was possible through VRFY requests.

Multiple valid usernames were identified during testing.

## Security Considerations

- Disable unnecessary VRFY/EXPN functionality.
- Restrict SMTP enumeration.
- Apply appropriate mail-server access controls.
