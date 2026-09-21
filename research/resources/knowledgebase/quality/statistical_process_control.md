# Knowledge Base: Quality — Statistical Process Control

**Synthesized from:** SPC (Oakland), Kutz Vol.3 (quality chapter)

## Quick Reference

| Concept | Definition | Application |
|---------|------------|-------------|
| Quality | Meeting customer requirements | Fitness for purpose |
| SPC | Statistical Process Control | Monitor process variation |
| Control chart | Time-ordered plot with limits | Detect special causes |
| Capability | Process meets specifications | Cp, Cpk indices |
| 7 tools | Basic quality tools | Problem solving |
| DMAIC | Define-Measure-Analyze-Improve-Control | Six Sigma improvement |

## 4 SPC Questions

1. Can we do the job correctly? → **Capability**
2. Are we doing the job correctly? → **Control**
3. Have we done the job correctly? → **Quality assurance**
4. Could we do the job better? → **Improvement**

## 7 Basic Quality Tools

| Tool | Purpose | When to Use |
|------|---------|-------------|
| Flowchart | Map process steps | Understand process |
| Check sheet | Collect data systematically | Data collection |
| Histogram | Show variation distribution | Analyze spread |
| Run chart | Time series plot | Trend detection |
| Pareto | 80/20 analysis | Prioritize problems |
| Cause-effect | Fishbone diagram | Root cause analysis |
| Scatter diagram | Correlation analysis | Find relationships |

## Control Charts

### Variables Charts (continuous data)
| Chart | Use | Formula |
|-------|-----|---------|
| X̄-R | Subgroup size 2-10 | Mean and range |
| X̄-S | Subgroup size >10 | Mean and standard deviation |
| X-MR | Individual values | Moving range |

### Attributes Charts (count data)
| Chart | Use | Formula |
|-------|-----|---------|
| p | Proportion defective | p = defectives/n |
| np | Number defective | np = defectives |
| c | Defects per unit | c = defects |
| u | Defects per unit (variable size) | u = defects/n |

### Control Limits
```
UCL = X̄ + A₂R̄
CL = X̄
LCL = X̄ - A₂R̄
```

### Rules for Special Causes
- Point outside control limits
- 7 points on one side of center line
- 7 points trending up or down
- Other non-random patterns

## Capability Indices

| Index | Formula | Interpretation |
|-------|---------|----------------|
| Cp | (USL-LSL) / 6σ | Process spread vs spec spread |
| Cpk | min[(USL-X̄)/3σ, (X̄-LSL)/3σ] | Process centered capability |

| Cpk Value | Interpretation |
|-----------|----------------|
| < 1.0 | Incapable |
| 1.0 - 1.33 | Marginally capable |
| 1.33 - 1.67 | Capable |
| > 1.67 | Highly capable |

## DMAIC Improvement Cycle

```
Define → Measure → Analyze → Improve → Control
```

| Phase | Key Activities |
|-------|----------------|
| Define | Problem statement, scope, goals |
| Measure | Data collection, baseline performance |
| Analyze | Root cause analysis, statistical analysis |
| Improve | Implement solutions, pilot testing |
| Control | Standardize, monitor, sustain |

## Quality Costs (P-A-F)

| Type | When | Examples |
|------|------|----------|
| Prevention | Before production | Training, planning, QA system |
| Appraisal | During checking | Inspection, audits, calibration |
| Internal failure | Before delivery | Scrap, rework, reinspection |
| External failure | After delivery | Warranty, complaints, litigation |

**Key**: Prevention investment yields highest ROI. Quality cannot be inspected into a product.

## Design of Experiments (DOE) (Kutz Vol.3)

| Method | Purpose |
|--------|---------|
| Full factorial | Test all combinations |
| Fractional factorial | Reduce runs while maintaining info |
| Taguchi | Robust design, minimize variation |
| Response surface | Optimize process parameters |

## Six Sigma (Kutz Vol.3)

- **Goal**: 3.4 defects per million opportunities
- **Method**: DMAIC (Define-Measure-Analyze-Improve-Control)
- **Belt system**: Green Belt → Black Belt → Master Black Belt
- **Focus**: Process variation reduction

## Decision Matrix

| Problem | Tool | When |
|---------|------|------|
| Process understanding | Flowchart | Start of any project |
| Data collection | Check sheet | Need systematic data |
| Variation analysis | Histogram + control chart | Process monitoring |
| Prioritization | Pareto | Multiple problems |
| Root cause | Cause-effect (fishbone) | Finding causes |
| Correlation | Scatter diagram | Two variables |
| Capability | Cp, Cpk | Process meets specs |
| Process optimization | DOE (Taguchi) | Parameter tuning |

## Cross-References
- See also: Quality — ISO 9001 (QMS framework, Clause 8 measurement)
- See also: Quality — Reliability Engineering (failure rate measurement)
- See also: Management — Lean Manufacturing (Kaizen integration)
- See also: Decision — Operations Research (optimization methods)

## Source Books
- John S. Oakland — Statistical Process Control (5th Ed, 2003)
- Kutz Vol.3 — Mechanical Engineers' Handbook: Manufacturing and Management (quality chapter)
