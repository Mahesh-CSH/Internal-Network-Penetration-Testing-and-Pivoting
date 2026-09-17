# NFS Enumeration

## Target

`10.10.10.130`

## Service

- TCP/2049 — NFS

## Findings

NFS exports were identified during enumeration.

The export configuration included:

`/*(rw,sync,no_root_squash,no_subtree_check)`

This configuration presents a significant access-control risk.

## Security Considerations

- Restrict exports to required hosts.
- Remove `no_root_squash` where unnecessary.
- Use least-privilege export permissions.
