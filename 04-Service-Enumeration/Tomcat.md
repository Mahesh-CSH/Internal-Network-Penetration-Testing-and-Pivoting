# Apache Tomcat Enumeration

## Target

`10.10.10.130`

## Services

- TCP/8009 — AJP
- TCP/8180 — HTTP

## Findings

Apache Tomcat was identified on TCP/8180.

Web enumeration identified administrative and example endpoints,
including:

- `/admin/`
- `/manager/`
- `/host-manager/`
- `/jsp-examples/`
- `/servlets-examples/`
- `/tomcat-docs/`

The laboratory Tomcat installation was also found to accept
default credentials during controlled testing.

## Security Considerations

- Remove default credentials.
- Upgrade obsolete Tomcat versions.
- Remove example applications.
- Restrict administrative interfaces.
- Restrict AJP exposure.
