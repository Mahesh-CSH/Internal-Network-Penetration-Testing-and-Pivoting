# Findings Summary

## Overview

The assessment identified weaknesses across network services,
authentication, access control, legacy software, and network exposure.

## Findings

|  ID  |            Finding                  | Severity | Status     |
|------|-------------------------------------|----------|------------|
| F-01 | Windows Pivot Host Compromise       | Critical | Validated  |
| F-02 | SMB Remote Code Execution           | Critical | Validated  |
| F-03 | Java RMI Remote Code Execution      | High     | Validated  |
| F-04 | Exposed Bind Shell / Root Access    | High     | Validated  |
| F-05 | Weak PostgreSQL Credentials         | High     | Validated  |
| F-06 | Tomcat Default Credentials          | High     | Validated  |
| F-07 | Anonymous FTP Access                | Medium   | Validated  |
| F-08 | SMTP User Enumeration               | Medium   | Identified |
| F-09 | NFS Access-Control Misconfiguration | Medium   | Identified |
| F-10 | MySQL Network Exposure              | Medium   | Validated  |
| F-11 | Unnecessary Network Services        | Medium   | Identified |
| F-12 | Service Version Disclosure          | Low      | Identified |
| F-13 | Telnet Service Exposure             | Low      | Validated  |
| F-14 | Web Directory/Application Exposure  | Low      | Identified |

## Assessment Conclusion

The testing demonstrated multiple weaknesses in the legacy internal
target and demonstrated how compromise of a dual-homed Windows host
could provide access to an isolated internal network.
