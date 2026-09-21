# Knowledge Base: Patterns — Workflow Patterns

**Synthesized from:** Van der Aalst Workflow Patterns

## Quick Reference

| Category | Count | Purpose |
|----------|-------|---------|
| Control-flow patterns | 20+ | How tasks are ordered |
| Resource patterns | 5+ | Who performs tasks |
| Data patterns | 4+ | How data flows |
| Workflow enactment | 6 | System capabilities |

## Control-Flow Patterns

### Basic Patterns (1-5)

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 1 | Sequence | A → B → C | Order processing steps |
| 2 | Parallel Split | A → (B AND C) | Parallel approvals |
| 3 | Synchronization | (B AND C) → D | Wait for all parallel |
| 4 | Exclusive Choice | A → (B XOR C) | Decision branching |
| 5 | Simple Merge | (B XOR C) → D | Rejoin after XOR |

### Advanced Branching & Synchronization (6-9)

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 6 | Multi-Choice | A → (B AND/OR C AND/OR D) | Select applicable services |
| 7 | Structured Synchronizing Merge | Merge after multi-choice | Wait for selected branches |
| 8 | Multi-Merge | Multiple instances converge | Any completion triggers next |
| 9 | Structured Discriminator | First-then-ignore sync | First response wins |

### Iteration Patterns (10-15)

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 10 | Arbitrary Cycles | Loop back to any point | Review-revise cycle |
| 11 | Implicit Termination | Process ends naturally | No more work to do |
| 12 | Multiple Instances (no sync) | Parallel instances | Batch processing |
| 13 | MI with a Priori Design N | N instances, known at design | Fixed parallel tasks |
| 14 | MI with a Priori Runtime N | N instances, known at runtime | Dynamic batch size |
| 15 | MI without a Priori N | N instances, unknown | Streaming processing |

### State-Based Patterns (16-18)

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 16 | Deferred Choice | Environment decides | External event triggers path |
| 17 | Interleaved Parallel Routing | No simultaneous execution | Shared resource constraint |
| 18 | Milestone | Task enabled in specific state | Approval gate |

### Cancellation Patterns (19-20)

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 19 | Cancel Task | Terminate specific task | Timeout handling |
| 20 | Cancel Case | Terminate entire workflow | Abort process |

## Resource Patterns

| # | Pattern | Description | Example |
|---|---------|-------------|---------|
| 1 | Direct Distribution | Specific person assigned | Named expert |
| 2 | Role-Based Distribution | Assign to role | "Any manager" |
| 3 | Deferred Distribution | Assignment at runtime | Queue-based |
| 4 | Authorization | Capability-based | Skill matching |
| 5 | Separation of Duties | Different people for consecutive tasks | Compliance (4-eyes) |

## Data Patterns

| # | Pattern | Description |
|---|---------|-------------|
| 1 | Data Transfer via Value | Pass actual data between tasks |
| 2 | Data Transfer via Reference | Pass pointer/ID between tasks |
| 3 | Data Transformation | Convert data format between tasks |
| 4 | Data-based Routing | Route based on data values |

## Petri Net Formalism

- **Place** = state/condition
- **Transition** = task/event
- **Token** = control flow marker
- **Firing** = task execution

## Decision Matrix

| Problem | Pattern | Why |
|---------|---------|-----|
| Sequential tasks | Sequence | Simple ordering |
| Parallel work | Parallel Split + Synchronization | Concurrent execution |
| Conditional routing | Exclusive Choice | XOR decision |
| Complex branching | Multi-Choice | AND/OR decisions |
| Loop processing | Arbitrary Cycles | Iteration |
| Deferred decisions | Deferred Choice | Environment-driven |
| Resource constraints | Separation of Duties | Compliance |
| Data-driven routing | Data-based Routing | Conditional on data |
| Shared resource | Interleaved Parallel | No simultaneous access |
| Timeout/cancel | Cancel Task/Case | Process termination |

## Cross-References
- See also: GoF Design Patterns — behavioral patterns (Observer, Strategy, State)
- See also: Analysis Patterns — Plan pattern (resource management)
- See also: Management — Project Management (PM scheduling, critical path)
- See also: Systems — Systems Methodology (process decomposition)
- See also: Expert Systems — Building Expert Systems (inference as workflow)

## Source Books
- Van der Aalst, ter Hofstede, Kiepuszewski, Barros — Workflow Patterns (2002)
