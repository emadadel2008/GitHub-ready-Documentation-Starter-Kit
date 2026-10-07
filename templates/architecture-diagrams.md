# Architecture Diagram Pack

> Copy only the views your readers need. These Mermaid fragments are illustrative scaffolding, not assertions about your system. Replace every placeholder with verified information and link the diagram to its HLD or LLD.

## Diagram Metadata

| Field | Value |
|---|---|
| Title / view | `<system context, network, data flow, etc.>` |
| Purpose | `<question this diagram answers>` |
| Audience | `<business, engineering, security, data, operations>` |
| Scope / exclusions | `<what is and is not shown>` |
| Owner / last reviewed | `<team / YYYY-MM-DD>` |
| Source / related design | `<link>` |

## System Context / HLD

```mermaid
flowchart LR
    user["<User / actor>"] --> system["<System>"]
    system --> external["<External system>"]
```

## Component / LLD

```mermaid
flowchart TB
    entry["<Entry point>"] --> api["<Component A>"]
    api --> data[("<Data store>")]
    api --> worker["<Component B>"]
```

## Network and Trust Boundaries

```mermaid
flowchart LR
    subgraph public["<Public zone>"]
        client["<Client>"]
    end
    subgraph private["<Private zone>"]
        service["<Service>"]
        store[("<Data store>")]
    end
    client -->|"HTTPS : <port>"| service
    service -->|"<protocol> : <port>"| store
```

## Data Flow

```mermaid
flowchart LR
    source["<Data source>"] -->|" <protocol / format> "| process["<Processing step>"]
    process -->|" <protocol / format> "| destination[("<Destination>")]
```

Add data classification, transformations, retention, or replication notes where relevant and verified.

## Sequence

```mermaid
sequenceDiagram
    actor User as <User>
    participant App as <Application>
    participant Dependency as <Dependency>
    User->>App: <Request>
    App->>Dependency: <Call>
    Dependency-->>App: <Response>
    App-->>User: <Result>
```

Add alternate, timeout, and failure paths that materially affect the scenario.

## Integration / Communication

```mermaid
flowchart LR
    producer["<Producer>"] -->|" <API / event / protocol> "| consumer["<Consumer>"]
    consumer -->|" <API / event / protocol> "| partner["<Partner system>"]
```

Document interface ownership, direction, protocol, and synchronous or asynchronous behavior.

## Security View

```mermaid
flowchart LR
    actor["<Identity / actor>"] -->|" <authentication> "| boundary["<Trust boundary>"]
    boundary -->|" <authorized flow> "| resource["<Protected resource>"]
```

Show verified identities, trust boundaries, and controls without exposing secrets or sensitive implementation details.

## Disaster Recovery

```mermaid
flowchart LR
    primary["<Primary environment>"] -->|" <replication / backup mechanism> "| recovery["<Recovery environment>"]
    trigger["<Recovery trigger>"] --> action["<Verified failover procedure>"]
    action --> recovery
```

Link recovery targets and tested procedures; do not imply replication or failover exists unless verified.
