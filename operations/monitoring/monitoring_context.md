# Monitoring Context — Smekalka

**Purpose:** Track monitoring, alerting, and operational health.
**Last updated:** 2026-09-20

---

## Health Checks

| Check | Endpoint/Method | Expected | Frequency |
|-------|----------------|----------|-----------|
| Orchestrator health | TBD | TBD | TBD |
| Agent availability | TBD | TBD | TBD |
| Pipeline throughput | TBD | TBD | TBD |

---

## Key Metrics

| Metric | Description | Target | Alert Threshold |
|--------|-------------|--------|-----------------|
| Pipeline throughput | Completed pipelines per hour | TBD | TBD |
| TRIZ resolution time | Time to resolve contradictions | TBD | TBD |
| Quality Gateway pass rate | Solutions passing first attempt | TBD | TBD |
| Agent error rate | Failed agent responses / total | TBD | TBD |
| Idea Vault entries | Archived solutions per session | TBD | TBD |

---

## Alert Routing

| Severity | Channel | Response Time |
|----------|---------|---------------|
| Critical | TBD | Immediate |
| Warning | TBD | Within 1 hour |
| Info | TBD | Review daily |

---

## Incident Template

```markdown
### INC-[NNN]: [Incident Title]

- **Severity:** [Critical / Warning / Info]
- **Status:** [Active / Resolved]
- **Started:** [YYYY-MM-DD HH:MM]
- **Resolved:** [YYYY-MM-DD HH:MM]
- **Duration:** [N hours N minutes]

**Impact:**
[What was affected]

**Root Cause:**
[Why it happened]

**Timeline:**
- [HH:MM] [Event]
- [HH:MM] [Event]

**Resolution:**
[How it was fixed]

**Action Items:**
- [ ] [Preventive measure 1]
- [ ] [Preventive measure 2]
```

---

## Incident History

| ID | Date | Severity | Duration | Summary |
|----|------|----------|----------|---------|
| — | — | — | — | No incidents yet |
