# 12 - Monitoring

## What to Monitor

### Availability

- Health endpoint
- HTTP availability
- Dependency availability

### Performance

- CPU
- Memory
- Latency
- Throughput

### Application

- Error rate
- Failed jobs
- Queue depth
- Authentication failures

## Alert Example

```text
Condition:
HTTP 5xx rate > 5% for 5 minutes

Action:
1. Create alert
2. Notify on-call
3. Check application logs
4. Check dependencies
5. Follow incident runbook
```

## Unknowns

Do not claim monitoring exists until the actual configuration has been verified.
