# 14 - Disaster Recovery

## DR Model

Document whether the system uses:

- Backup/restore
- Pilot light
- Warm standby
- Active/passive
- Active/active

## Example

```text
Primary Region
      |
      | Replication
      v
Secondary Region

Failure
  |
  v
DNS / Traffic Switch
  |
  v
Secondary Region
```

## DR Requirements

| Requirement | Value | Status |
|---|---|---|
| RTO | 4 hours | ⚠️ Assumption |
| RPO | 1 hour | ⚠️ Assumption |
| Secondary Region | Unknown | ❓ |

Do not turn business requirements into technical facts without evidence.
