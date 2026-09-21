# Knowledge Base: Patterns — Analysis Patterns

**Synthesized from:** Fowler Analysis Patterns, Fowler Refactoring

## Quick Reference

| Pattern | What It Models | When to Use |
|---------|---------------|-------------|
| Party | Person + Organization supertype | Any system with actors |
| Accountability | Relationships between parties | Employment, contracts, consent |
| Post | Position ≠ Person | Org charts, HR systems |
| Quantity | Number + Unit | Any measurement domain |
| Measurement | Observation of phenomenon | Scientific/financial tracking |
| Account | Balance + Entries | Financial, inventory, any ledger |
| Transaction | Balanced entry set | Double-entry bookkeeping |
| Plan | Actions + Resources | Project/resource management |
| Contract | Trading agreement | Financial/trading systems |
| Portfolio | Position collection | Investment management |

## Core Modeling Principles

1. Models are useful artifacts, not reality — "more or less useful," not right/wrong
2. Conceptual models relate to interfaces, not implementations
3. Separate what the problem IS (analysis) from how to solve it (design)
4. Choose model granularity appropriate to the job

## Party & Accountability

```
Party (supertype)
├── Person
└── Organization
    └── (recursive hierarchy — more flexible than fixed levels)

Accountability = Party → Party (employment, contract, consent)
  └── OperatingScope = responsibilities within accountability

Post = position with responsibilities (NOT attached to person)
  → Person fills Post; Post has Accountabilities
```

**Knowledge Level**: Meta-rules governing what accountabilities can exist between which party types.

## Observations & Measurements

```
Quantity = Number + Unit
  └── ConversionRatio: feet → meters

Measurement = Observation of a phenomenon
  ├── when observed vs when recorded (DualTimeRecord)
  └── Protocol = rules for how measurement taken

CompoundUnits: feet², meters/second (via multiplication of units)
```

**Anti-pattern**: Bare numbers without units. Always use Quantity.

## Inventory & Accounting

```
Account
  ├── balance (derived from entries)
  ├── entries (debit/credit)
  └── types: Summary, Memo, Posting

Transaction = set of entries that MUST balance (Σdebits = Σcredits)

Posting Rules = automated entry generation
  └── Individual Instance Method: behavior can vary per instance
```

### Standard Views
- **Balance Sheet**: Assets = Liabilities + Equity (snapshot)
- **Income Statement**: Revenue - Expenses = Profit (period)

## Trading & Finance

```
Contract = agreement to trade
Portfolio = collection of Positions
Quote = price at moment in time
Scenario = what-if analysis

Forward = future delivery obligation
Option = right but not obligation (call/put)
SubtypeStateMachine = behavior varies by contract subtype
```

**Parallel Hierarchies**: Separate technical infrastructure from domain model layers.

## Support Patterns

### Layered Architecture
| Tier | Responsibility |
|------|---------------|
| Presentation | UI, user interaction |
| Application Logic | Business rules, orchestration |
| Database | Persistence, queries |

### Application Facade
Simplified interface to complex subsystem. Common operations, type conversions.

### Association Patterns
- **AssociativeType**: many-to-many with attributes (e.g., Employment with start_date)
- **KeyedMapping**: lookup table by key
- **HistoricMapping**: track association changes over time

## Refactoring Patterns (Fowler)

### Code Smells → Refactorings

| Code Smell | Indicator | Refactoring |
|-----------|-----------|-------------|
| Long Method | >10 lines doing multiple things | Extract Method |
| Large Class | Too many responsibilities | Extract Class |
| Long Parameter List | >3-4 parameters | Introduce Parameter Object |
| Primitive Obsession | Primitives instead of objects | Replace Data Value with Object |
| Switch on type | Type-checking conditionals | Replace with Polymorphism |
| Divergent Change | One class, many reasons to change | Extract Class |
| Shotgun Surgery | One change, many classes | Move Method/Field |
| Feature Envy | Method uses other class's data | Move Method |
| Duplicate Code | Same code in multiple places | Extract Method |
| Dead Code | Unused code | Remove it |
| Comments | Explain bad code | Refactor until unnecessary |

### Refactoring Process Rules

1. **Solid tests FIRST** — never refactor without tests
2. **Small changes** — each step compiles and passes tests
3. **Run tests after EVERY change**
4. **Commit frequently** — rollback capability
5. **Separate refactoring from features** — never mix

### When to Refactor

| Trigger | Action |
|---------|--------|
| Adding feature | Refactor first → then add |
| Fixing bug | Refactor to clarify → then fix |
| Code review | Refactor to improve understanding |
| Rule of Third | 3rd time doing similar → refactor |

## Decision Matrix

| Situation | Use This Pattern | Avoid This |
|-----------|-----------------|------------|
| Actor/Entity in system | Party (Person/Organization) | Separate Person/Org tables |
| Org hierarchy | Recursive Organization | Fixed-level hierarchy |
| Any measurement | Quantity (number+unit) | Bare numeric fields |
| Financial tracking | Account + Transaction | Single balance field |
| Position vs person | Post pattern | Direct person-responsibility link |
| Complex subsystem | Application Facade | Direct coupling |
| History tracking | Historic Mapping | Overwriting records |
| Long method | Extract Method | Ignoring complexity |
| Large class | Extract Class | God objects |
| Type switch | Polymorphism | switch/if-else chains |

## Cross-References
- See also: GoF Design Patterns — Strategy (for varying behavior by type)
- See also: Enterprise Patterns — Repository, Unit of Work (implementation layer)
- See also: Systems — Hierarchy Theory (organizational structure maps to Accountability/Post)

## Source Books
- Martin Fowler — Analysis Patterns: Reusable Object Models (1997)
- Martin Fowler — Refactoring: Improving the Design of Existing Code (1999)
