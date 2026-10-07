# Runbook — `<procedure or symptom>`

> Use this for a repeatable operational task or incident pattern. Include only verified commands and procedures. Link to the system overview, deployment guide, and escalation path.

## Document Control

| Field | Value |
|---|---|
| System / component | `<name>` |
| Owner / escalation team | `<team and contact path>` |
| Last tested / reviewed | `<YYYY-MM-DD or Unknown>` |
| Related documentation | `<links>` |

## Purpose and Scope

`<What does this procedure accomplish, and when should it be used?>`

## Symptoms and Impact

| Symptom / alert | User or business impact | Severity / trigger |
|---|---|---|
| `<observable symptom>` | `<impact>` | `<verified threshold or Unknown>` |

## Preconditions and Safety

- Required role / approval: `<verified requirement or Unknown>`
- Maintenance window or user impact: `<details>`
- Dependencies / checks before starting: `<details>`
- Safety or data-loss warning: `<details>`

## Diagnosis

1. `<Check the relevant alert, dashboard, or log. Link to it.>`
2. `<Run a verified, read-only diagnostic command or query.>`
3. `<Check dependencies and recent changes.>`

| Check | Expected result | If not, see |
|---|---|---|
| `<check>` | `<verified result>` | `<next step or escalation>` |

## Procedure

1. `<Action, including the approved tool or command.>`
2. `<Expected result and validation.>`
3. `<Record the action and outcome.>`

## Recovery / Rollback

`<Provide the verified recovery or rollback steps, or state Unknown and identify the owner who must validate them.>`

## Validation

- [ ] `<Health or service check>`
- [ ] `<User-facing operation or smoke test>`
- [ ] `<Monitoring / error-rate confirmation>`

## Escalation

| Trigger | Team / role | Contact path | Information to provide |
|---|---|---|---|
| `<condition>` | `<team>` | `<approved contact path>` | `<logs, timestamps, change reference>` |

## Change and Incident Notes

| Date | What happened / changed? | Evidence or incident reference | Follow-up owner |
|---|---|---|---|
| `<YYYY-MM-DD>` | `<summary>` | `<link>` | `<owner>` |
