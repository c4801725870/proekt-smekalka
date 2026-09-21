# Knowledge Base: Expert Systems — Knowledge-Based Decisions

**Synthesized from:** Балтрашевич, Коробова, Нейлор, Барский

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Expert System | Software replacing domain expert | Diagnosis, forecasting |
| Knowledge Base | Domain rules + facts | Core ES component |
| Inference Engine | Rule application mechanism | Reasoning process |
| Production Rule | IF <condition> THEN <action> | Knowledge representation |
| Forward Chaining | Data → goals (data-driven) | Monitoring |
| Backward Chaining | Goals → data (goal-driven) | Diagnosis |
| Confidence Factor | MB - MD ∈ [-1,+1] | Uncertain reasoning |

## ES Architecture

```
Knowledge Base + Inference Engine + Knowledge Acquisition + Explanation System
```

## Knowledge Representation

| Method | Structure | Best For |
|--------|-----------|----------|
| Production Rules | IF→THEN | Simple domains |
| Semantic Networks | Graph (nodes + arcs) | Inheritance |
| Frames | Slots with values/defaults | Structured objects |
| Fuzzy Rules | IF x is A THEN y is B | Uncertainty |
| Neural Networks | Layers + weights | Pattern recognition |

## Inference Methods

| Method | Direction | Approach |
|--------|-----------|----------|
| Forward Chaining | Data → Goal | Facts → rules → new facts |
| Backward Chaining | Goal → Data | Hypothesis → verify conditions |

## ES vs Traditional Programs

| Traditional Program | Expert System |
|--------------------|---------------|
| Solves one task | Serves multiple goals |
| Program-driven control | Data-driven control |
| No explanations | Explains reasoning |
| Domain-bound | Instrumental |

## Neural Network Types

| Network | Type | Application |
|---------|------|-------------|
| Feedforward (MLP) | Layered | General classification |
| Hopfield | Recurrent | Optimization, pattern completion |
| Kohonen (SOM) | Self-organizing | Clustering, data mining |

## Decision Matrix

| Problem | Method | Why |
|---------|--------|-----|
| Simple domain | Production Rules | Natural, modular |
| Inheritance needed | Semantic Networks | IS-A, PART-OF |
| Uncertainty | Fuzzy Logic / Confidence Factors | Quantified reasoning |
| Pattern recognition | Neural Networks | Learning from data |
| Diagnosis | Backward Chaining | Goal-driven |
| Monitoring | Forward Chaining | Data-driven |

## Source Books
- Балтрашевич — ES implementation
- Коробова — decisions in KBS
- Нейлор — building expert systems
- Барский — neural networks
