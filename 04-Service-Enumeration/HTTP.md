# HTTP Enumeration

## Target

`10.10.10.130`

## Service

- TCP/80 — Apache 2.2.8
- PHP 5.2.4

## Findings

Web enumeration identified several accessible directories and
applications, including:

- `/phpMyAdmin/`
- `/test/`
- `/doc/`
- `/cgi-bin/`
- `/icons/`
- `/index/`

## Security Considerations

- Upgrade obsolete Apache/PHP versions.
- Remove unnecessary applications and directories.
- Restrict administrative interfaces.
