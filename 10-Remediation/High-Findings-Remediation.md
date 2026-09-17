# High Findings Remediation

## F-03 — Java RMI Remote Code Execution

- Upgrade or remove vulnerable Java RMI services.
- Restrict RMI access to trusted hosts.
- Apply network firewall controls.
- Disable unnecessary remote interfaces.
- Keep Java and associated applications patched.
- Monitor unusual RMI connections.

## F-04 — Bind Shell Root Access

- Remove exposed bind-shell services.
- Disable unnecessary listening ports.
- Prevent services from running with root privileges.
- Apply host firewall rules.
- Investigate why the service was exposed.
- Use least privilege for application services.

## F-05 — PostgreSQL Weak Credentials

- Replace weak/default credentials.
- Use strong unique passwords.
- Restrict PostgreSQL access to trusted hosts.
- Configure `pg_hba.conf` securely.
- Disable unnecessary remote database access.
- Avoid using privileged database accounts for normal applications.

## F-06 — Tomcat Default Credentials

- Immediately remove default credentials.
- Create strong unique administrative credentials.
- Restrict the Tomcat Manager application.
- Disable unnecessary management interfaces.
- Upgrade unsupported Tomcat versions.
- Restrict administrative access using network controls.
