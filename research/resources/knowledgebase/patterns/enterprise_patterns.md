# Knowledge Base: Patterns — Enterprise Patterns

**Synthesized from:** Fowler PoEAA, .NET Application Architecture, Enterprise Solution Patterns .NET

## Quick Reference

| Pattern | Category | Problem | Solution |
|---------|----------|---------|----------|
| Domain Model | Domain Logic | Complex business rules | Rich object model |
| Data Mapper | ORM | Object-relational impedance | Mapping layer |
| Unit of Work | ORM | Track dirty objects | Batch update tracking |
| Identity Map | ORM | Duplicate loads | Per-transaction cache |
| Remote Facade | Distribution | Chatty remote interface | Coarse-grained API |
| Data Transfer Object | Distribution | Multiple remote calls | Serializable data carrier |
| MVC | Presentation | Presentation coupling | Model+View+Controller |
| Layered Architecture | Architecture | Concern separation | Presentation→Domain→Data |

## Fowler's PoEAA Patterns

### Domain Logic

| Pattern | When to Use | Key Idea |
|---------|-------------|----------|
| Transaction Script | Simple logic, few rules | One procedure per request |
| Domain Model | Complex logic, many objects | Object model of domain |
| Table Module | Moderate logic, record-set | One class per table |
| Service Layer | Thin facade over domain | Application operations |

### Object-Relational Mapping (14 patterns)

| Pattern | Intent |
|---------|--------|
| Table Data Gateway | One gateway per table |
| Row Data Gateway | One gateway per row |
| Data Mapper | Layer of mappers (objects ↔ DB) |
| Active Record | Object wraps row + domain logic |
| Unit of Work | Track affected objects |
| Identity Map | Each object loaded once per transaction |
| Lazy Load | Load on demand |
| Identity Field | Object ID in DB field |
| Foreign Key Mapping | Reference → FK |
| Association Table Mapping | Many-to-many → join table |
| Dependent Mapping | Owned objects saved with owner |
| Embedded Value | Value object in owner's table |
| Serialized LOB | Object graph → single field |
| Single/Class/Concrete Table Inheritance | Inheritance mapping strategies |

### Web Presentation

| Pattern | Intent |
|---------|--------|
| MVC | Separate presentation from domain |
| Page Controller | One controller per page |
| Front Controller | Single handler for all requests |
| Template View | Render with embedded markers |
| Transform View | Transform domain to response |
| Application Controller | Centralized flow logic |

### Distribution

| Pattern | Intent |
|---------|--------|
| Remote Facade | Coarse-grained remote interface |
| Data Transfer Object | Serializable data carrier |

### Session State

| Pattern | Where |
|---------|-------|
| Client Session State | Cookies, hidden fields |
| Database Session State | Database table |
| Server Session State | Server session |

### Concurrency

| Pattern | Intent |
|---------|--------|
| Optimistic Offline Lock | Detect conflicts at commit |
| Pessimistic Offline Lock | Prevent conflicts by locking |

### Base Patterns

| Pattern | Intent |
|---------|--------|
| Gateway | Wrap external resource |
| Registry | Well-known lookup object |
| Layer Supertype | Base type per layer |
| Special Case | Polymorphism for null/special |
| Money | Currency-safe value object |
| Plugin | Replace via configuration |

## .NET Architecture Patterns

### 3-Layer Architecture

```
┌─────────────────────────────┐
│ Presentation Layer          │
│  ├── UI components          │
│  └── User process components│
├─────────────────────────────┤
│ Business Layer              │
│  ├── Business components    │
│  ├── Workflows              │
│  ├── Service interfaces     │
│  └── Business entities      │
├─────────────────────────────┤
│ Data Layer                  │
│  ├── Data stores            │
│  ├── Data access logic      │
│  └── Service integration    │
└─────────────────────────────┘
```

### Web Presentation (.NET)

| Pattern | Use | Implementation |
|---------|-----|----------------|
| MVC | Separate presentation | Code-behind, user controls |
| Page Controller | Per-page handling | Code-behind pages |
| Front Controller | Centralized handling | HTTPHandler |
| Intercepting Filter | Pre/post-processing | HTTP modules |

### Distributed Patterns (.NET)

| Pattern | Problem | Solution |
|---------|---------|----------|
| Broker | Client-server coupling | Intermediary |
| Proxy | Remote object access | Local surrogate |
| Message Broker | System integration | Central routing |

## Security Architecture

| Concern | Options |
|---------|---------|
| Authentication | Windows, forms, certificate |
| Authorization | Role-based, URL-based |
| Communication | Encryption, SSL/TLS |
| Auditing | Who did what when |

## Operational Requirements

| Requirement | Metric |
|-------------|--------|
| Scalability | Horizontal (more servers) vs Vertical (bigger) |
| Availability | 99.9% = 8.76 hours/year downtime |
| Maintainability | Ease of updates |
| Security | Threat protection |
| Performance | Response time, throughput |

## Layering Principle

```
Presentation → Domain Logic → Data Source
```

- Each layer only calls layers below
- Domain layer has NO infrastructure dependencies
- Data source layer handles persistence

## Decision Matrix

| Problem | Pattern | Why |
|---------|---------|-----|
| Simple business logic | Transaction Script | Simple, procedural |
| Complex business rules | Domain Model | Rich object model |
| Object ↔ relational mapping | Data Mapper | Clean separation |
| Object owns persistence | Active Record | Simple, direct |
| Track dirty objects | Unit of Work | Batch updates |
| Avoid duplicate loads | Identity Map | Cache per transaction |
| Chatty remote interface | Remote Facade + DTO | Coarse-grained |
| Presentation coupling | MVC | Code-behind |
| Request centralization | Front Controller | HTTPHandler |
| Tier separation | Layered Architecture | Physical deployment |
| Conflict detection | Optimistic Lock | Version checking |

## Cross-References
- See also: GoF Design Patterns — patterns used within PoEAA (Strategy, Observer, etc.)
- See also: Analysis Patterns — domain model patterns (Party, Account, etc.)
- See also: Requirements — Requirements Engineering (Volere NFRs for operational requirements)
- See also: Quality — ISO 9001 (process approach maps to layered architecture)
- See also: Systems — Hierarchy Theory (layering as hierarchy)

## Source Books
- Martin Fowler — Patterns of Enterprise Application Architecture (2002)
- Microsoft — Application Architecture for .NET (2002)
- Microsoft — Enterprise Solution Patterns Using .NET (2003)
