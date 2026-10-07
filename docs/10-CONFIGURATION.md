# 10 - Configuration

Separate configuration from secrets.

## Example

```text
APP_ENV=production
API_PORT=8080
DATABASE_HOST=<secret/configuration source>
DATABASE_PASSWORD=<secret manager>
```

## Configuration Matrix

| Setting | Dev | Test | Prod | Source |
|---|---|---|---|---|
| APP_ENV | development | test | production | Environment |
| API_PORT | 8080 | 8080 | 8080 | App config |
| DB Host | Different | Different | Different | Secret/config store |

## Rules

- Never commit secrets.
- Document where secrets are stored.
- Document who can access them.
- Document rotation procedures.
