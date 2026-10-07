# 17 - Documentation Review

Documentation should be reviewed against the actual system.

## Review Checklist

### Accuracy

- [ ] Architecture matches implementation
- [ ] Component list is complete
- [ ] Requirements, designs, and decisions link to one another
- [ ] APIs match actual endpoints
- [ ] Deployment steps are current
- [ ] Configuration is current
- [ ] Security controls are verified
- [ ] Diagrams are current, legible, and suited to their audience
- [ ] Architecturally significant quality requirements have measurable scenarios or explicit owners for unresolved targets

### Operations

- [ ] Monitoring documented
- [ ] Alerts documented
- [ ] Backup documented
- [ ] Restore tested
- [ ] Troubleshooting documented
- [ ] DR documented
- [ ] Significant incidents have a learning review and owned follow-up actions
- [ ] Cross-cutting technical risks have owners, responses, and review dates

### Ownership and maintenance

- [ ] Each maintained artifact has a named owner or owning team
- [ ] The canonical location is clear and accessible to its audience
- [ ] Review cadence or next review date is recorded
- [ ] Changes are version-controlled so prior decisions and states can be traced
- [ ] Relevant documentation was updated with the associated code, infrastructure, or process change

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
- Find who owns each artifact and where the source of truth lives.
