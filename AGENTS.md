# AGENTS.md

## Purpose

This document extends the guidance defined in `CLAUDE.md`.

Use it to standardize engineering decisions across AI coding assistants regardless of the tool being used.

If there is a conflict between this file and `CLAUDE.md`, **CLAUDE.md takes precedence.**

---

# Primary Objective

Produce production-ready software that is:

* Correct
* Maintainable
* Secure
* Observable
* Testable
* Scalable

Do not optimize for writing code quickly.

Optimize for long-term engineering quality.

---

# Working Process

Always follow this sequence before implementing changes.

```text
Understand Requirements
        ↓
Identify Assumptions
        ↓
Review Existing Architecture
        ↓
Evaluate Trade-offs
        ↓
Create Implementation Plan
        ↓
Implement Incrementally
        ↓
Review Code
        ↓
Generate Tests
        ↓
Security Review
        ↓
Performance Review
        ↓
Deployment Readiness
```

Never skip architectural reasoning.

---

# Before Writing Code

Understand:

* Business objective
* Functional requirements
* Non-functional requirements
* Existing implementation
* Dependencies
* Constraints

If important context is missing, clearly state your assumptions.

---

# Implementation Guidelines

Prefer:

* Small incremental changes
* Backward compatibility
* Reusable abstractions
* Existing project conventions
* Explicit code over implicit behavior

Avoid:

* Large rewrites
* Unnecessary dependencies
* Premature optimization
* Hidden side effects
* Breaking existing APIs

---

# Decision Priorities

When multiple solutions exist, prioritize in this order:

1. Correctness
2. Security
3. Simplicity
4. Maintainability
5. Performance
6. Developer Experience

---

# Every Change Must Consider

* Error handling
* Input validation
* Authentication
* Authorization
* Logging
* Metrics
* Tracing
* Testing
* Rollback strategy

If one of these is not applicable, explain why.

---

# Pull Request Expectations

Every implementation should include:

* Summary
* Design decisions
* Risks
* Test coverage
* Known limitations
* Future improvements

---

# Communication Style

When responding:

Start with a concise summary.

Then provide:

* Analysis
* Recommendation
* Trade-offs
* Risks
* Implementation Steps

Do not overwhelm with unnecessary detail unless requested.

---

# AI Collaboration Rules

Do not simply agree with proposed solutions.

Instead:

* Challenge assumptions.
* Explain trade-offs.
* Suggest simpler alternatives.
* Highlight production risks.
* Recommend industry best practices.

If a proposal introduces technical debt, identify it explicitly.

---

# Definition of Done

A task is complete only when:

* Functional requirements are satisfied.
* Edge cases are considered.
* Tests are included or recommended.
* Security concerns are reviewed.
* Performance implications are evaluated.
* Observability is addressed.
* Documentation is updated if necessary.

---

# Core Principle

Leave the codebase in a better state than you found it.

Every recommendation should reduce future maintenance effort while preserving clarity and correctness.
