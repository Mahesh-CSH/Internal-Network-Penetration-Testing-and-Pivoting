# Critical Findings Remediation

## F-01 — Windows Pivot Host Compromise

### Recommended Remediation

- Keep Windows fully patched.
- Enable Windows Defender and real-time protection.
- Enable and properly configure Windows Firewall.
- Remove unnecessary software and services.
- Restrict inbound connections to required ports only.
- Apply least-privilege access.
- Use strong unique passwords.
- Monitor suspicious executable and PowerShell activity.
- Restrict administrative privileges.
- Prevent unauthorized remote access.

### Network Controls

The Windows system should not provide unnecessary access between network segments.

Only explicitly required communication should be permitted between the attacker-facing and internal network interfaces.

### Validation

After remediation:

- Confirm firewall configuration.
- Confirm endpoint protection is enabled.
- Confirm unnecessary ports are closed.
- Verify that the previous attack path cannot be reproduced.
