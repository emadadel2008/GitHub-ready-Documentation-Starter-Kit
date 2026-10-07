# 20 - Incident Learning and Postmortems

## Purpose

Troubleshooting and runbooks help responders diagnose and recover while an incident is active. A postmortem is a separate, blameless learning review after a significant incident. It records the impact and timeline, examines contributing system and process conditions, and tracks actions that reduce the likelihood or impact of recurrence.

Use the [postmortem template](../templates/postmortem.md) as a starting point. Not every event needs a formal postmortem; define the review threshold with the teams responsible for the service, and follow applicable security, privacy, and regulatory incident processes.

## Review Principles

- **Learn, do not blame.** Examine the system conditions, safeguards, information, and constraints that shaped outcomes. Do not treat an individual's action as the full explanation.
- **Separate fact from hypothesis.** Cite incident records, alerts, logs, deployment changes, and other evidence. Label unverified causes or impacts as Assumption or Unknown.
- **Make the timeline useful.** Use a consistent timezone, distinguish event time from report time, and record sources.
- **Quantify impact responsibly.** State affected users, systems, data, duration, and uncertainty where known. Do not publish sensitive customer or personal information.
- **Turn learning into owned work.** Actions need a single accountable owner, a due date, priority, and measurable completion evidence.
- **Share appropriately.** Make the review accessible to teams who can learn from it while respecting privacy, security, legal, and communication requirements.

## Suggested Process

1. **Stabilize and preserve evidence.** Follow the incident response process; retain relevant timelines and technical evidence under the organization's policies.
2. **Assign a facilitator.** A facilitator gathers evidence and helps participants review the event without assigning personal blame.
3. **Reconstruct the timeline and impact.** Separate what was observable at the time from what became clear later.
4. **Analyze contributing conditions.** Consider architecture, dependencies, capacity, deployment, monitoring, procedures, access, and communication as relevant; do not assume one root cause if the evidence supports several factors.
5. **Agree on follow-up.** Prioritize prevention, detection, mitigation, recovery, and learning actions. Track them in the team's work system and link them from the review.
6. **Publish and revisit.** Share the review with its intended audience, check action progress, and update affected architecture, runbooks, monitoring, or risk records.

## Postmortem Quality Check

- [ ] Incident scope, severity, impact window, and reviewers are recorded.
- [ ] Impact and timeline claims cite evidence or are marked Unknown.
- [ ] Root cause is not asserted beyond the available evidence.
- [ ] Analysis addresses contributing system and process conditions without blame.
- [ ] Actions are specific, prioritized, owned, dated, and verifiable.
- [ ] Sensitive information is minimized and the audience is appropriate.
- [ ] Related runbooks, designs, risk records, and monitoring are updated when needed.

## Related Resources

- [Troubleshooting](15-TROUBLESHOOTING.md) for diagnosis and recovery during an active issue.
- [Operations](11-OPERATIONS.md) and the [runbook template](../templates/operational-runbook.md) for repeatable procedures.
- [Risk register template](../templates/risk-register.md) for cross-cutting risks and tracked mitigations.
- [Documentation Lifecycle](18-DOCUMENTATION-LIFECYCLE.md) for ownership and ongoing maintenance.
