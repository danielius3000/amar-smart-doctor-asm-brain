# Engineering Principles

**Project:** ASM Core

**Status:** Approved

**Version:** 1.0

---

# Purpose

This document defines the engineering principles that guide every architectural, technical, and implementation decision for ASM Core.

These principles take precedence over convenience, speed, or personal preference.

---

# Core Philosophy

ASM Core exists to solve Amar Smart Doctor's real operational problems before becoming a reusable platform.

We optimize for long-term maintainability, simplicity, reliability, and knowledge integrity.

---

# Principle 1 — Knowledge First

Knowledge is the primary asset.

Software exists to serve knowledge—not the other way around.

ASM Brain is the single source of truth.

---

# Principle 2 — Human Approved Knowledge

AI may draft.

AI may recommend.

AI may analyze.

Only humans approve permanent knowledge changes.

---

# Principle 3 — Markdown First

Markdown remains the canonical knowledge format.

Knowledge should never become locked inside proprietary databases.

---

# Principle 4 — Git Everything

Every important change should be version controlled.

Knowledge evolves.

Engineering evolves.

Decisions evolve.

History must never be lost.

---

# Principle 5 — Simplicity Before Intelligence

Never introduce complexity before it solves a real problem.

Simple systems are easier to understand, maintain, and trust.

---

# Principle 6 — Build for Amar Smart Doctor First

ASM Core is built to solve Amar Smart Doctor's needs.

Generalization comes only after real-world validation.

---

# Principle 7 — AI Retrieves Context

AI should retrieve relevant knowledge instead of relying on conversation memory.

Knowledge retrieval should be deterministic whenever possible.

---


# Principle 8 — Documentation Drives Development

Approved documentation comes before implementation.

Engineering follows decisions—not assumptions.

---

# Principle 9 — Small, Incremental Progress

Prefer small working improvements over large unfinished systems.

Ship.

Learn.

Improve.

Repeat.

---

# Principle 10 — AI Assists, Humans Decide

AI accelerates engineering.

Humans remain responsible for product direction, medical integrity, and final approval.

---

# Principle 11 — Context Before Reasoning

AI should never reason without first receiving an approved context package.

ASM Core is responsible for assembling trusted context before intelligence begins processing.

Reasoning without context increases inconsistency, reduces trust, and weakens organizational knowledge.

---


# Success Criteria

Every engineering decision should satisfy the following questions:

- Does this reduce complexity?
- Does this improve maintainability?
- Does this preserve knowledge?
- Does this support future AI agents?
- Would this still make sense in five years?

If the answer is "No", reconsider the decision.

---

# Related Documents

- [[ASM Core Vision]]
- [[ASM Core Architecture]]
- [[ASM Core PRD]]
- [[MCP Integration]]

---

# Review History

| Version | Status | Reviewer |
|----------|---------|----------|
| 1.0 | Approved | Founder & CTO 