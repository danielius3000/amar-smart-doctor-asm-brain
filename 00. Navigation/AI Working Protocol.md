---
title: AI Working Protocol
version: v1.0
status: Approved Draft
owner: CTO Office
category: Navigation
created: 2026-08-05
updated: 2026-08-05
---

# AI Working Protocol

## 1. Purpose

This document defines how AI assistants are used within ASM Brain.

The goal is to use AI as an accelerator while maintaining human control, accuracy, and trust.

---

# 2. AI Role in ASM Brain

AI acts as:

- Research assistant
- Documentation assistant
- Analysis assistant
- Content generation assistant
- Automation assistant

AI does not act as:

- Final authority
- Source of truth
- Independent decision maker

---

# 3. Source of Truth Principle

ASM Brain documents are the source of truth.

AI-generated information must not automatically become official knowledge.

Before becoming part of ASM Brain:

AI output must be:

1. Reviewed
2. Verified
3. Approved

---

# 4. Approved AI Usage

AI may assist with:

## Research

- Finding information
- Summarizing research
- Comparing concepts

## Documentation

- Drafting documents
- Improving clarity
- Creating structure

## Content Development

- Transforming knowledge into user-facing formats
- SEO assistance
- Translation support

## Engineering

- Reviewing architecture
- Suggesting improvements
- Explaining technical concepts

---

# 5. Restricted AI Usage

AI should not independently:

- Publish medical advice
- Approve medical claims
- Replace expert review
- Modify critical knowledge without approval

---

# 6. Human Approval Requirement

The following require human approval:

- Medical knowledge
- Patient-facing information
- Product decisions
- Architecture decisions
- Business strategy

---

# 7. AI Collaboration Workflow

Recommended workflow:

```
Human Question
        ↓
AI Assistance
        ↓
Human Review
        ↓
ASM Brain Update
        ↓
Git Commit
        ↓
Version History
```

---

# 8. AI Quality Standard

AI-generated work should be:

- Accurate
- Structured
- Traceable
- Reviewable
- Maintainable

---

# Document Control

| Field    | Value               |
| -------- | ------------------- |
| Document | AI Working Protocol |
| Version  | v1.0                |
| Status   | Approved Draft      |
| Owner    | CTO Office          |
| Created  | 2026-08-05          |