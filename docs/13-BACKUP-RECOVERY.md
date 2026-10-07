# 13 - Backup & Recovery

## Backup Inventory

| System | Backup | Frequency | Retention | Status |
|---|---|---|---|---|
| Database | ❓ | ❓ | ❓ | Unknown |
| Files | ❓ | ❓ | ❓ | Unknown |
| Configuration | Git | Every change | Repository policy | ✅ |

## Recovery Questions

- What is the RPO?
- What is the RTO?
- Where are backups stored?
- Are backups encrypted?
- Are backups isolated from production?
- When was the last restore test?

## Critical Rule

A backup is not proven until a restore has been tested.

Prefer:

> Last verified restore test: 2026-XX-XX

over:

> Backups are working.
