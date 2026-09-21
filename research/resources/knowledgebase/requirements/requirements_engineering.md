# Knowledge Base: Requirements — Requirements Engineering

**Synthesized from:** Suzanne Robertson (Volere), Gathering Business Requirements, RUP, Vvedenie v RUP

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Volere | Complete requirements discovery process | Requirements engineering |
| Brown Cow Model | Essence vs implementation separation | Find real problem |
| Business Event | Trigger for business response | Work partitioning |
| Fit Criterion | Measurable requirement property | Testability |
| Quality Gateway | Filter bad requirements | Quality control |
| Use case | Functional requirement from user perspective | RUP foundation |
| User story | Negotiable requirement on card | Agile approach |

## Requirements Methods Comparison

| Method | Approach | Best For |
|--------|----------|----------|
| Volere | Complete process with template | Large/complex projects |
| Sequential role playing | Walk through with actors | 90-95% capture rate |
| User stories (Agile) | Cards, conversation, confirmation | Iterative development |
| RUP use cases | Use-case driven | Architecture-centric |

## Volere Process

```
Blastoff → Trawl for Knowledge → Day in the Life →
Prototype → Functional Requirements → Non-functional →
Quality Gateway → Review → Reuse
```

## Brown Cow Model (4 Quadrants)

| Quadrant | What | Focus |
|----------|------|-------|
| Current-What (How-Now) | Current state with technology | Understand existing |
| Current-Essence (What-Now) | Current state without technology | Find real problem |
| Future-What (How-Future) | Future state with technology | Design solution |
| Future-Essence (What-Future) | Future state without technology | Define purpose |

**Key insight**: Separate essence (what the work DOES) from implementation (how it's done).

## Non-functional Requirement Types (Volere)

| # | Type | Examples |
|---|------|---------|
| 10 | Look and Feel | Appearance, style |
| 11 | Usability | Ease of use, accessibility |
| 12 | Performance | Speed, capacity, reliability |
| 13 | Operational | Environment, interfaces |
| 14 | Maintainability | Adaptability, support |
| 15 | Security | Access, integrity, privacy |
| 16 | Cultural | Localization |
| 17 | Legal | Compliance, standards |

## Fit Criterion

**"When you can measure what you are speaking about, and express it in numbers, you know something about it."** — Lord Kelvin

Every requirement must have a measurable fit criterion:
- Description: "The system shall be fast"
- Fit criterion: "Response time < 2 seconds for 95% of requests"

## Quality Gateway

Single entry point for all requirements. Each must pass:
1. Complete? (all attributes present)
2. Meaningful to stakeholders?
3. Fit criterion testable?
4. No conflicts?
5. Traceable to business event?

## Business Objectives (Gate)

1. Improve Customer Relationships
2. Reduce Costs
3. Improve Productivity
4. Eliminate Non-Value Added Work
5. Leverage Technology

**If project meets none: STOP — project isn't important.**

## RUP Requirements Process

```
1. Inception → Vision, use-case model
2. Elaboration → Detailed use cases, architecture baseline
3. Construction → Implement use cases
4. Transition → Validate with users
```

## Decision Matrix

| Problem | Solution | Avoid |
|---------|----------|-------|
| Wrong problem solved | Brown Cow Model | Jumping to solution |
| Ambiguous requirements | Fit Criterion | Unmeasurable specs |
| Bad requirements enter | Quality Gateway | No filtering |
| Low capture rate | Sequential role playing | Traditional use cases alone |
| No business value | Check objectives gate | Proceed anyway |

## Source Books
- Suzanne Robertson (Volere) — gold standard requirements process
- Gathering Business Requirements — practical method
- RUP — use-case driven development
- Vvedenie v RUP — Russian RUP overview
