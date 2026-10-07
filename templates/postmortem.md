# Incident Postmortem — `<incident ID and short title>`

> Use this template after a significant incident to understand impact, improve systems and response, and track follow-up. Keep the review blameless: focus on system conditions and decisions made with the information available at the time, not individual fault. Do not include secrets or unnecessary personal/customer data.

## Document Control

| Field | Value |
|---|---|
| Incident ID | `<link to incident record>` |
| Severity | `<incident severity or Unknown>` |
| Incident start / end | `<timestamp and timezone>` |
| Review date | `<YYYY-MM-DD>` |
| Facilitator | `<name or team>` |
| Participants / impacted teams | `<names or teams>` |
| Status | `<Draft / In review / Published>` |

## Executive Summary

`<What happened, who or what was affected, how it was resolved, and what will change as a result?>`

## Customer and Business Impact

| Measure | Impact | Evidence / confidence | Unknowns and validation |
|---|---|---|---|
| `<users, requests, data, duration, business process>` | `<verified impact>` | `<source and confidence>` | `<unknown or none>` |

State the impact window, affected services or regions, and any confirmed data integrity or security impact. Mark unavailable measurements Unknown rather than estimating them without evidence.

## Detection and Response

| Item | Detail |
|---|---|
| How was the incident detected? | `<alert, customer report, operator observation, or Unknown>` |
| Time to detect / acknowledge / mitigate | `<verified durations or Unknown>` |
| Resolution / recovery | `<summary and link to runbook or incident record>` |
| Communications | `<audiences, channels, and relevant links>` |

## Timeline

Use one timezone throughout, preferably UTC. Cite a log, alert, change, or incident record for each time where possible.

| Time (timezone) | Event | Source / confidence |
|---|---|---|
| `<YYYY-MM-DD HH:MM UTC>` | `<observable event or response action>` | `<link or Unknown>` |

## What Happened

### Trigger

`<The event or condition that initiated the incident, if confirmed.>`

### Root cause and contributing conditions

`<Describe the technical and organizational conditions supported by evidence. If root cause is not established, say so and list hypotheses separately. Avoid "human error" as a stopping point; examine the system conditions, safeguards, and information available.>`

| Finding | Status | Evidence / validation |
|---|---|---|
| `<cause, contributing condition, or hypothesis>` | `<Confirmed / Assumption / Unknown>` | `<source or next validation step>` |

## Response Review

### What helped?

- `<tool, signal, process, or action>`

### What made response or recovery harder?

- `<gap, ambiguity, missing signal, or dependency>`

### What did we learn?

- `<specific learning>`

## Follow-up Actions

Actions should address contributing conditions and improve prevention, detection, mitigation, or recovery. Each action needs one accountable owner, a due date, and verifiable completion criteria.

| ID | Action | Type | Priority | Owner | Due date | Completion evidence | Status |
|---|---|---|---|---|---|---|---|
| INC-ACT-001 | `<specific change>` | `<Prevent / Detect / Mitigate / Recover / Learn>` | `<priority>` | `<name or team>` | `<YYYY-MM-DD>` | `<measurable evidence>` | `<Open / In progress / Done>` |

## References and Approval

- Incident record: `<link>`
- Related changes / ADRs / runbooks: `<links>`
- Reviewers / publication approval: `<names, teams, or status>`
- Next review date: `<date or N/A>`
