# Documentation Standard

**Status:** Approved  
**Owner:** Founder & CTO  
**Version:** 1.0

---

# Purpose

This document defines how documentation is created, organized, reviewed, and maintained throughout the Amar Smart Doctor project.

The goal is to ensure every document is:

- Easy to understand
- Easy to maintain
- AI-friendly
- Human-friendly
- Consistent across the entire project

ASM Brain is the single source of truth for all project knowledge.

---

# Documentation Principles

## 1. Single Source of Truth (SSOT)

Every important piece of information must exist in only one location.

Other documents should reference it using Obsidian links instead of duplicating content.

Example:

```
[[Vision]]
[[PRD]]
[[Roadmap]]
```

---

## 2. Atomic Documentation

Each document should have one primary responsibility.

Good examples:

- Vision
- PRD
- Roadmap
- Healthcare Taxonomy

Avoid combining unrelated topics into one document.

---

## 3. Modular Knowledge

Prefer many small documents over one massive document.

Large documents become difficult to maintain.

Split documents only when doing so improves clarity.

---

## 4. Documentation Before Memory

Project knowledge belongs in ASM Brain.

Do not rely on conversation history or AI memory as the long-term source of information.

---

# Naming Convention

## Folders

Use:

Title Case

Examples:

```
Knowledge Bible
Operations
Research
```

Top-level folders use numeric prefixes for ordering.

Example:

```
20. Product
21. Knowledge Bible
22. Operations
```

---

## Documents

Use:

Title Case.md

Examples:

```
Vision.md
PRD.md
Current Sprint.md
Healthcare Taxonomy.md
```

Do not use:

- Dates
- Version numbers
- "Final"
- "Final Final"

Git manages version history.

---

# Internal Linking

Whenever another document already exists, reference it using Obsidian links.

Example:

```
[[Vision]]
[[PRD]]
[[Roadmap]]
```

Avoid copying information between documents.

---

# Standard Document Structure

Every major document should contain the sections that are relevant from the list below.

```
# Title

## Purpose

## Background

## Scope

## Content

## Decisions

## Related Documents

## Open Questions
```

Not every document requires every section.

Keep documents concise.

---

# Document Lifecycle

Every document follows this lifecycle.

```
Draft

↓

Review

↓

Approved

↓

Archived
```

Only approved documents become part of the project's official knowledge.

---

# Writing Guidelines

Documentation should be:

- Clear
- Accurate
- Concise
- Practical
- Actionable

Avoid:

- Marketing language
- Repetition
- Unnecessary complexity
- Assumptions presented as facts

---

# Quality Checklist

Before approving any document, verify:

- Correct
- Complete
- Concise
- Reusable
- Maintainable

If any answer is "No", revise the document before approval.

---

# Review Process

Every important document should be reviewed before becoming part of ASM Brain.

Review should verify:

- Structure
- Accuracy
- Consistency
- Scope
- Long-term maintainability

---

# Versioning

Git is the official version control system.

Do not create filenames such as:

```
PRD_v2.md
Roadmap_Final.md
Vision_Final_Final.md
```

Version history belongs in Git.

---

# Future Improvements

Future versions of this standard may include:

- Metadata (YAML Front Matter)
- Document IDs
- Templates
- AI Agent compatibility
- Automated documentation validation

These will be introduced only when they provide clear value.

---

# Guiding Principle

Write documentation that is easy for both humans and AI to understand.

If a document cannot be understood six months later without additional explanation, it should be improved.