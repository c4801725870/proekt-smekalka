# Knowledge Base: Systems — Systems Methodology

**Synthesized from:** Клир (Systems Methodology), Месарович (Hierarchical Systems)

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| System | S = (A, R) — elements + relations | Model any problem as system |
| URSS | Universal System Problem Solver | Automated system problem solving |
| Epistemological hierarchy | 5 levels of system description | Choose right abstraction level |
| Generative system | Parametrically invariant constraint | Find patterns in data |
| Metasystem | Set of systems + replacement procedure | Higher-order generalization |
| Functional system | S: X → Y mapping | Abstract system definition |
| Coordination | Align local optimization with global goals | Multilevel systems |

## System Definition (Klir)

```
S = (A, R)
A = {a₁, a₂, ..., aₙ} — set of elements
R = {r₁, r₂, ..., rₘ} — set of relations
```

**System is NOT an object — it is a list of variables** representing abstracted properties.

### Variable Types

| Type | Description |
|------|-------------|
| Neutral | No input/output distinction |
| Directed | Input (controlled) + Output (observed) |
| Crisp | Exact values |
| Fuzzy | Possibility distributions |
| Discrete | Finite state sets |
| Continuous | Infinite state sets |

## Epistemological Hierarchy (5 Levels — Klir)

| Level | Name | What It Contains | When to Use |
|-------|------|-----------------|-------------|
| 0 | Source system | Variables, state sets, observation channels | Define problem |
| 1 | Data system | Source + actual observations | Collect data |
| 2 | Generative system | Behavior function (parametrically invariant) | Find patterns |
| 3 | Structure system | Subsystems with shared variables | Decompose problem |
| 4 | Metasystem | Set of systems + replacement procedure | Generalize across systems |

**Key**: Each higher level contains ALL knowledge of lower levels PLUS additional knowledge.

## Complexity Degrees (Bellman/Klir)

| Degree | Variables | Determinism | Method |
|--------|----------|-------------|--------|
| Organized simplicity | Few | High | Analytical (Newton) |
| Organized complexity | Many | Significant interactions | Computational |
| Disorganized complexity | Many | Statistical regularity | Probabilistic |

## System Definition (Mesarovich)

```
S: X → Y (functional system)
S ⊆ X × Y (relational system)
```

## Three Types of Hierarchies (Mesarovich)

### 1. Multilayer (Functional Decomposition)
| Layer | Function | Frequency |
|-------|----------|-----------|
| 1 | Direct control/execution | Continuous |
| 2 | Optimization/coordination | Periodic |
| 3 | Adaptation/learning | Occasional |
| 4 | Self-organization | Rare |

### 2. Multilevel (Decision Decomposition)
| Level | Scope | Impact | Frequency |
|-------|-------|--------|-----------|
| 1 | Detailed | Low | Frequent |
| 2 | Medium | Medium | Periodic |
| 3 | Strategic | High | Rare |

### 3. Nested Hierarchies
```
Component → Subsystem → System → Supersystem → System-of-systems
```

## Coordination Problem

**Problem**: Lower-level subsystems optimize local objectives, but global system needs coordinated behavior.

### 3 Coordination Principles

| Principle | Mechanism | When to Use |
|-----------|-----------|-------------|
| Interaction Balance | Higher predicts interactions, lower optimizes | Continuous processes |
| Interaction Decomposition | Higher decomposes, lower solves independently | Modular systems |
| Price/Cost Coordination | Higher sets prices for shared resources | Resource allocation |

### Coordination Algorithm
1. Coordinator selects coordination variables
2. Subsystems solve local problems with fixed variables
3. Solutions sent to coordinator
4. Coordinator adjusts variables based on balance
5. Repeat until convergence

## Finding Suitable Systems (Klir Algorithm)

1. Define source system on object (choose properties, bases)
2. Collect data → data system
3. For maximum acceptable mask M:
   - Generate all submasks in decreasing complexity order
   - For each mask: compute behavior function + generating uncertainty
4. Find Pareto-optimal solutions (complexity vs. determinism)
5. Select from nondominated set

## Key Measures

| Measure | Formula | What It Captures |
|---------|---------|-----------------|
| Shannon entropy | H = −Σ p·log(p) | Determinism |
| U-uncertainty | Possibilistic | Nondeterminism |
| Complexity | \|M\| | Size of mask (neighborhood scheme) |

## URSS Architecture (Klir)

```
Interpreted task → URSS → Solution mapped back
     ↓                ↑
Abstraction: domain → general system
Interpretation: general system → domain
```

## Practical Principles

1. **Two dimensions of science**: by element type (traditional) + by relation type (systems)
2. **Computer = laboratory** of systems science
3. **Modularity**: k²·n(n−1) memory vs. nᵏ for complete system
4. **Reducibilism AND holism are complementary** — neither is absolute
5. **Metasystem = generalization** across comparable systems
6. **Hierarchical decomposition** reduces complexity
7. **Coordination mechanisms** align local and global optimization
8. **Price coordination** mimics market mechanisms

## Decision Matrix

| Problem | Approach | Why |
|---------|----------|-----|
| Complexity | Decomposition | Manageable subsystems |
| Coordination | Hierarchical structure | Clear authority |
| Adaptation | Feedback mechanisms | Self-correcting |
| Optimization | Mathematical modeling | Formal analysis |
| Pattern finding | Generative system (Klir) | Parametrically invariant |
| Cross-domain generalization | Metasystem (Klir) | Higher-order abstraction |
| Local vs global optimization | Coordination principles (Mesarovich) | Balance objectives |

## Cross-References
- See also: Decision — Operations Research (optimization within systems)
- See also: Management — Project Management (organizational systems)
- See also: Expert Systems — Building Expert Systems (knowledge representation)
- See also: TRIZ — Inventive Principles (system evolution laws)

## Source Books
- Клир Дж. — Системология: Автоматизация решения системных задач (1990)
- Месарович, Мако, Такахара — Теория иерархических многоуровневых систем (1973)
