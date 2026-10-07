# 05 - Data Flow

## Purpose

Explain how data moves through the system.

## Example

```text
User
 |
 | HTTPS
 v
Web App
 |
 | REST/JSON
 v
Orders API
 |
 | SQL
 v
PostgreSQL

Orders API
 |
 | Event
 v
Message Queue
 |
 v
Fulfillment Worker
```

## Data Flow Table

| Step | Source | Destination | Protocol | Data |
|---|---|---|---|---|
| 1 | Browser | API | HTTPS | Order JSON |
| 2 | API | Database | PostgreSQL | Order record |
| 3 | API | Queue | AMQP | Order event |
| 4 | Worker | External system | HTTPS | Fulfillment request |

## Questions

- Is data encrypted in transit?
- Is sensitive data stored?
- How long is it retained?
- Is PII involved?
- Where is data replicated?
