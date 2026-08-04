---
title: AI Collaboration Guidelines
version: v1.0
status: Approved Draft
owner: CTO Office
category: Operations
created: 2026-08-05
updated: 2026-08-05
---

# AI Collaboration Guidelines

## 1. Purpose

This document defines the practical workflow for using AI assistants while working on ASM Brain.

The objective is to make AI collaboration consistent, efficient, and safe.

---

# 2. Working Relationship

ASM Brain follows this model:

```
Human Direction
        ↓
AI Assistance
        ↓
Human Review
        ↓
Knowledge Update
        ↓
Git Version Control
```

Human remains responsible for final decisions.

---

# 3. When to Use AI

AI should be used for:

## Research Support

Examples:

- Exploring new ideas
- Summarizing information
- Comparing approaches
- Identifying risks

---

## Documentation Support

Examples:

- Creating first drafts
- Improving structure
- Finding inconsistencies
- Maintaining standards

---

## Technical Support

Examples:

- Reviewing architecture
- Explaining technologies
- Suggesting implementation approaches

---

## Content Transformation

Examples:

- Turning knowledge into articles
- Creating social media formats
- Translating content

---

# 4. When Human Review Is Required

Human approval is required before:

- Adding medical knowledge
- Publishing healthcare content
- Changing architecture decisions
- Modifying company strategy
- Making patient-facing claims

---

# 5. Recommended Prompt Structure

When requesting AI assistance, provide:

## Context

What is the project or document?

## Objective

What needs to be achieved?

## Constraints

What limitations exist?

## Expected Output

What format is required?

Example:

```
Context:
ASM Brain healthcare knowledge system

Objective:
Create disease knowledge model

Constraints:
Must be structured and SEO-friendly

Output:
Markdown document
```

---

# 6. Document Creation Workflow

For new documents:

1. Define purpose
2. Create draft
3. Review structure
4. Verify information
5. Save in correct location
6. Commit changes to Git

---

# 7. Change Management

Every significant ASM Brain update should follow:

```
Edit
 ↓
Review
 ↓
Git Commit
 ↓
Git Push
```

Commit messages should describe the change.

Good:

```
Add healthcare knowledge model foundation
```

Avoid:

```
Update files
```

---

# 8. AI Limitations

AI may produce:

- Incorrect information
- Missing context
- Outdated information
- Unsupported assumptions

Therefore:

AI output must always be reviewed.

---

# Document Control

| Field    | Value                       |
| -------- | --------------------------- |
| Document | AI Collaboration Guidelines |
| Version  | v1.0                        |
| Status   | Approved Draft              |
| Owner    | CTO Office                  |
| Created  | 2026-08-05                  |