# ADR-001 — Repository Responsibility Principle

## Status

Approved

---

## Date

2026-08-05

---

## Context

As Amar Smart Doctor grows, multiple independent assets will evolve at different speeds.

Keeping all knowledge, software, and products inside a single repository would create unnecessary coupling, reduce maintainability, and make future expansion difficult.

---

## Decision

Each repository must have one clear responsibility.

### Repository 1 — asm-brain

Purpose:

The single source of truth for all approved organizational knowledge.

Contains:

- Company documentation
- Product documentation
- Medical knowledge
- Engineering documentation
- Operations
- Research
- Decision records

Does NOT contain:

- Application code
- MCP implementation
- Product source code

---

### Repository 2 — asm-core

Purpose:

The Knowledge Engine responsible for retrieving, searching, understanding, and preparing context from ASM Brain.

Contains:

- MCP Server
- Context Engine
- Retrieval
- Search
- AI integrations
- Tests

Does NOT contain:

- Business documentation
- Product documentation
- Medical knowledge

---

### Repository 3 — amar-smart-doctor

Purpose:

The user-facing application.

Contains:

- Website
- Backend
- API
- Authentication
- Doctor platform
- SEO pages
- User experience

Consumes ASM Core.

Does NOT contain:

- Knowledge source
- Knowledge retrieval engine

---

## Principles

Knowledge is independent.

The Knowledge Engine is independent.

Products are independent.

Each evolves independently.

---

## Consequences

Benefits:

- Loose coupling
- Independent versioning
- Easier maintenance
- Easier scaling
- Reusable Knowledge Engine
- Reusable Knowledge Base

Trade-offs:

- More repositories
- Clear interface definitions required

These trade-offs are acceptable.

---

## Rationale

ASM Brain is the company's intellectual property.

ASM Core is the software that understands that knowledge.

Applications consume the services provided by ASM Core.

Separating these responsibilities creates a cleaner architecture and supports future expansion without restructuring.