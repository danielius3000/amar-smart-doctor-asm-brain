---
title: ASM Brain Documentation Standard
version: v1.0
status: Approved Draft
owner: CTO Office
category: Navigation
created: 2026-08-05
updated: 2026-08-05
---

# ASM Brain Documentation Standard

## 1. Purpose

ASM Brain is the central knowledge operating system of Amar Smart Doctor.

This document defines the rules for creating, organizing, maintaining, and connecting documents inside ASM Brain.

The objective is to ensure ASM Brain remains:

- Structured
- Scalable
- Searchable
- Understandable by humans and AI systems
- Maintainable over many years

ASM Brain is not a collection of random notes.

Every document must have a clear purpose and responsibility.

---

# 2. Documentation Philosophy

## Knowledge First Principle

The primary asset of Amar Smart Doctor is structured knowledge.

Web pages, articles, social media content, videos, and future products are outputs generated from this knowledge.

The workflow is:

```
Knowledge → Content → Product → User Value
```

Therefore:

> Build and organize knowledge first. Publish outputs later.

---

## Single Source of Truth Principle

Each important concept should have one authoritative document.

Avoid:

- Duplicate documents
- Multiple competing versions
- Copy-paste information across folders

When information changes, update the source document.

---

# 3. ASM Brain Folder Responsibility

Each top-level folder has a specific responsibility.

---

## 00. Navigation

Purpose:

Defines how ASM Brain works.

Contains:

- Dashboard
- Documentation standards
- Navigation rules

---

## 10. Company

Purpose:

Defines Amar Smart Doctor's identity and strategic foundation.

Contains:

- Vision
- Mission
- Manifesto
- Company principles

---

## 20. Knowledge Bible

Purpose:

The core healthcare knowledge asset.

Contains:

- Medical knowledge models
- Disease knowledge structures
- Specialty knowledge
- Healthcare research

---

## 30. Product

Purpose:

Defines user-facing products and experiences.

Contains:

- Website strategy
- AI product planning
- User experience documentation

---

## 40. Engineering

Purpose:

Technical architecture and implementation decisions.

Contains:

- Architecture documents
- ADRs
- Technical specifications
- Engineering standards

---

## 80. Operations

Purpose:

Execution management and organizational workflow.

Contains:

- Current Sprint
- Reviews
- Decisions
- Operational processes

---

## 90. Archive

Purpose:

Preserve historical information.

Contains:

- Deprecated documents
- Previous versions
- Completed experiments

---

# 4. File Naming Convention

## General Rule

Files should use clear descriptive names.

Format:

```
Document Name.md
```

Examples:

```
Documentation Standard.md
Medical Knowledge Model.md
Healthcare Content Framework.md
```

Avoid unclear names:

```
doc1.md
new.md
final-final.md
```

---

## ADR Naming Convention

Technical decisions follow:

```
ADR-XXX Title.md
```

Example:

```
ADR-001 Repository Responsibility Principle.md
```

---

# 5. Standard Document Structure

Important documents should follow this structure:

```markdown
# Title

## Purpose

Why this document exists.

## Context

Background information.

## Main Content

Primary information.

## Decision / Conclusion

Final understanding or approved direction.

## Related Documents

Links to connected documents.

## Document Control

Version:
Status:
Owner:
Last Updated:
```

---

# 6. Linking Rules

ASM Brain uses Obsidian internal links.

Format:

```
[[Document Name]]
```

Rules:

- Link related concepts instead of duplicating information.
- Create meaningful relationships between documents.
- Avoid excessive unnecessary linking.
- Maintain clear knowledge connections.

---

# 7. Document Status System

Documents should use one of the following statuses:

## Draft

Initial creation stage.

## Review

Under evaluation.

## Approved

Accepted as the current standard.

## Deprecated

No longer active but preserved for history.

---

# 8. Version Control Rules

Important documents should use semantic versioning.

Format:

```
v1.0
v1.1
v2.0
```

## Major Version

Large structural changes.

Example:

```
v1.0 → v2.0
```

## Minor Version

Small improvements or updates.

Example:

```
v1.0 → v1.1
```

---

# 9. Review Process

Important documents should be periodically reviewed.

Review questions:

1. Is this information still accurate?
2. Is this document stored in the correct location?
3. Does another document duplicate this information?
4. Does this improve ASM Brain quality?

---

# 10. AI Usage Guidelines

AI is an accelerator for ASM Brain.

Approved AI usage:

- Research assistance
- Drafting documents
- Content generation
- Summarization
- SEO analysis
- Knowledge organization
- Automation

AI-generated information must be:

- Reviewed
- Verified
- Approved

AI assists knowledge creation but is not the source of truth.

---

# 11. Documentation Quality Standard

A high-quality ASM Brain document should be:

## Clear

Easy for humans and AI systems to understand.

## Structured

Follow consistent organization.

## Connected

Linked with related knowledge.

## Maintainable

Easy to update.

## Trustworthy

Based on verified information.

---

# Document Control

| Field | Value |
|---|---|
| Document | ASM Brain Documentation Standard |
| Version | v1.0 |
| Status | Approved Draft |
| Owner | CTO Office |
| Created | 2026-08-05 |
| Last Updated | 2026-08-05 |