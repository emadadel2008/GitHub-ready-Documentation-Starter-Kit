# 19 - Architecture Artifacts

## Purpose

Architecture artifacts communicate intent and design to different audiences, preserve decisions, and help teams build and operate a system consistently. Create only the artifacts that help stakeholders make decisions or do their work; keep each one linked to evidence and to the other relevant artifacts.

## Trace Requirements to Design

A useful documentation chain is:

```text
Business requirements (BRD)
              |
              v
Functional and non-functional requirements
              |
              v
High-level design (HLD)
              |
              v
Low-level design (LLD)
              |
              v
Implementation, tests, and operational procedures
```

Link each important design choice back to the requirement or constraint it addresses. Use stable IDs where traceability matters (for example, `REQ-012`); do not create IDs that imply formal approval if none exists.

| Artifact | Main question | Typical content |
|---|---|---|
| Business requirements (BRD) | Why is the change needed, and what outcome is required? | Goals, stakeholders, scope, business rules, success measures, constraints |
| HLD | What are the major building blocks and how do they work together? | Context, major components, integrations, deployment, key quality attributes |
| LLD | How will a specific component or capability be implemented? | Interfaces, schemas, detailed flows, validation, errors, configuration |
| ADR | Why was a significant architecture option chosen? | Context, options, decision, consequences, status |
| Decision log | What notable decisions were made and where is the detail? | Date, decision, owner, status, ADR or evidence link |
| Diagram | What relationship or flow should this audience understand? | A focused visual view with scope, legend, and evidence |

Start with the reusable files in [`../templates/README.md`](../templates/README.md).

## HLD and LLD Are Different Views

- **HLD** communicates system boundaries and major responsibilities. It should help business stakeholders, architects, security reviewers, and delivery teams understand the shape of the solution without implementation noise.
- **LLD** explains the details needed by engineers implementing or changing a component: interfaces, data structures, interactions, error behavior, and relevant constraints.

One diagram rarely serves every audience. Prefer a small set of clear, linked views over one crowded diagram; state what each view includes and excludes.

## Choosing a Diagram

| View | Use it to explain | Common audience |
|---|---|---|
| System context / HLD | System boundary, users, and external dependencies | Business, product, architecture |
| Component / LLD | Internal modules and their responsibilities | Engineering |
| Network | Boundaries, connectivity, exposure, and trust zones | Infrastructure, network, security |
| Data flow | Data sources, transformations, stores, and destinations | Engineering, data, privacy, security |
| Sequence | Time-ordered interactions for a scenario | Engineering, integration |
| Integration / communication | Systems, interfaces, protocols, and ownership | Architecture, integration teams |
| Security | Trust boundaries, identities, controls, and sensitive flows | Security, architecture, engineering |
| Disaster recovery | Recovery topology, dependencies, and failover steps | Operations, business continuity |

Use [`../templates/architecture-diagrams.md`](../templates/architecture-diagrams.md) for Mermaid starters. Treat examples as scaffolding only; replace them with verified project details.

## Decision Log vs. ADR

A **decision log** is an index: it makes decisions easy to find and gives a short summary. An **Architecture Decision Record (ADR)** captures the context and reasoning for one consequential decision, including alternatives and trade-offs. Use a log entry alone for a small, easily reversible choice; link to an ADR when future contributors need the deeper rationale.

Record decisions while the context is still available. If a decision changes, preserve the previous ADR and create a new record that supersedes it rather than erasing history.

## Artifact Repository

Store artifacts where their intended readers can discover, access, review, and maintain them. Options include version-controlled repositories (docs-as-code), SharePoint, Confluence, Notion, Azure DevOps Wiki, or a developer portal such as Backstage. Choose based on access control, collaboration, review workflow, version history, and integration with the team's delivery process; no single tool fits every organization.

Regardless of tool:

- Name one canonical source of truth and link supporting copies to it.
- Keep current diagrams and design documents close to the system and its change workflow where practical.
- Assign an owner and review cadence; see [Documentation Lifecycle](18-DOCUMENTATION-LIFECYCLE.md).
- Avoid including credentials, secrets, or sensitive production data in artifacts.

## Quality Check

- [ ] Audience and purpose are stated.
- [ ] Requirements, designs, decisions, and implementation are linked where applicable.
- [ ] Diagrams have a title, scope, legend when needed, and readable labels.
- [ ] Claims are supported or marked Assumption / Unknown with a validation path.
- [ ] Owner, canonical location, and review cadence are clear.
