# 15 - Troubleshooting

## Troubleshooting Method

Use:

**Observe → Reproduce → Isolate → Verify → Fix → Validate → Document**

Troubleshooting supports diagnosis and recovery while an issue is active. After a significant incident, capture organizational learning and follow-up actions separately using the [Incident Learning guide](20-INCIDENT-LEARNING.md) and [postmortem template](../templates/postmortem.md).

## Example: API Returns 500

### 1. Observe

Check:

- Application logs
- Metrics
- Recent deployments
- Dependency health

### 2. Isolate

Determine whether the problem is:

- Application
- Database
- Network
- Authentication
- External dependency

### 3. Verify

Example:

```bash
curl -I https://api.example.com/health
```

### 4. Fix

Apply the approved remediation.

### 5. Validate

Confirm:

- Error rate returned to normal
- Health endpoint is healthy
- Users can complete the affected operation

### 6. Document

Add the incident pattern to this file.

## Troubleshooting Table

| Symptom | Possible Cause | Validation |
|---|---|---|
| 500 errors | Database unavailable | Check DB connectivity |
| Slow requests | High CPU | Check metrics |
| 401 | Token issue | Validate identity configuration |
