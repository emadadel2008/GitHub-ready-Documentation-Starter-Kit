# Project Documentation Starter Kit

A practical, AI-friendly framework for documenting any software, cloud, infrastructure, or enterprise project — even when you are new to the project.

## Goal

The objective is not to write documentation from assumptions.

The workflow is:

**Discover → Verify → Document → Review → Maintain**

Every important statement should be classified as:

- ✅ **Confirmed** — verified from code, configuration, infrastructure, diagrams, or an authoritative source.
- ⚠️ **Assumption** — inferred but not yet verified.
- ❓ **Unknown** — information is missing and needs validation.

## Documentation Flow

```text
Project / Repository
        |
        v
01 - Discovery
        |
        v
02 - Architecture
        |
        v
03 - Components & Data Flow
        |
        v
04 - Deployment & Configuration
        |
        v
05 - Security & Operations
        |
        v
06 - Troubleshooting & DR
        |
        v
Review / Validate
        |
        v
Continuous Maintenance
```

## Recommended Documentation

```text
docs/
├── 01-PROJECT-DISCOVERY.md
├── 02-PROJECT-OVERVIEW.md
├── 03-ARCHITECTURE.md
├── 04-COMPONENTS.md
├── 05-DATA-FLOW.md
├── 06-NETWORK.md
├── 07-SECURITY.md
├── 08-API.md
├── 09-DEPLOYMENT.md
├── 10-CONFIGURATION.md
├── 11-OPERATIONS.md
├── 12-MONITORING.md
├── 13-BACKUP-RECOVERY.md
├── 14-DISASTER-RECOVERY.md
├── 15-TROUBLESHOOTING.md
├── 16-CHANGELOG.md
└── 17-DOCUMENTATION-REVIEW.md
```

## The Golden Rule

> Never convert an assumption into a fact.

If you cannot verify something, document it as **Unknown** or **Assumption** and explain how it can be validated.

## AI Prompt

Use this prompt when giving a new repository to an AI:

> You are a Senior Solutions Architect joining an unfamiliar project. Analyze the repository and available infrastructure/configuration documentation. Do not invent facts. Classify findings as Confirmed, Assumption, or Unknown. Create a Project Discovery Report first. For every unknown, provide a validation question, command, file, or owner that could confirm the answer. Do not write final architecture documentation until discovery is complete.
