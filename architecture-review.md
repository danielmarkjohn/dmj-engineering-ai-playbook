# architecture-review.md

# Architecture Review Framework

This document defines the framework I use when reviewing technical designs, architecture proposals, and major engineering initiatives.

The objective is to ensure every design is scalable, maintainable, observable, and aligned with business goals before implementation begins.

---

# Review Process

Every architecture review follows this sequence:

```text
Understand Business Problem
          ↓
Clarify Functional Requirements
          ↓
Identify Non-functional Requirements
          ↓
Evaluate Existing Architecture
          ↓
Review Proposed Solution
          ↓
Analyze Trade-offs
          ↓
Identify Risks
          ↓
Recommend Improvements
          ↓
Approve or Block
```

Architecture reviews should happen **before implementation**, not after.

---

# 1. Business Alignment

Understand:

* What business problem is being solved?
* What customer pain point exists?
* Why is this solution needed now?
* What happens if we do nothing?
* How will success be measured?

A technically elegant solution that does not solve the business problem is a poor solution.

---

# 2. Functional Requirements

Verify:

* Core functionality
* Edge cases
* User workflows
* Failure scenarios
* Backward compatibility

Requirements should be explicit rather than assumed.

---

# 3. Non-functional Requirements

Every design should evaluate:

* Scalability
* Reliability
* Availability
* Performance
* Security
* Maintainability
* Cost
* Compliance
* Developer Experience

These are first-class requirements.

---

# 4. API Design

Review:

* Resource naming
* Versioning strategy
* Authentication
* Authorization
* Validation
* Error contracts
* Idempotency
* Pagination
* Filtering
* Rate limiting

Public interfaces should remain stable.

---

# 5. Data Design

Evaluate:

* Data model
* Relationships
* Indexes
* Transactions
* Consistency
* Schema evolution
* Migration strategy
* Rollback strategy
* Data retention

Poor data models become long-term technical debt.

---

# 6. Scalability

Determine:

* Expected traffic
* Peak load
* Growth projections
* Horizontal scaling strategy
* Vertical scaling limitations
* Statelessness
* Bottlenecks

Design for realistic growth, not theoretical maximums.

---

# 7. Reliability

Review:

* Retry strategy
* Timeouts
* Circuit breakers
* Dead-letter queues
* Graceful degradation
* Dependency failures
* Disaster recovery

Assume downstream systems will eventually fail.

---

# 8. Performance

Evaluate:

* Network calls
* Database queries
* Caching opportunities
* Parallel execution
* Payload size
* Latency targets
* Throughput expectations

Measure performance rather than guessing.

---

# 9. Security

Every design must consider:

* Authentication
* Authorization
* Encryption
* Secret management
* Input validation
* Injection attacks
* Least privilege
* Audit logging

Security should be designed in, not added later.

---

# 10. Observability

Production systems should include:

* Structured logging
* Metrics
* Distributed tracing
* Dashboards
* Alerts
* Health endpoints
* Runbooks

If a failure cannot be observed, it cannot be managed effectively.

---

# 11. Operational Readiness

Review:

* Deployment strategy
* Feature flags
* Rollback plan
* Database migrations
* Monitoring
* Incident response
* On-call considerations

Shipping code is only part of delivering software.

---

# 12. Engineering Impact

Consider:

* Development effort
* Team ownership
* Documentation
* Knowledge sharing
* Long-term maintenance
* Technical debt
* Developer productivity

The best architecture is one that teams can successfully operate.

---

# Architecture Decision Record

Every major design should answer:

## What problem are we solving?

---

## Why is this solution preferred?

---

## Alternatives considered

* Option A
* Option B
* Option C

Why were they rejected?

---

## Risks

Technical

Operational

Business

---

## Mitigation Strategy

How will each risk be reduced?

---

## Success Metrics

Examples:

* Deployment frequency
* Error rate
* API latency
* System availability
* Infrastructure cost
* MTTR
* Customer satisfaction

Architecture decisions should define measurable outcomes.

---

# Approval Criteria

## ✅ Approve

The design:

* Solves the business problem
* Meets functional requirements
* Meets non-functional requirements
* Is operationally ready
* Is maintainable
* Has acceptable risk

---

## ⚠️ Approve with Changes

The design is fundamentally sound but requires improvements before implementation.

Examples:

* Missing observability
* Incomplete rollback plan
* Weak API contract
* Missing security controls

---

## ❌ Block

The proposal should not proceed if it introduces unacceptable risk such as:

* Data integrity issues
* Security vulnerabilities
* Poor scalability
* Missing failure handling
* Excessive operational complexity
* Undefined ownership

Blocking feedback should always include recommended alternatives.

---

# Guiding Principles

Every architecture review should answer five questions:

1. Does it solve the right problem?
2. Can it scale with the business?
3. Can engineers maintain it?
4. Can operators support it?
5. Will this still be a good decision in two years?

If the answer to any question is "no", revisit the design before implementation.
