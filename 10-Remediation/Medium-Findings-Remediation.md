# Medium Findings Remediation

## F-07 — FTP Anonymous Access

- Disable anonymous FTP if not required.
- Require authenticated access.
- Restrict write permissions.
- Prefer SFTP/SSH for secure file transfer.
- Restrict FTP access using firewall rules.

## F-08 — SMTP User Enumeration

- Disable unnecessary SMTP user-enumeration functionality.
- Restrict SMTP commands where possible.
- Apply anti-enumeration configuration.
- Monitor suspicious SMTP requests.

## F-09 — NFS Misconfiguration

- Remove unnecessary NFS exports.
- Avoid exporting the entire filesystem.
- Remove `no_root_squash` unless specifically required.
- Restrict exports to trusted hosts/networks.
- Apply least-privilege filesystem permissions.

## F-10 — MySQL Exposure

- Restrict MySQL access to trusted systems.
- Disable remote access when unnecessary.
- Use strong database credentials.
- Avoid wildcard host access where possible.
- Apply firewall restrictions.
- Keep MySQL patched.

## F-11 — Unnecessary Network Services

- Disable services that are not required.
- Remove legacy protocols.
- Restrict administrative services.
- Apply host and network firewall rules.
- Regularly review listening ports.
