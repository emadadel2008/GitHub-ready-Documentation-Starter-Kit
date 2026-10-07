# 18 - Documentation Lifecycle

## Purpose

Documentation is part of delivering and operating a system, not a one-time handoff after deployment. A maintained, discoverable source of truth helps the team continue work, troubleshoot incidents, and understand the history of a system when its original contributors are unavailable.

## Working Principles

- **Update with the change.** Code, infrastructure, configuration, operational, and architecture changes should update the relevant docs and diagrams in the same pull request or change record.
- **Record the reason as well as the result.** Capture what changed, when, who changed it, and why. Link implementation changes to their related decisions or issues when possible.
- **Keep history.** Use version control or an equivalent change-history mechanism. Preserve superseded decisions and important prior states instead of silently overwriting the rationale.
- **Make ownership explicit.** Every maintained artifact needs a named owner or owning team, even when contributions are shared.
- **Review on a useful cadence.** Align recurring reviews with the team's iteration (for example, weekly, every two weeks, or at each release). Also review after a significant incident, architecture change, or ownership transition.
- **Be honest about evidence.** Mark unverified claims as Assumption or Unknown and provide a validation path; see [Project Discovery](01-PROJECT-DISCOVERY.md).

## Choose and Publish a Source of Truth

Choose a canonical, accessible location that fits the team's access, review, and versioning needs. It may be a repository (docs-as-code), an engineering wiki, or an approved knowledge base. If information must live in multiple systems, designate one canonical copy and link to it from the others.

For repository-hosted documentation, a practical layout is:

```text
repository/
├── README.md
├── docs/
│   ├── architecture/
│   ├── operations/
│   └── decisions/
└── diagrams/
```

This is a suggested layout, not a required structure. Keep the entry point obvious and avoid duplicate copies that can drift.

## Ownership and Review Register

Use this table in a project index or knowledge base to make maintenance actionable:

| Artifact | Audience | Owner | Canonical location | Review cadence / next review | Status |
|---|---|---|---|---|---|
| `<artifact name>` | `<who uses it>` | `<person or team>` | `<link or path>` | `<cadence or date>` | `<Current / Needs review / Unknown>` |

If ownership, cadence, or currency is not yet known, record it as Unknown and assign a validation action instead of implying it is covered.

## Update Workflow

1. **Identify affected artifacts** when a requirement, design, component, interface, dependency, deployment, security control, or operational procedure changes.
2. **Edit the canonical copy** alongside the relevant implementation or process change. Use the starter files in [`../templates/`](../templates/README.md) when a new artifact is needed.
3. **Verify claims and examples** against code, configuration, infrastructure, tests, or an authoritative owner. Label remaining gaps.
4. **Review for the audience** and keep diagrams at the right level of detail.
5. **Record history and ownership** in version control, decision records, or the project index.
6. **Schedule follow-up** for unresolved unknowns and routine reviews.

## Optional Automation

Automation can help enforce the process, but it does not replace clear ownership or review:

- Use an ADR helper such as [adr-tools](https://github.com/npryce/adr-tools) if numbering, linking, and superseding records manually is error-prone for your team.
- Consider a CI check that flags changes to architecture-sensitive paths when no related ADR or documentation update is linked. Start with a visible warning and a clearly scoped path list; only make it blocking when the rule is reliable and exceptions are documented.
- Render and validate diagrams in CI when the repository has diagrams-as-code and a suitable renderer. Keep the source and generated-artifact policy explicit.

Choose automation proportionate to the team's tools and change volume. A lightweight manual checklist is preferable to a brittle gate.

## Change Record

For a significant documentation or architecture update, capture:

| Field | Record |
|---|---|
| What changed? | `<summary>` |
| Why? | `<requirement, incident, decision, or change reference>` |
| When? | `<date>` |
| Who updated / approved it? | `<name or team>` |
| Affected artifacts | `<paths or links>` |
| Validation / remaining unknowns | `<evidence and follow-up>` |

Use [`16-CHANGELOG.md`](16-CHANGELOG.md) for a human-readable summary when appropriate; use an [ADR](../templates/architecture-decision-record.md) for decisions that need their own context and rationale.

## Lifecycle Review Checklist

- [ ] Is this still the canonical, findable copy?
- [ ] Do the owner and intended audience remain correct?
- [ ] Do implementation, diagrams, deployment, and operational steps still match reality?
- [ ] Are assumptions and unknowns resolved, revalidated, or assigned?
- [ ] Are links, examples, and commands still valid?
- [ ] Is the next review date or cadence clear?
