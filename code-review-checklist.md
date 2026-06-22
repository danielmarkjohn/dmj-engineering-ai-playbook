# code-review-checklist.md

# Code Review Checklist

This checklist standardizes how pull requests are reviewed to improve code quality, reduce production defects, and maintain consistent engineering standards.

The objective of a code review is not to find fault with the author. It is to improve the software before it reaches production.

---

# Review Philosophy

Every review should answer three questions:

1. Is the implementation correct?
2. Can another engineer easily maintain it?
3. Is it safe to deploy?

If the answer to any question is "No", the review should explain why and recommend improvements.

---

# Review Process

Every pull request should be reviewed in the following order.

```text
Understand the Problem
        ↓
Review Overall Design
        ↓
Review Business Logic
        ↓
Review Edge Cases
        ↓
Review Security
        ↓
Review Performance
        ↓
Review Testing
        ↓
Review Production Readiness
        ↓
Approve or Request Changes
```

Never begin by reviewing formatting.

---

# 🔴 Blocking Issues

These should prevent a merge until resolved.

## Correctness

* [ ] Business logic is incorrect
* [ ] Functional requirements are not met
* [ ] Edge cases are missing
* [ ] Breaking existing functionality

---

## Security

* [ ] Missing authentication
* [ ] Missing authorization
* [ ] SQL / NoSQL injection risk
* [ ] Sensitive information exposed
* [ ] Secrets committed
* [ ] Input validation missing

---

## Data Integrity

* [ ] Race conditions
* [ ] Missing transactions
* [ ] Duplicate writes possible
* [ ] Data corruption risk
* [ ] Idempotency missing where required

---

## Reliability

* [ ] No timeout handling
* [ ] Retry strategy missing
* [ ] Unhandled exceptions
* [ ] Dependency failures ignored

---

# 🟡 Major Issues

These should normally be fixed before merging.

* [ ] Poor architecture
* [ ] Large methods
* [ ] Duplicate logic
* [ ] Tight coupling
* [ ] Poor naming
* [ ] Missing logging
* [ ] Missing metrics
* [ ] Missing tracing
* [ ] Missing documentation
* [ ] Missing integration tests

---

# 🟢 Minor Issues

These improve readability and consistency.

* [ ] Formatting
* [ ] Readability
* [ ] Better naming
* [ ] Small refactoring
* [ ] Documentation improvements
* [ ] Comment cleanup

---

# ⚡ Performance Review

Check for:

* [ ] N+1 database queries
* [ ] Missing indexes
* [ ] Large payloads
* [ ] Blocking operations
* [ ] Sequential work that could run in parallel
* [ ] Missing caching
* [ ] Memory leaks

---

# 🔒 Security Review

Verify:

* [ ] Authentication
* [ ] Authorization
* [ ] Input validation
* [ ] Output encoding
* [ ] Rate limiting
* [ ] Secret management
* [ ] Audit logging

---

# 📊 Observability

Ensure the implementation includes:

* [ ] Structured logging
* [ ] Metrics
* [ ] Distributed tracing
* [ ] Health checks
* [ ] Meaningful error messages
* [ ] Monitoring support

---

# 🧪 Testing

Verify appropriate coverage.

* [ ] Unit tests
* [ ] Integration tests
* [ ] API tests
* [ ] Negative tests
* [ ] Boundary conditions
* [ ] Regression tests

If tests are missing, explain what should be added.

---

# 🚀 Deployment Readiness

Before approving verify:

* [ ] Feature flag required?
* [ ] Database migration reviewed?
* [ ] Rollback possible?
* [ ] Backward compatible?
* [ ] Configuration changes documented?
* [ ] Operational impact understood?

---

# Review Feedback Format

Every review should follow this structure.

```text
Summary

🔴 Blocking

🟡 Major

🟢 Minor

💡 Suggestions

Decision
```

---

# Decision

Choose one:

## ✅ Approve

Implementation is production ready.

---

## ⚠️ Approve with Changes

Minor improvements are required but do not introduce significant risk.

---

## ❌ Block

The implementation introduces unacceptable business, security, architectural, or operational risk.

Every blocking decision should include:

* Why it is blocked
* Business impact
* Recommended solution

---

# Reviewer Principles

A reviewer should:

* Protect production quality.
* Coach rather than criticize.
* Explain the reasoning behind feedback.
* Prefer evidence over opinion.
* Encourage simpler solutions when appropriate.
* Recognize good engineering decisions.

A successful review improves both the software and the engineer who wrote it.

---

# Core Principle

Review the design before reviewing the syntax.

The highest value feedback improves architecture, correctness, reliability, and maintainability rather than formatting or style.
