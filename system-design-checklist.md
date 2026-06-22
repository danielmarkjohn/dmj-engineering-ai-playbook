# system-design-checklist.md

# System Design Checklist

This checklist is used before approving or implementing any significant backend service, API, or distributed system.

The objective is to identify production risks early and ensure every system is operationally ready.

---

# 1. Business Requirements

* [ ] Business problem is clearly defined
* [ ] Success metrics are identified
* [ ] Customer impact is understood
* [ ] Scope is documented
* [ ] Assumptions are explicitly stated

---

# 2. Functional Requirements

* [ ] Core functionality documented
* [ ] Edge cases identified
* [ ] Failure scenarios considered
* [ ] User flows validated
* [ ] Backward compatibility reviewed

---

# 3. API Design

* [ ] RESTful resource naming
* [ ] API versioning strategy
* [ ] Authentication implemented
* [ ] Authorization enforced
* [ ] Request validation
* [ ] Consistent response format
* [ ] Error contract defined
* [ ] Pagination supported
* [ ] Filtering supported
* [ ] Sorting supported
* [ ] Rate limiting defined
* [ ] Idempotency considered

---

# 4. Data Layer

* [ ] Database technology selected appropriately
* [ ] Schema reviewed
* [ ] Indexes planned
* [ ] Transactions identified
* [ ] Data consistency model defined
* [ ] Migration strategy prepared
* [ ] Rollback strategy documented
* [ ] Retention policy defined

---

# 5. Scalability

* [ ] Expected traffic estimated
* [ ] Peak load identified
* [ ] Horizontal scaling possible
* [ ] Stateless services where appropriate
* [ ] Caching opportunities evaluated
* [ ] Bottlenecks identified

---

# 6. Reliability

* [ ] Timeouts configured
* [ ] Retry policy defined
* [ ] Circuit breakers considered
* [ ] Graceful degradation available
* [ ] Dead-letter queue required?
* [ ] Dependency failures handled

---

# 7. Security

* [ ] Authentication reviewed
* [ ] Authorization reviewed
* [ ] Input validation
* [ ] Output encoding
* [ ] Secrets protected
* [ ] Sensitive data encrypted
* [ ] OWASP Top 10 considered
* [ ] Audit logging required

---

# 8. Performance

* [ ] Database queries optimized
* [ ] N+1 queries eliminated
* [ ] Payload sizes minimized
* [ ] Parallel execution considered
* [ ] Compression enabled
* [ ] Caching strategy documented
* [ ] Performance targets defined

---

# 9. Observability

* [ ] Structured logging
* [ ] Metrics exposed
* [ ] Distributed tracing
* [ ] Health endpoints
* [ ] Dashboards created
* [ ] Alert thresholds defined
* [ ] Runbook available

---

# 10. Deployment

* [ ] Feature flags available
* [ ] CI/CD pipeline updated
* [ ] Infrastructure changes reviewed
* [ ] Database migrations tested
* [ ] Rollback tested
* [ ] Canary or phased rollout planned

---

# 11. Testing

* [ ] Unit tests
* [ ] Integration tests
* [ ] API contract tests
* [ ] Security testing
* [ ] Performance testing
* [ ] Load testing (if required)
* [ ] Regression testing

---

# 12. Operational Readiness

* [ ] On-call ownership defined
* [ ] Incident response documented
* [ ] SLA/SLO reviewed
* [ ] Capacity planning completed
* [ ] Backup and recovery verified

---

# Design Review Questions

Before approving any design, ask:

1. Is this solving the correct problem?
2. Is this the simplest viable solution?
3. Can another engineer understand and maintain it?
4. What happens if a dependency fails?
5. Can this be rolled back safely?
6. How will we detect failures?
7. How will we measure success?
8. What technical debt does this introduce?

---

# Approval Decision

## ✅ Approve

The design is production-ready with acceptable risk.

## ⚠️ Approve with Changes

Minor improvements are required before implementation.

## ❌ Block

The design introduces unacceptable business, operational, security, or architectural risk.

Blocking decisions should always include actionable recommendations.

---

# Engineering Principle

A successful system is not one that only works in development.

A successful system is one that can be deployed, monitored, scaled, operated, and maintained confidently in production.
