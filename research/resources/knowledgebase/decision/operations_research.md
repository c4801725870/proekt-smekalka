# Knowledge Base: Decision — Operations Research

**Synthesized from:** Таха, Конюховский, Шимко, Танаев

## Quick Reference

| Method | Problem | Key Result |
|--------|---------|------------|
| LP (Simplex) | Linear optimization | Optimal vertex |
| Duality | Resource valuation | Shadow prices |
| Transportation | Shipping problems | Min cost flow |
| Network | Shortest path, max flow | Dijkstra, Ford-Fulkerson |
| CPM/PERT | Project scheduling | Critical path |
| Integer LP | Discrete decisions | Branch and bound |
| DP | Multi-stage | Bellman equation |
| Queuing | Waiting lines | M/M/1, M/M/c |
| Simulation | Complex systems | Monte Carlo |

## OR Methodology

```
Problem → Verbal model → Math model → Solve → Validate → Implement
```

## Key Formulas

| Formula | Meaning |
|---------|---------|
| Q* = √(2DS/H) | Economic Order Quantity |
| L = λW | Little's Law |
| Critical path = max path | Minimum project duration |
| Dual variable = shadow price | Resource value |

## LP Key Concepts

- **Feasible region**: intersection of constraints
- **Corner point optimum**: LP optimal at vertex
- **Sensitivity analysis**: ranges for coefficients
- **Dual problem**: economic interpretation

## Network Models

| Model | Algorithm | Use |
|-------|----------|-----|
| Minimum spanning tree | Prim, Kruskal | Connect all nodes |
| Shortest path | Dijkstra | Route finding |
| Maximum flow | Ford-Fulkerson | Capacity analysis |
| CPM/PERT | Forward/backward pass | Project scheduling |

## Decomposition Methods

| Method | Approach | Best For |
|--------|----------|----------|
| Dantzig-Wolfe | Column generation | Large LP |
| Benders | Row generation | Mixed-integer |
| Lagrangian | Relax constraints | Combinatorial |

## Decision Matrix

| Problem | Method | Why |
|---------|--------|-----|
| Resource allocation | LP | Efficient |
| Project scheduling | CPM/PERT | Critical path |
| Inventory | EOQ | Optimal order |
| Waiting lines | Queuing theory | Performance measures |
| Complex system | Simulation | When analytical fails |
| Multi-stage | DP | Optimal substructure |

## Source Books
- Таха — comprehensive OR textbook
- Конюховский — OR in economics
- Шимко — economic system optimization
- Танаев — decomposition methods
