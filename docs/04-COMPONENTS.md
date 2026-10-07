# 04 - Components

Document each major component independently.

## Component Template

### Component: Orders API

| Property | Value |
|---|---|
| Type | Backend API |
| Technology | Node.js / TypeScript |
| Responsibility | Order processing |
| Repository | `src/orders-api` |
| Port | 8080 |
| Owner | ❓ Unknown |
| Status | Production |

### Responsibilities

- Validate requests
- Authenticate users
- Persist orders
- Publish events

### Dependencies

| Dependency | Purpose | Required? |
|---|---|---|
| PostgreSQL | Persistent data | Yes |
| Message Queue | Events | Yes |
| Identity Provider | Authentication | Yes |

### Failure Behavior

Document what happens if each dependency is unavailable.

Example:

```text
PostgreSQL unavailable
        |
        v
API cannot persist orders
        |
        v
Return controlled error
        |
        v
Alert operations team
```
