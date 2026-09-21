# Knowledge Base: Quality — Reliability Engineering

**Synthesized from:** Reliability Engineering (Smith), ISO 9001 (Schlickman, Пич), Metrology (Ковалевская)

## Quick Reference

| Concept | Definition | Formula |
|---------|------------|---------|
| Failure rate (λ) | Failures per unit time | F/10⁶h or FITS |
| MTBF | Mean Time Between Failures | T/k |
| MTTF | Mean Time To Fail | For non-repaired items |
| Reliability | Probability of survival | R(t) = e^(-λt) |
| Availability | Uptime ratio | A = MTBF/(MTBF+MDT) |
| FMEA | Failure Mode, Effects, and Criticality Analysis | RPN = S × O × D |

## Core Formulas

### Reliability (constant failure rate)
```
R(t) = e^(-λt)
MTBF = 1/λ = ∫₀^∞ R(t)dt
```

### Availability
```
A = MTBF / (MTBF + MDT)
MDT = fault recognition + access + diagnosis + spare + replacement + checkout
```

### Series System
```
R_series = R₁ × R₂ × ... × Rₙ
λ_series = λ₁ + λ₂ + ... + λₙ
```

### Parallel (Redundant) System
```
R_parallel = 1 - (1-R₁)(1-R₂)...(1-Rₙ)
```

### k-out-of-n System
```
R_k/n = Σ C(n,i) Rⁱ(1-R)ⁿ⁻ⁱ  for i=k to n
```

## Bathtub Curve (3 Phases)

| Phase | Failure Rate | Cause | Action |
|-------|-------------|-------|--------|
| Early (burn-in) | Decreasing | Manufacturing defects | Screening, burn-in |
| Useful life | Constant (λ) | Random failures | MTBF = 1/λ |
| Wearout | Increasing | Degradation | Preventive replacement |

## Quality Costs (P-A-F)

| Type | Typical % of Turnover |
|------|----------------------|
| Prevention | ~1% |
| Appraisal | ~3% |
| Failure | ~4% |
| **Total** | **4-15%, avg ~8%** |

**Key insight**: Prevention investment yields highest ROI. Quality cannot be inspected into a product.

## Reliability Prediction Methods

| Method | When to Use | Accuracy |
|--------|-------------|----------|
| Parts count | Early design | ±50% |
| Parts stress | Detailed design | ±20% |
| Field data | Existing systems | Best |
| Test data | New components | Good |

## FMEA/FMECA

**Failure Mode, Effects, and Criticality Analysis**
- Identify failure modes
- Assess effects on system
- Calculate RPN = Severity × Occurrence × Detection
- Prioritize corrective actions

## Fault Tree Analysis (FTA)

- Top-down deductive method
- Top event → intermediate events → basic events
- Boolean logic (AND, OR gates)
- Calculate top event probability

## Software Reliability Models

| Type | Models |
|------|--------|
| Discrete | Jelinski-Moranda, Musa |
| Continuous | Millas, Lipov |
| Static | Simple intuitive, Corcoran, Nelson |
| Empirical | Shuman, Schick-Wolverton |

## Metrology & Correctness (Ковалевская)

### Correctness Levels

| Level | Type | What |
|-------|------|------|
| Text | Syntactic | Language syntax conformance |
| Text | Semantic | Language construct correctness |
| Module | Constructive | Structural programming rules |
| Module | Functional | Data processing correctness |
| System | Deterministic | Exact I/O correspondence |
| System | Stochastic | Statistical distribution match |
| System | Dynamic | Time-varying result conformance |

### Quality Criteria by Lifecycle

| Phase | Criteria |
|-------|----------|
| Design | Creation complexity, correctness, development effort |
| Operation | Functional complexity, reliability, resource efficiency |
| Maintenance | Modifiability, mobility, learning effort |

## ISO 9001 Reliability Integration

| ISO 9001 Clause | Reliability Application |
|-----------------|------------------------|
| 7.1 Planning | Reliability targets in product planning |
| 7.3 Design | FMEA, reliability prediction, testing |
| 7.5 Production | Process control, SPC |
| 8.2.4 Monitoring | Reliability testing, field data collection |
| 8.3 Nonconformance | Failure analysis, corrective action |
| 8.5 Improvement | Reliability growth, preventive action |

## Decision Matrix

| Problem | Method | Output |
|---------|--------|--------|
| System reliability prediction | Series/parallel models | R(t) |
| Identify failure modes | FMEA/FMECA | Risk Priority Number |
| Root cause of failure | Fault Tree Analysis | Cut sets |
| Optimize maintenance | Availability analysis | Preventive replacement interval |
| Life cycle cost | LCC analysis | Optimal design point |
| Syntax errors | Syntactic correctness check | Language conformance |
| Logic errors | Functional testing | I/O verification |
| Reliability | Statistical testing | Failure rate estimation |

## Cross-References
- See also: Quality — ISO 9001 (QMS framework)
- See also: Quality — Statistical Process Control (measurement methods)
- See also: Management — Project Management (risk management)
- See also: TRIZ — Inventive Principles (contradiction resolution in design)

## Source Books
- David J. Smith — Reliability, Maintainability and Risk (1997/1999)
- Schlickman — ISO 9001:2000 Quality Management System Design (2003)
- Пич — ISO 9001 Pocket Guide (2004)
- Ковалевская — Метрология, качество и сертификация ПО (2002)
