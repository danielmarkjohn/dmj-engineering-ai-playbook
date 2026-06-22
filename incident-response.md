# incident-response.md

# Production Incident Response Playbook

This document defines the process for responding to production incidents.

The objective is to restore service quickly, minimize customer impact, identify the true root cause, and implement permanent preventive actions.

The goal is not simply to resolve incidents, but to learn from them.

---

# Incident Priorities

| Severity  | Description                                       | Target Response   |
| --------- | ------------------------------------------------- | ----------------- |
| **Sev 1** | Complete outage, major customer impact, data loss | Immediate         |
| **Sev 2** | Major feature unavailable or severe degradation   | Within 30 minutes |
| **Sev 3** | Partial degradation or workaround available       | Same business day |
| **Sev 4** | Minor defect with limited business impact         | Planned backlog   |

---

# Incident Lifecycle

```text
Alert Triggered
        ↓
Acknowledge
        ↓
Assess Severity
        ↓
Stabilize Service
        ↓
Identify Root Cause
        ↓
Implement Fix
        ↓
Validate Recovery
        ↓
Post-Incident Review
        ↓
Prevent Recurrence
```

---

# Phase 1. Detection

Determine:

* What triggered the alert?
* Is the issue customer-facing?
* Is the incident ongoing?
* What systems are affected?
* When did it begin?

Never assume the first alert represents the actual problem.

---

# Phase 2. Assessment

Determine:

## Customer Impact

* Who is affected?
* How many users?
* What functionality is unavailable?
* Is data integrity at risk?

---

## Business Impact

* Revenue impact
* SLA/SLO violations
* Compliance implications
* Operational disruption

---

## Technical Impact

* APIs affected
* Services affected
* Databases affected
* Third-party dependencies
* Infrastructure impact

---

# Phase 3. Stabilization

The first objective is restoring service.

Possible actions include:

* Roll back deployment
* Disable feature flag
* Restart unhealthy services
* Scale infrastructure
* Fail over to healthy regions
* Enable degraded mode
* Disable non-critical functionality

Prefer the safest recovery path over the fastest code change.

---

# Phase 4. Root Cause Analysis

Identify:

## Root Cause

What actually caused the failure?

Avoid stopping at symptoms.

---

## Trigger

What event exposed the problem?

Examples:

* Deployment
* Traffic spike
* Configuration change
* Infrastructure failure
* Third-party outage

---

## Blast Radius

Determine:

* Services affected
* Customers affected
* Internal teams affected
* Data affected

---

# Phase 5. Recovery Validation

Confirm:

* Service restored
* Error rates normalized
* Latency acceptable
* Customer functionality verified
* Monitoring healthy
* No secondary failures introduced

Recovery is complete only after validation.

---

# Phase 6. Post-Incident Review

Every incident should document:

## Timeline

* Detection
* Response
* Recovery
* Resolution

---

## Root Cause

Describe the underlying issue.

---

## Contributing Factors

Examples:

* Missing monitoring
* Technical debt
* Process gaps
* Human error
* Documentation gaps

---

## Customer Impact

* Duration
* Severity
* Scope
* Business consequences

---

## Resolution

Document:

* Immediate fix
* Permanent fix
* Follow-up work

---

# Prevention Plan

Every incident should result in improvements.

Examples:

* Better monitoring
* New alerts
* Additional tests
* Improved documentation
* Automation
* Architecture improvements
* Team training

Never close an incident without identifying preventive actions.

---

# Communication Principles

During incidents:

* Share facts, not assumptions.
* Communicate regularly.
* Clearly identify knowns and unknowns.
* Avoid speculation.
* Document decisions as they are made.

Transparency builds trust.

---

# Common Root Cause Categories

* Application bug
* Infrastructure failure
* Database issue
* Third-party dependency
* Deployment failure
* Configuration error
* Capacity limitation
* Security event
* Human error

Categorizing incidents helps identify long-term trends.

---

# Success Metrics

Track incident performance over time.

Examples:

* Mean Time to Detect (MTTD)
* Mean Time to Acknowledge (MTTA)
* Mean Time to Recover (MTTR)
* Change Failure Rate
* Repeat Incident Rate
* Customer Impact Duration
* Number of Sev 1 and Sev 2 incidents

Engineering teams improve what they measure.

---

# Lessons Learned

Every incident should answer:

1. What happened?
2. Why did it happen?
3. Why wasn't it detected sooner?
4. What worked well?
5. What could be improved?
6. What actions will prevent recurrence?

The purpose of a postmortem is continuous improvement, not assigning blame.

---

# Core Principle

Production incidents are opportunities to improve systems, processes, and engineering practices.

Fix the system that allowed the failure, not just the failure itself.
