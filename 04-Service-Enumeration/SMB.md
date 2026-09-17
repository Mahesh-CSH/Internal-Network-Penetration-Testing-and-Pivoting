# SMB Enumeration

## Target

`10.10.10.130`

## Services

- TCP/139 — NetBIOS/SMB
- TCP/445 — SMB
- Samba 3.0.20

## Findings

The following shares were identified during enumeration:

- `print$`
- `tmp`
- `opt`
- `IPC$`
- `ADMIN$`

The Samba service was subsequently validated for the usermap-script
vulnerability during exploitation.

## Security Considerations

- Upgrade Samba.
- Remove unnecessary shares.
- Restrict anonymous access.
- Apply least-privilege permissions.
