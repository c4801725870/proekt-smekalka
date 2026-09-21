# Knowledge Base: Expert Systems — Building Expert Systems

**Synthesized from:** Нейлор, Балтрашевич, Коробова

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Expert system | Software replacing domain expert | Diagnosis, forecasting, monitoring |
| Knowledge base | Domain rules + facts | Core ES component |
| Inference engine | Rule application mechanism | Reasoning process |
| Production rule | IF <condition> THEN <action> | Knowledge representation |
| Forward chaining | Data → goals (data-driven) | Monitoring |
| Backward chaining | Goals → data (goal-driven) | Diagnosis |
| Confidence Factor | MB - MD ∈ [-1,+1] | Uncertain reasoning |

## ES Architecture (7 Blocks — Балтрашевич)

```
┌─────────────────────────────────────┐
│ 1. Knowledge Base (production rules)│
│ 2. Inference Engine (interpreter)   │
│ 3. Dispatcher (rule ordering)       │
│ 4. Explanation Block (reasoning log)│
│ 5. Message Block                    │
│ 6. Expert Interface (KB editing)    │
│ 7. User Interface (domain language) │
└─────────────────────────────────────┘
```

## ES Building Phases (Нейлор)

### Phase 1: Simple ES
- Variables + Outcomes + Rules (IF→THEN)
- Example: weather prediction (clouds, wind, barometer → rain/sun/snow)
- Parallel inference: all info gathered, then decision

### Phase 2: Training
- **Nearest Mean method**: compute average per class, classify by minimum distance
- **Rule correction formula**:
  ```
  If WRONG:  RULES(J,K) = RULES(J,K) - EXAMPLES(J,I)
  If RIGHT:  RULES(J,CORRECT) = RULES(J,CORRECT) + EXAMPLES(J,I)
  ```
- Iterative improvement through examples

### Phase 3: Sequential Inference
- Decision made after each new fact
- Next question depends on current state
- **RULEVALUE**: measure of variable informativeness
- Stops when BESTPOSS = BEST (decision reached)

## Production System (3 Components — Балтрашевич)

1. **Global Database** — facts, states, observations
2. **Production Rules** — IF <condition> THEN <action>
3. **Control System** — rule selection + termination condition

### Execution Cycle
```
while not terminal_condition:
    match rules against database
    select applicable rule
    apply rule → modify database
```

## Knowledge Types (Коробова)

| Type | Source | Characteristics |
|------|--------|----------------|
| Formalized | Books, laws, formulas | Complete, precise |
| Non-formalized | Experts, intuition | Incomplete, ambiguous, contradictory |

## Knowledge Representation Methods

| Method | Structure | Best For |
|--------|-----------|----------|
| Production Rules | IF→THEN | Simple domains, TRIZ principles |
| Semantic Networks | Graph (nodes + arcs) | Inheritance, hierarchies |
| Frames | Slots with values/defaults | Structured objects, templates |
| Fuzzy Rules | IF x is A THEN y is B | Uncertainty handling |
| Neural Networks | Layers + weights | Pattern recognition |

## Inference Methods

| Method | Direction | Approach | Best For |
|--------|-----------|----------|----------|
| Forward Chaining | Data → Goal | Facts → rules → new facts | Monitoring, interpretation |
| Backward Chaining | Goal → Data | Hypothesis → verify conditions | Diagnosis, proof |

### Search Modes (Балтрашевич)

| Mode | Behavior | Pros/Cons |
|------|----------|-----------|
| Irrevocable | Apply rule, no backtracking | Simple, may loop |
| Tentative + backtracking | Backtrack on failure | Memory-efficient, one path |
| Tentative + graph search | Remember multiple paths | Complete, memory-heavy |

### Search Optimization
- Use user answers to direct search
- "Telephone consultation" — askable questions first
- Dramatically reduces state space exploration

## Task Types Solved by ES

| Task | Input | Output |
|------|-------|--------|
| Interpretation | Observations | Situation description |
| Forecasting | Situations | Likely consequences |
| Diagnosis | Observations | System faults |
| Monitoring | Observations vs plan | Critical deviations |
| Training | Student behavior | Corrections |

## ES vs Traditional Programs

| Traditional Program | Expert System |
|--------------------|---------------|
| Solves one task | Serves multiple goals |
| Program-driven control | Data-driven control |
| No explanations | Explains reasoning |
| Domain-bound | Instrumental (domain-independent) |
| Programmer decides HOW | User states WHAT, ES decides HOW |

## ES Requirements (Балтрашевич)

1. Communication in domain language (not programming language)
2. Multiple task types
3. Instrumentality (domain-independent tool)
4. Explanation of reasoning
5. Role separation: programmer, expert, user

## Inference Modes (Нейлор)

| Mode | Behavior | Efficiency |
|------|----------|-----------|
| Parallel | Gather all info → decide | Simple, many questions |
| Sequential | Decide incrementally | Fewer questions, adaptive |

## Multi-Node Architecture (Нейлор)

- N nodes, each with own variables and outcomes
- Output of one node = input of another
- Hierarchical knowledge distribution
- For complex domains spanning multiple areas

## Implementation Languages

| Language | Approach | Strength |
|----------|----------|----------|
| Pascal | Imperative | Traditional, compiler-like |
| LISP | Functional | List processing, natural knowledge representation |
| Prolog | Logical | Built-in unification, declarative rules |
| BASIC | Simple | Quick prototyping (Нейлор) |

## Decision Matrix

| Situation | Approach | Avoid |
|-----------|----------|-------|
| Simple domain | Single-node, parallel inference | Over-engineering |
| Many questions | Sequential inference | Asking everything |
| Complex domain | Multi-node architecture | Single flat rule base |
| No expert available | Train from examples | Manual rule writing |
| Need explanations | Explanation block | Black-box decisions |
| Uncertainty | Fuzzy Logic / Confidence Factors | Ignoring uncertainty |
| Pattern recognition | Neural Networks | Rule-based approach |

## Cross-References
- See also: Expert Systems — Neural Networks (alternative AI approach)
- See also: Expert Systems — Knowledge-Based Decisions (decision-making in KBS)
- See also: Decision — Fuzzy Decisions (uncertainty handling)
- See also: TRIZ — Inventive Principles (knowledge representation for TRIZ)
- See also: Systems — Systems Methodology (system decomposition)

## Source Books
- Нейлор К. — Как построить свою экспертную систему (1991)
- Балтрашевич В.Э. — Реализация инструментальной экспертной системы (1993)
- Коробова И.Л., Артемов Г.В. — Принятие решений в системах, основанных на знаниях (2005)
