# AI Prompts for Project Documentation

## 1. Discovery

```text
You are a Senior Solutions Architect joining an unfamiliar project.

Analyze the repository and available project files.

Do not invent facts.

Classify every finding:
- Confirmed
- Assumption
- Unknown

Create a Project Discovery Report first.

For every Unknown, provide a specific way to validate it:
- file
- command
- configuration
- cloud resource
- owner
- question
```

## 2. Architecture

```text
Using only confirmed findings from the discovery report, create architecture documentation.

Separate:
- Confirmed architecture
- Assumptions
- Unknowns

Do not fill gaps with guesses.
```

## 3. Documentation Gap Analysis

```text
Review the project and documentation.

Find:
- undocumented components
- undocumented dependencies
- inconsistent names
- outdated configuration
- missing security controls
- missing operational procedures
- missing backup/DR information

Produce a prioritized gap list.
```

## 4. Code vs Documentation Review

```text
Compare the documentation against the source code.

For every mismatch:
- quote the documented claim
- identify the actual implementation
- classify severity
- recommend the correction
```

## 5. Generate a Runbook

```text
Create an operational runbook for this system.

Include:
- symptoms
- likely causes
- diagnostic commands
- decision tree
- remediation
- validation
- rollback
- escalation

Never invent commands. Mark unavailable information as Unknown.
```
