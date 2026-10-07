# Reusable Documentation Templates

These files are blank starting points, unlike the example/reference material in [`../docs/`](../docs/). Copy a template into the canonical documentation location for your project, rename it to fit your naming conventions, and remove sections that do not apply.

## Suggested Order

1. [Project documentation index](project-documentation-index.md) — identify the source of truth, audience, owners, and review cadence.
2. [Business requirements](business-requirements.md) — capture the business need, scope, constraints, and outcomes.
3. [High-level design](high-level-design.md) — describe the system boundary and major design.
4. [Architecture diagrams](architecture-diagrams.md) — select and create focused views that support the design.
5. [Low-level design](low-level-design.md) — detail the components that need implementation guidance.
6. [Architecture decision record](architecture-decision-record.md) and [decision log](decision-log.md) — preserve rationale and make decisions discoverable. Use the [lightweight ADR](architecture-decision-record-lightweight.md) for a small, low-risk decision when a full record is unnecessary.
7. [Risk register](risk-register.md) — track cross-cutting technical and delivery risks with owners and responses.
8. [Operational runbook](operational-runbook.md) — document verified procedures for operating and troubleshooting the system.
9. [Incident postmortem](postmortem.md) — capture impact, timeline, contributing conditions, and owned follow-up actions after an incident.

You do not need every artifact for every project. Follow [Architecture Artifacts](../docs/19-ARCHITECTURE-ARTIFACTS.md) to choose the right level of detail and [Documentation Lifecycle](../docs/18-DOCUMENTATION-LIFECYCLE.md) to keep the set current. Use a postmortem for learning after an incident; use a runbook for repeatable operational procedures.

## Before Publishing

- Replace every `<placeholder>` and remove unused instructions.
- Verify claims against code, configuration, infrastructure, tests, or an authoritative owner.
- Mark unverified statements as **Assumption** or **Unknown** and specify how to validate them.
- Link requirements, diagrams, implementation, and decisions where relevant.
- Assign an owner, canonical location, and review date or cadence.
- Never include credentials, secrets, or sensitive production data.

Suggested status labels: **Confirmed**, **Assumption**, and **Unknown**. The examples in this repository illustrate formats only; they are not facts about your system.
