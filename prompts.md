# prompts.md

# Reusable Engineering Prompts

This document contains the reusable prompts I use during software architecture, engineering management, code reviews, debugging, and production support.

These prompts are intended to improve consistency rather than replace engineering judgment.

---

# 1. Architecture Review

## Objective

Review a technical design like a Staff or Principal Engineer.

## Prompt

```
Review this architecture proposal as a senior software architect.

Evaluate:

• Business requirements
• Scalability
• Reliability
• Security
• Performance
• Operational complexity
• Cost
• Developer experience

Identify:

• Strengths
• Risks
• Missing considerations
• Trade-offs
• Questions for the author

Finish with:

Approve
Approve with Changes
Block

Explain why.
```

---

# 2. Pull Request Review

## Objective

Perform a production-quality code review.

## Prompt

```
Review this Pull Request as a senior engineering lead.

Categorize findings as:

🔴 Blocking
🟡 Major
🟢 Minor
💡 Suggestions

Evaluate:

• Correctness
• Security
• Performance
• Error handling
• Maintainability
• Readability
• Testing
• Observability

Conclude with:

Approve
Approve with Changes
Block

Include reasoning for each decision.
```

---

# 3. System Design Review

## Objective

Evaluate the design before implementation.

## Prompt

```
Review this system design.

Evaluate:

Requirements

Architecture

API design

Data model

Caching

Concurrency

Scalability

Failure scenarios

Deployment

Rollback

Observability

Identify bottlenecks and recommend improvements.
```

---

# 4. Root Cause Analysis

## Objective

Investigate production incidents.

## Prompt

```
Analyze this production issue.

Determine:

Root Cause

Symptoms

Impact

Blast Radius

Immediate Recovery

Long-term Prevention

Operational Improvements

Engineering Process Improvements

Avoid stopping at the first observed symptom.
```

---

# 5. API Review

## Objective

Evaluate REST or GraphQL APIs.

## Prompt

```
Review this API.

Evaluate:

Naming

HTTP status codes

Authentication

Authorization

Validation

Pagination

Filtering

Versioning

Error responses

Rate limiting

Idempotency

Backward compatibility

Recommend improvements where appropriate.
```

---

# 6. Database Review

## Objective

Review database schema and queries.

## Prompt

```
Review this database design.

Evaluate:

Indexes

Normalization

Query performance

Transactions

Lock contention

Data integrity

Migration strategy

Rollback strategy

Potential scalability concerns
```

---

# 7. Security Review

## Objective

Perform a production security assessment.

## Prompt

```
Review this implementation for security.

Check for:

Authentication

Authorization

SQL Injection

NoSQL Injection

XSS

CSRF

Sensitive data exposure

Secrets management

Dependency risks

Privilege escalation

Provide remediation steps for each issue found.
```

---

# 8. Performance Review

## Objective

Identify performance bottlenecks.

## Prompt

```
Analyze this implementation for performance.

Look for:

N+1 queries

Blocking operations

Large payloads

Repeated work

Missing caching

Memory leaks

CPU hotspots

Network latency

Database bottlenecks

Suggest measurable optimizations.
```

---

# 9. Sprint Planning

## Objective

Break work into executable tasks.

## Prompt

```
Act as an Engineering Manager.

Break this feature into deliverable tasks.

Estimate:

Complexity

Dependencies

Risks

Testing effort

Deployment strategy

Rollback considerations

Highlight work that can run in parallel.
```

---

# 10. Technical Debt Assessment

## Objective

Identify engineering debt before it becomes a delivery problem.

## Prompt

```
Review this codebase.

Identify:

Architectural debt

Code smells

Operational risks

Maintainability issues

Documentation gaps

Testing gaps

Deployment risks

Rank findings by business impact and engineering effort.
```

---

# General Prompting Principles

Every engineering prompt should encourage the AI to:

* Challenge assumptions instead of agreeing.
* Explain trade-offs.
* Identify production risks.
* Consider scalability.
* Consider operational excellence.
* Recommend industry best practices.
* Distinguish facts from assumptions.
* Prefer maintainable solutions over clever implementations.

---

# Philosophy

AI should function as an experienced engineering partner.

Its primary purpose is to improve decision quality, reduce repetitive work, and help engineers make better technical decisions while keeping humans responsible for final judgment.
