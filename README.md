# Engineering AI Playbook

A practical AI-assisted engineering workflow for software architecture, system design, implementation, code reviews, incident response, and engineering management.

---

## Overview

This repository contains the AI configuration, engineering standards, and reusable workflows I use to improve software quality and developer productivity.

The goal is not to replace engineering judgment, but to augment it by making architecture decisions more consistent, code reviews more thorough, and engineering practices more repeatable.

AI is treated as a senior engineering collaborator rather than a code generator.

---

# Philosophy

The best engineering teams optimize for:

* Maintainability over cleverness
* Simplicity over unnecessary complexity
* Long-term scalability over short-term speed
* Observability over debugging
* Automation over repetitive work
* Engineering judgment over blind AI suggestions

Every AI interaction should improve software quality while reducing cognitive load for engineers.

---

# Repository Structure

```
.
├── README.md
├── CLAUDE.md
├── AGENTS.md
├── prompts.md
```

---

# What's Included

## CLAUDE.md

The primary AI configuration.

Defines engineering standards, architecture expectations, code review workflow, communication style, and production engineering principles.

---

## AGENTS.md

Additional operating instructions for AI coding assistants.

Provides reusable guidance across multiple AI tools.

---

## prompts.md

A collection of reusable prompts for common engineering tasks, including:

* Architecture reviews
* Pull request reviews
* Root cause analysis
* System design
* Performance optimization
* Technical documentation

---

## architecture-review.md

A structured framework for reviewing technical designs, evaluating trade-offs, identifying risks, and making architectural recommendations.

---

## system-design-checklist.md

A production readiness checklist covering APIs, scalability, observability, resilience, deployment, rollback strategy, and operational concerns.

---

## code-review-checklist.md

A practical checklist for reviewing pull requests with consistent engineering standards.

Reviews are categorized into:

* Blocking
* Major
* Minor
* Suggestions

---

## incident-response.md

A structured incident investigation workflow focused on:

* Root Cause
* Impact
* Blast Radius
* Recovery
* Prevention

---

## engineering-principles.md

Core engineering values and decision-making principles used to maintain consistency across projects and teams.

---

# AI Workflow

My typical engineering workflow looks like this:

```
Requirements
      │
      ▼
Architecture Review
      │
      ▼
System Design
      │
      ▼
Implementation Plan
      │
      ▼
Code Generation
      │
      ▼
Self Review
      │
      ▼
Testing
      │
      ▼
Security Review
      │
      ▼
Performance Review
      │
      ▼
Deployment Checklist
```

AI assists throughout the process but does not replace engineering ownership or decision-making.

---

# Typical Use Cases

This repository is used for:

* Software architecture reviews
* Backend API design
* Frontend architecture
* Pull request reviews
* Engineering documentation
* Technical design discussions
* Production incident investigations
* Performance optimization
* Security reviews
* Engineering management decisions
* Sprint planning
* Technical debt analysis

---

# Guiding Principles

Every recommendation should answer four questions:

1. Is it correct?
2. Is it maintainable?
3. Is it scalable?
4. Is it simple?

If the answer to any of these is "no", the solution should be reconsidered.

---

# Disclaimer

This repository intentionally contains no proprietary code, internal documentation, customer information, or employer-specific configuration.

All examples and workflows are generic engineering practices designed to be reusable across projects and organizations.

---

# Continuous Improvement

Engineering practices evolve.

This repository is intended to grow over time as new tools, workflows, and lessons are incorporated through real-world software development and engineering leadership experience.
