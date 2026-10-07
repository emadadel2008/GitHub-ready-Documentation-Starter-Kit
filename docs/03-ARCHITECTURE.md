# 03 - Architecture

## Purpose

Explain how the major pieces work together.

## Architecture Example

```text
                    Internet
                       |
                       v
                +-------------+
                | Web Client  |
                +-------------+
                       |
                       v
                +-------------+
                | API Gateway |
                +-------------+
                       |
                       v
              +------------------+
              | Orders API       |
              | Node.js          |
              +------------------+
                 |            |
                 v            v
          +-----------+   +-----------+
          | PostgreSQL|   | Message   |
          | Database  |   | Queue     |
          +-----------+   +-----------+
                              |
                              v
                       +-------------+
                       | Worker      |
                       +-------------+
```

## Architecture Questions

- What are the components?
- What protocols are used?
- Where does data enter?
- Where is data stored?
- Which components are synchronous?
- Which components are asynchronous?
- What happens when a dependency fails?

## Architecture Decision Example

### Decision: Use asynchronous order processing

**Status:** ✅ Confirmed

**Reason:** Order processing can continue independently from notification processing.

**Benefit:**
- Better resilience
- Lower coupling
- Independent scaling

**Trade-off:**
- More operational complexity
- Eventual consistency

## Architecture Evidence

For every major component, record the source:

- Repository path
- Terraform/Bicep file
- Cloud resource
- Diagram
- Configuration
- Ticket
