# 17 - Documentation Review

Documentation should be reviewed against the actual system.

## Review Checklist

### Accuracy

- [ ] Architecture matches implementation
- [ ] Component list is complete
- [ ] APIs match actual endpoints
- [ ] Deployment steps are current
- [ ] Configuration is current
- [ ] Security controls are verified

### Operations

- [ ] Monitoring documented
- [ ] Alerts documented
- [ ] Backup documented
- [ ] Restore tested
- [ ] Troubleshooting documented
- [ ] DR documented

### AI Review Prompt

> Review this documentation against the repository and infrastructure evidence. Identify:
>
> 1. Statements that are unsupported.
> 2. Statements that contradict the code.
> 3. Missing components.
> 4. Missing dependencies.
> 5. Missing security controls.
> 6. Missing operational procedures.
> 7. Assumptions incorrectly presented as facts.
>
> Classify every finding as Confirmed, Assumption, or Unknown and provide the evidence or validation method.

## Final Quality Gate

A documentation set is ready when another engineer can:

- Understand the system.
- Deploy it.
- Operate it.
- Troubleshoot common failures.
- Understand its dependencies.
- Understand its security model.
- Recover it after a failure.
