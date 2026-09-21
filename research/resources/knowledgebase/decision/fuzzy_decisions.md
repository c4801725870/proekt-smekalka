# Knowledge Base: Decision — Fuzzy Decisions

**Synthesized from:** Коробова (Decision in KBS), with fuzzy logic sections

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Fuzzy set | Set with membership degrees [0,1] | Handle vagueness |
| Membership function | μ(x) ∈ [0,1] for each element | Quantify "how much" |
| Linguistic variable | Variable with words as values | Natural language modeling |
| Fuzzy rule | IF x is A THEN y is B | Knowledge representation |
| Defuzzification | Fuzzy output → crisp value | Action selection |
| Confidence Factor | MB - MD ∈ [-1,+1] | Quantified uncertainty |

## Fuzzy Logic Fundamentals

### Classical vs Fuzzy Sets
| Classical | Fuzzy |
|-----------|-------|
| x ∈ A or x ∉ A | μ(x) ∈ [0,1] |
| Sharp boundary | Gradual boundary |
| Binary membership | Degree of membership |

### Fuzzy Set Operations
| Operation | Formula |
|-----------|---------|
| Union (OR) | μ_A∪B(x) = max(μ_A(x), μ_B(x)) |
| Intersection (AND) | μ_A∩B(x) = min(μ_A(x), μ_B(x)) |
| Complement (NOT) | μ_Ā(x) = 1 - μ_A(x)) |

### Membership Functions
| Shape | Use |
|-------|-----|
| Triangular | Simple, computationally cheap |
| Trapezoidal | Plateau of certainty |
| Gaussian | Smooth, natural transitions |

## Fuzzy Inference

### Mamdani Method
1. Fuzzify inputs (crisp → fuzzy)
2. Apply fuzzy rules (IF-THEN)
3. Aggregate rule outputs
4. Defuzzify (fuzzy → crisp)

### Sugeno Method
1. Fuzzify inputs
2. Apply rules (output = linear function of inputs)
3. Weighted average of rule outputs

## Defuzzification Methods

| Method | Approach | When to Use |
|--------|----------|-------------|
| Center of Gravity (COG) | Centroid of fuzzy set | Most common |
| Mean of Maximum (MOM) | Average of peak values | When peak matters |
| Smallest of Maximum (SOM) | Conservative | Risk-averse |
| Largest of Maximum (LOM) | Aggressive | Risk-tolerant |

## Confidence Factors (KBS)

```
CF(H,E) = MB(H,E) - MD(H,E)    CF ∈ [-1, +1]

MB = Measure of Belief
MD = Measure of Disbelief

CF(H, E1∧E2) = min(CF1, CF2) × CF_rule
CF(H, E1∨E2) = max(CF1, CF2)
```

## Bayesian Decision

```
P(H|E) = P(E|H) × P(H) / P(E)
```

Naive Bayes: features conditionally independent given hypothesis.

## Dempster-Shafer Theory

- Belief function Bel(A) — total belief committed to A
- Plausibility Pl(A) — total belief not committed to ¬A
- Belief interval [Bel(A), Pl(A)]
- Dempster's rule: combine evidence from independent sources

## Uncertainty Methods Comparison

| Method | Representation | Combining | Best For |
|--------|---------------|-----------|----------|
| Fuzzy Logic | Membership degrees [0,1] | Min/Max operators | Vague concepts |
| Confidence Factors | CF ∈ [-1,+1] | Min/Max with rules | Expert systems |
| Bayesian | Probabilities | Bayes theorem | Statistical data |
| Dempster-Shafer | Belief intervals | Dempster's rule | Incomplete evidence |

## Fuzzy Control Systems

### Structure
```
Crisp Input → Fuzzification → Rule Base → Defuzzification → Crisp Output
```

### Rule Base Example (Temperature Control)
```
IF temperature is COLD THEN heating is HIGH
IF temperature is WARM THEN heating is LOW
IF temperature is HOT THEN heating is OFF
```

## Decision Matrix

| Problem | Method | Why |
|---------|--------|-----|
| Vague concepts | Fuzzy Logic | Membership degrees |
| Expert system uncertainty | Confidence Factors | Quantified reasoning |
| Statistical data available | Bayesian | Data-driven |
| Incomplete evidence | Dempster-Shafer | Belief intervals |
| Control systems | Fuzzy Control | Natural language rules |
| Pattern recognition | Neural Networks | Learning from data |

## Cross-References
- See also: Decision — AHP (structured multi-criteria decisions)
- See also: Expert Systems — Knowledge-Based Decisions (knowledge representation)
- See also: Expert Systems — Building Expert Systems (ES implementation)
- See also: TRIZ — Inventive Principles (contradiction resolution with fuzzy boundaries)

## Source Books
- Коробова И.Л., Артемов Г.В. — Принятие решений в системах, основанных на знаниях (2005)
