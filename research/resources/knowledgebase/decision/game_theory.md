# Knowledge Base: Decision — Game Theory

**Synthesized from:** Суздаль, Блекуэлл, Таха, Конюховский

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Matrix game | Finite strategies, one payoff matrix | Two-player zero-sum |
| Nash equilibrium | No player can improve unilaterally | General non-zero-sum |
| Minimax | Max your minimum guaranteed payoff | Antagonistic games |
| Mixed strategy | Probability distribution over actions | No pure equilibrium |
| Characteristic function v(S) | Guaranteed payoff of coalition S | Cooperative games |

## Game Classification

```
By information:
  Deterministic → all factors known
  Stochastic → probabilities known
  Game-theoretic → only strategy sets known

By parties:
  Optimization (1 party) → classical OR
  Game (2+ parties) → conflict/cooperation
```

## Key Results

| Game Type | Solution Concept | Method |
|-----------|-----------------|--------|
| Zero-sum, finite | Saddle point / Mixed strategies | LP |
| Non-zero-sum | Nash equilibrium | Best response |
| Cooperative | Core / Shapley value | Characteristic function |
| Sequential | Subgame perfect equilibrium | Backward induction |

## Key Formulas

| Formula | Meaning |
|---------|---------|
| v̲ = max_i min_j a_ij | Lower game value (maximin) |
| v̄ = min_j max_i a_ij | Upper game value (minimax) |
| p'Aq = v | Expected payoff in mixed strategies |
| v(S) | Characteristic function of coalition S |

## Decision Matrix

| Situation | Method | Avoid |
|-----------|--------|-------|
| Zero-sum, finite | Matrix game (LP) | Guessing |
| No saddle point | Mixed strategies | Pure strategies only |
| Multiple players, cooperation | Cooperative game theory | Treating as bilateral |
| Multiple players, no cooperation | Nash equilibrium | Assuming cooperation |
| Sequential decisions | Dynamic programming | Single-stage analysis |

## Source Books
- Суздаль — military game theory applications
- Блекуэлл — game theory and statistical decisions
- Таха — OR methods including game theory
- Конюховский — OR in economics
