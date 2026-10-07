# 01 - Project Discovery

## Purpose

Project Discovery is the first step when documenting a project you do not understand yet.

The goal is to answer:

1. What is this project?
2. Why does it exist?
3. Who uses it?
4. What technologies does it use?
5. How is it deployed?
6. What does it depend on?
7. What is still unknown?

## Discovery Template

### Project Identity

| Field | Value | Status |
|---|---|---|
| Project Name | `Example Orders API` | ✅ Confirmed |
| Business Purpose | Processes customer orders | ✅ Confirmed |
| Owner | Platform Team | ❓ Unknown |
| Repository | `company/orders-api` | ✅ Confirmed |
| Production URL | `https://api.example.com` | ⚠️ Assumption |

### Technology

| Area | Finding | Status |
|---|---|---|
| Frontend | React | ✅ Confirmed |
| Backend | Node.js / TypeScript | ✅ Confirmed |
| Database | PostgreSQL | ✅ Confirmed |
| Cloud | Azure | ⚠️ Assumption |
| CI/CD | GitHub Actions | ✅ Confirmed |

## Discovery Questions

### Business

- What problem does the system solve?
- Who are the users?
- What business process depends on it?
- What happens if the system is unavailable?

### Technical

- What are the main services?
- What database is used?
- Which APIs are exposed?
- Which external systems are required?
- Where are secrets stored?

### Operational

- How is it deployed?
- How is it monitored?
- Who receives alerts?
- How are backups performed?
- What is the recovery procedure?

## Unknown Register

| ID | Unknown | Impact | How to Validate |
|---|---|---|---|
| U-001 | Production owner | High | Ask platform team |
| U-002 | RTO | High | Check DR/business continuity docs |
| U-003 | Database backup frequency | High | Check backup configuration |

## Example Discovery Result

```text
Confirmed:
- Backend is Node.js.
- Database is PostgreSQL.
- CI/CD uses GitHub Actions.

Assumptions:
- Azure App Service appears to host the API based on deployment workflow.

Unknown:
- Production RTO/RPO.
- Database backup retention.
- API rate limits.
```
