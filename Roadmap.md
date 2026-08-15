# Amar Smart Doctor — Master Roadmap

**Document ID:** ASM-ROADMAP-001
**Document Name:** Amar Smart Doctor Master Roadmap
**Version:** 1.3
**Status:** Active
**Owner:** Amar Smart Doctor
**System:** ASM Brain
**Repository:** amar-smart-doctor-asm-brain
**Created:** 2026-08-08
**Updated:** 2026-08-15

---

# 1. Purpose

This document is the controlling roadmap for the Amar Smart Doctor project.

It defines:

- the long-term product direction
- major project phases
- milestones
- current project state
- milestone dependencies
- major deliverables
- completion criteria
- public MVP direction
- long-term expansion

All significant project work should be traceable to a roadmap milestone.

---

# 2. Roadmap Authority

This roadmap is the controlling planning document for Amar Smart Doctor.

The roadmap does not replace detailed specifications.

The relationship is:

```text
Master Roadmap
      ↓
   Milestone
      ↓
Architecture / Specification
      ↓
  Implementation
      ↓
   Verification
      ↓
     Release
```

Individual standards and architecture documents remain authoritative for their respective domains.

The roadmap determines:

- what should be worked on
- in what broad sequence
- why the work exists
- when a milestone is considered complete

Domain standards determine:

- how that domain is governed
- what rules apply
- what implementation must respect

---

# 3. North Star

> **Amar Smart Doctor is an AI-native Healthcare Knowledge Platform.**

The long-term architecture is based on three major layers:

```text
AMAR SMART DOCTOR
        │
┌───────┴────────┐
│                │
KNOWLEDGE     INTELLIGENCE
  LAYER          LAYER
│                │
│                ├── AI Workforce
│                ├── Human Workforce
│                ├── Governance
│                └── Orchestration
│
├── Knowledge Assets
├── Evidence
├── Taxonomy
└── Relationships
        │
        └───────────────┐
                        │
                   EXPERIENCE
                      LAYER
                        │
          ┌─────────────┴─────────────┐
          │             │             │
       Website       Mobile        APIs
          │
       Search
       Chat
       Education
       Future Products
```

The central product principle is:

> **Knowledge is created once, governed continuously, and reused across many products.**

The website is therefore a consumer of the Knowledge Platform, not the Knowledge Platform itself.

---

# 4. Strategic Product Philosophy

Amar Smart Doctor is built around structured medical knowledge rather than traditional article production.

The primary asset is:

> **Governed medical knowledge.**

Pages, articles, videos, social content, search experiences, AI experiences, and future products are outputs generated from that knowledge.

Therefore:

```text
Knowledge
    ↓
Governed Knowledge Assets
    ↓
Platform
    ↓
Multiple Experiences
    ↓
Multiple Products
```

AI is an accelerator, not the source of truth.

AI may assist with:

- research
- evidence discovery
- knowledge extraction
- structuring
- content generation
- translation
- SEO
- analysis
- automation

AI-generated information must not become authoritative without appropriate verification and governance.

---

# 5. Roadmap Status Model

| Symbol | Meaning                            |
| ------ | ---------------------------------- |
| ✅     | Complete and verified              |
| 🟢     | Current / actively being worked on |
| 🟡     | Next planned milestone             |
| ⬜     | Planned                            |
| 🔭     | Long-term                          |
| ⛔     | Blocked                            |
| ❌     | Cancelled / removed                |

A milestone is complete only after:

```text
Architecture
    ↓
  Draft
    ↓
  Review
    ↓
 Approval
    ↓
Final Artifact
    ↓
 Git Verification
    ↓
 Commit
    ↓
 Release Tag
    ↓
 Push
    ↓
 Clean Working Tree
```

---

# 6. PHASE 1 — FOUNDATION

**Objective:** Build the organizational, documentation, engineering, AI, and knowledge foundations before serious product engineering.

---

# S1-01 — Repository Foundation

**Status:** ✅ COMPLETE

## Objective

Establish the Git repository and foundational documentation environment.

## Completed

- ASM Brain repository initialized
- Git/GitHub foundation
- Documentation structure
- Documentation Standard
- Initial navigation
- AI collaboration foundation
- Repository baseline

## Release

`S1-01`

**S1-01: COMPLETE**

---

# S1-02 — ASM Brain Foundation

**Status:** ✅ COMPLETE

## Objective

Establish ASM Brain as the institutional knowledge and documentation environment.

## Completed

- Obsidian structure
- Dashboard
- Manifesto
- Vision
- Mission
- Navigation
- Documentation framework
- ADR-001
- AI Working Protocol
- AI Collaboration Guidelines

## Release

`S1-02-foundation-v1.0`

**S1-02: COMPLETE**

---

# S1-03 — Organization Foundation

**Status:** ✅ COMPLETE

## Objective

Define the organizational, operational, engineering, and AI workforce foundations of Amar Smart Doctor.

## Company Foundation

Completed:

- Vision
- Mission
- Manifesto
- EOS v1.0
- ASDOM v1.0
- Strategic Principles v1.0
- Project Charter v1.0

## Engineering Foundation

Completed:

- Engineering Operating System
- Development Workflow
- Git Workflow
- Repository Strategy
- ADR-002
- Tool Responsibility Matrix
- AI Governance

## AI Organization

Completed:

- Organization Responsibility Matrix
- AI Workforce direction
- Human + AI workforce concept
- Future specialized AI roles

Future specialized roles include:

- Medical Reviewer AI
- SEO AI
- Content AI
- Translation AI
- Analytics AI
- Research AI
- Other specialized roles as justified

All AI roles remain subject to appropriate human governance and review gates.

## Release

`S1-03-company-foundation-v1.0`

**S1-03: COMPLETE**

---

# S1-04 — Knowledge Foundation

**Status:** ✅ COMPLETE

## Objective

Define the governed knowledge system that becomes the foundation of every future Amar Smart Doctor product.

The current Knowledge Foundation consists of six governed standards:

```text
KAS
KEF
MTS
ES
KLS
KDRS
```

These six standards collectively define:

- what knowledge is
- how knowledge is engineered
- how medical knowledge is classified
- how evidence is governed
- how knowledge evolves
- how knowledge relationships and dependencies are governed

## Important Architectural Note

The standards are interconnected and operate as a governed Knowledge System.

The sequence in this roadmap represents the documentation and execution sequence. It must not be interpreted as a strict technical dependency graph.

---

# S1-04.1 — Knowledge Asset Standard

**Status:** ✅ COMPLETE

**Release:** `S1-04.1-KAS-v1.0`

## Purpose

Define what a Knowledge Asset is.

The standard establishes the governed identity, structure, metadata, content, evidence, relationships, lifecycle, review, and traceability requirements for Knowledge Assets.

---

# S1-04.2 — Knowledge Engineering Framework

**Status:** ✅ COMPLETE

**Release:** `S1-04.2-KEF-v1.0`

## Purpose

Define how governed Knowledge Assets are researched, constructed, reviewed, maintained, and improved.

Conceptual pipeline:

```text
Medical Evidence
      ↓
Evidence Intake
      ↓
   Validation
      ↓
Knowledge Extraction
      ↓
Knowledge Structuring
      ↓
 Medical Review
      ↓
    Approval
      ↓
Knowledge Asset
      ↓
   ASM Brain
      ↓
Product Generation
```

The framework also establishes AI + Human collaboration.

---

# S1-04.3 — Medical Taxonomy Standard

**Status:** ✅ COMPLETE

**Release:** `S1-04.3-MTS-v1.0`

## Purpose

Define how medical knowledge is classified, organized, and semantically connected.

The taxonomy establishes the conceptual foundation for future medical knowledge graph capabilities.

Example conceptual structure:

```text
Disease
 ├── Symptoms
 ├── Causes
 ├── Risk Factors
 ├── Diagnosis
 ├── Treatment
 ├── Medicines
 ├── Procedures
 └── Related Conditions
```

---

# S1-04.4 — Evidence Standard

**Status:** ✅ COMPLETE

**Release:** `S1-04.4-ES-v1.0`

## Purpose

Define how evidence supporting governed medical knowledge is identified, assessed, represented, verified, synthesized, and maintained.

Core areas include:

- evidence hierarchy
- source credibility
- citation requirements
- verification
- evidence body
- evidence synthesis
- evidence relationships
- confidence
- evidence governance

---

# S1-04.5 — Knowledge Lifecycle Standard

**Status:** ✅ COMPLETE

**Release:** `S1-04.5-KLS-v1.0`

## Purpose

Define how Knowledge Assets live and evolve over time.

Conceptual lifecycle:

```text
Draft
  ↓
Review
  ↓
Approved
  ↓
Published
  ↓
Monitoring
  ↓
Update
  ↓
Re-review
  ↓
Archive
```

The lifecycle establishes controlled knowledge evolution rather than uncontrolled document editing.

---

# S1-04.6 — Knowledge Dependency & Relationship Standard

**Status:** ✅ COMPLETE

**Release:** `S1-04.6-KDRS-v1.0`

## Purpose

Define how relationships and dependencies between Knowledge Assets, evidence, medical concepts, and other governed knowledge objects are represented.

KDRS establishes:

- relationship identity
- relationship identifiers
- relationship categories
- relationship types
- relationship assertions
- relationship governance
- authority boundaries
- inferred relationship boundaries
- dependency impact
- historical relationship preservation
- relationship inclusion principles
- controlled relationship category extension

KDRS provides the foundation for future knowledge graph and dependency analysis capabilities.

---

# S1-04.7 — Knowledge Foundation Integration Review

**Status:** ✅ COMPLETE

## Objective

Review the six Knowledge System standards as one integrated architecture.

This is not another standard.

It is a cross-standard architecture review.

## Standards Reviewed

- KAS v1.0
- KEF v1.0
- MTS v1.0
- ES v1.0
- KLS v1.0
- KDRS v1.0

## Review Areas

### 1. Terminology Consistency

- Knowledge Asset
- evidence
- medical concept
- relationship
- version
- lifecycle state
- authority
- governance
- review
- publication

### 2. Authority Boundaries

Verify that no standard unintentionally transfers authority to another standard or to AI.

### 3. Dependency Consistency

Verify that the standards form a coherent dependency structure.

### 4. Evidence Integration

Verify that ES requirements are correctly consumed by KAS, KEF, and KLS.

### 5. Taxonomy Integration

Verify that MTS integrates correctly with KAS, KEF, and KDRS.

### 6. Lifecycle Integration

Verify that KLS correctly governs changes to assets, evidence, relationships, and derived outputs.

### 7. Relationship Integration

Verify that KDRS correctly governs relationships defined or referenced by the other standards.

### 8. Versioning Integration

Versioning responsibilities are distributed across KAS, KLS, and KDRS.

There is intentionally no separate Knowledge Versioning document at this stage.

### 9. Implementation Readiness

Determine whether an engineer can implement the Knowledge System without inventing missing governance rules.

### 10. Foundation Completeness

Determine whether S1-04 is ready to close.

## Result

**S1-04.7 completed and approved.**

The integrated Knowledge Foundation is the verified architectural baseline for Phase 2.

---

# S1-04 EXIT CRITERIA

All S1-04 foundation standards and the integration review have been completed and approved.

Completed:

- KAS v1.0 approved and released
- KEF v1.0 approved and released
- MTS v1.0 approved and released
- ES v1.0 approved and released
- KLS v1.0 approved and released
- KDRS v1.0 approved and released
- cross-standard consistency review completed
- authority boundaries reviewed
- implementation boundaries reviewed
- integrated Knowledge Foundation approved
- S1-04 formally closed

**S1-04: COMPLETE**

---

# 7. PHASE 2 — PLATFORM ENGINEERING

**Status:** 🟢 CURRENT

## Objective

Translate the governed Knowledge Foundation and approved Product & Business Architecture into the technical platform architecture and implementation foundation required for Amar Smart Doctor.

Phase 2 begins with product and business architecture before proceeding into technical platform architecture.

The sequence is:

```text
S1-04 Knowledge Foundation
      ↓
P2-00 Product & Business Architecture
      ↓
P2-01 Knowledge Platform Architecture
      ↓
Platform Engineering
```

The Knowledge Foundation defines how governed medical knowledge works.

P2-00 defines the product, business, portfolio, and commercial architecture that the platform must support.

P2-01 translates those approved architectural requirements into the technical Knowledge Platform Architecture.

---

# P2-00 — Product & Business Architecture

**Status:** COMPLETE

## Objective

Define the product and business architecture required to translate the Amar Smart Doctor vision and Knowledge Foundation into an executable Phase 1 product and commercial structure.

## Completed Deliverables

### P2-00.1 — Product & Business Architecture

**Status:** COMPLETE

Defines:

- product architecture
- product boundaries
- SEO-first product direction
- Knowledge Engine relationship
- Search Engine Strategy
- Discovery Engine
- Appointment Product
- Canonical Healthcare Identity principle
- user value journey
- Phase 1 product architecture

### P2-00.2 — Phase 1 Product Portfolio & Commercial Architecture

**Status:** COMPLETE

Defines:

- Phase 1 product portfolio
- product boundaries
- commercial architecture
- relationship between platform capabilities and products
- Phase 1 commercial direction
- product sequencing

## Architectural Role

P2-00 provides the approved product and business architecture inputs required by P2-01.

P2-00 does not replace the Knowledge Foundation or the technical platform architecture.

The relationship is:

```text
S1-04
Knowledge Foundation
      ↓
P2-00
Product & Business Architecture
      ↓
P2-01
Knowledge Platform Architecture
```

**P2-00: COMPLETE**

---

# P2-01 — Knowledge Platform Architecture

**Status:** ✅ COMPLETE

## Objective

Define the technical architecture of the Amar Smart Doctor Knowledge Platform.

P2-01 must translate the approved Product & Business Architecture and the S1-04 Knowledge Foundation into a coherent technical platform architecture.

## Principal Architectural Inputs

- S1-04 Knowledge Foundation
- P2-00 Product & Business Architecture
- P2-00.1 Product & Business Architecture
- P2-00.2 Phase 1 Product Portfolio & Commercial Architecture

## Define

- core platform architecture
- system boundaries
- knowledge data model
- knowledge storage
- knowledge relationships
- evidence integration
- versioning architecture
- API architecture
- authentication
- authorization
- governance boundaries
- integration boundaries
- product/platform boundaries
- technical interfaces between platform capabilities and Phase 1 products

## Architectural Constraint

P2-01 must implement the governance established by the Knowledge Foundation.

It must not redefine, bypass, or silently weaken the authority boundaries established by S1-04.

## Deliverable

Approved Knowledge Platform Architecture specification.

## Completion Gate

P2-01 must satisfy its architecture review and approval criteria before implementation of the Knowledge Data Layer begins.

**P2-01: NEXT**

---

# P2-02 — Knowledge Data Layer

**Status:** 🟡 NEXT

Build:

- Knowledge Asset storage
- medical concepts
- taxonomy relationships
- knowledge relationships
- evidence references
- lifecycle states
- versions
- review states
- metadata
- dependency structures

The implementation must follow the six Knowledge System standards and the approved P2-01 architecture.

---

# P2-03 — Knowledge API

**Status:** ⬜ PLANNED

Create the governed programmatic interface through which:

- Website
- AI Agents
- Mobile Applications
- Internal Tools
- Future Products

can access approved knowledge.

The API must not bypass Knowledge System governance.

Implementation must follow the approved P2-01 architecture and Knowledge System standards.

---

# P2-04 — AI Workforce Infrastructure

**Status:** ⬜ PLANNED

Operationalize the future AI workforce.

Potential roles include:

```text
Research AI
      ↓
Curation AI
      ↓
Knowledge Engineering AI
      ↓
Medical Reviewer AI
      ↓
Content AI
      ↓
Translation AI
      ↓
SEO AI
      ↓
Publishing AI
      ↓
Analytics AI
```

The objective is not:

> "AI writes articles."

The objective is:

> **A coordinated AI workforce operates the knowledge production pipeline under human governance.**

Human review gates remain mandatory where required by risk and governance.

---

# P2-05 — Search & Retrieval

**Status:** ⬜ PLANNED

Build the system capable of retrieving governed knowledge reliably.

Potential capabilities:

- structured search
- semantic search
- knowledge graph retrieval
- ranking
- filtering
- multilingual retrieval
- retrieval governance
- source/evidence awareness

Technology choices will be made from requirements rather than trend.

---

# 8. PHASE 3 — MVP PUBLIC PRODUCT

**Status:** ⬜ FUTURE

## Objective

Launch the first public Amar Smart Doctor product using the Knowledge Platform.

The website is the first consumer of the platform.

It is not the platform itself.

---

# P3-01 — Public Website

Build:

- AmarSmartDoctor.com
- responsive experience
- core navigation
- medical knowledge pages
- specialty discovery
- disease/topic discovery
- doctor discovery
- Bangla experience
- English experience

---

# P3-02 — Public Search

Provide:

- medical search
- disease/topic search
- specialty search
- doctor discovery
- structured filtering
- governed knowledge retrieval

---

# P3-03 — Knowledge Experience

Create public experiences for governed Knowledge Assets.

The public layer should consume approved knowledge rather than independently authoring medical truth.

---

# P3-04 — SEO Architecture

Implement:

- technical SEO
- structured data
- indexation architecture
- internal linking
- topic/specialty architecture
- metadata
- canonicalization
- multilingual SEO
- scalable page generation

SEO must remain downstream of governed knowledge.

---

# P3-05 — Analytics

Implement appropriate:

- product analytics
- search analytics
- content analytics
- SEO analytics
- conversion measurement
- privacy-aware tracking

---

# P3-06 — Editorial / Admin Interface

Provide controlled internal workflows for:

- knowledge review
- content publishing
- asset monitoring
- corrections
- lifecycle operations
- governance visibility

---

# PUBLIC MVP DEFINITION

The public MVP should prioritize:

- trust
- medical accuracy
- excellent structured knowledge
- useful search
- strong SEO foundations
- high-quality user experience

The MVP does not require:

- full AI workforce automation
- mobile application
- hospital management platform
- doctor management platform
- complete knowledge graph
- every medical specialty
- massive Knowledge Asset volume

The MVP should launch with **quality over quantity**.

A smaller set of excellent, governed Knowledge Assets is preferable to thousands of thin or weak AI-generated pages.

---

# PUBLIC MVP TARGET

**Planning target:** October–November 2026

This is a strategic planning target, not a fixed promise.

The target must not override:

- medical quality
- governance
- security
- technical readiness
- performance
- QA
- launch acceptance criteria

If those criteria are not satisfied, the launch moves rather than quality standards being reduced.

> **The calendar serves the product. The product does not serve the calendar.**

---

# 9. PHASE 4 — AI-NATIVE CONTENT & KNOWLEDGE OPERATIONS

**Status:** ⬜ FUTURE

Once the Knowledge Platform and MVP experience are operational, begin automating knowledge operations.

Potential pipeline:

```text
Research
   ↓
Evidence Collection
   ↓
Curation
   ↓
Knowledge Extraction
   ↓
Knowledge Asset Creation
   ↓
Medical Review
   ↓
Approval
   ↓
Content Generation
   ↓
Translation
   ↓
SEO Optimization
   ↓
Publishing
   ↓
Analytics
   ↓
Knowledge Improvement
```

The goal is controlled automation, not uncontrolled content generation.

---

# 10. PHASE 5 — SCALE & ECOSYSTEM

**Status:** 🔭 LONG-TERM

Once the core platform proves itself, potential products include:

- Website
- Mobile App
- API
- AI Health Assistant
- Doctor Platform
- Hospital Platform
- Medical Education
- Research Platform
- Doctor Appointment Platform
- Enterprise Knowledge API
- future medical-related solutions

These should be developed only when justified by:

- user demand
- strategic value
- platform maturity
- operational capacity
- governance readiness

---

# 11. PHASE 6 — GLOBAL PLATFORM

**Status:** 🔭 LONG-TERM VISION

The architecture should eventually support:

- multiple languages
- multiple countries
- multiple medical systems
- international evidence sources
- regional medical governance
- global knowledge distribution

We design for scalability without prematurely implementing global complexity.

---

# 12. Current Git Release Baseline

Verified released baseline:

- `S1-02-foundation-v1.0`
- `S1-03-company-foundation-v1.0`
- `S1-04.1-KAS-v1.0`
- `S1-04.2-KEF-v1.0`
- `S1-04.3-MTS-v1.0`
- `S1-04.4-ES-v1.0`
- `S1-04.5-KLS-v1.0`
- `S1-04.6-KDRS-v1.0`
- `S1-04-Knowledge-Foundation-v1.0`
- `P2-01-knowledge-platform-architecture-v1.0`

The S1-04 Knowledge Foundation aggregate release is:

`S1-04-Knowledge-Foundation-v1.0`

This aggregate release represents the completed S1-04 Knowledge Foundation, including:

- KAS v1.0
- KEF v1.0
- MTS v1.0
- ES v1.0
- KLS v1.0
- KDRS v1.0
- S1-04.7 Knowledge Foundation Integration Review

The S1-04.7 integration review does not require a separate Git tag.

The aggregate S1-04 release is the verified Git release checkpoint for the completed Knowledge Foundation.

The completed P2-01 Knowledge Platform Architecture release is:

`P2-01-knowledge-platform-architecture-v1.0`

This release includes:

- `P2-01 Knowledge Platform Architecture.md`
- `P2-01.0 Architecture Brief & Scope.md`
- `P2-01.1 System Context & Platform Boundary.md`

The P2-01 release is the verified Git release checkpoint for the completed Knowledge Platform Architecture milestone.

The repository is currently synchronized with `origin/main` and the working tree is clean.

---

# 13. Current Project State

**Current phase:**

`PHASE 2 — PLATFORM ENGINEERING`

**Completed milestones:**

- `P2-00 — Product & Business Architecture`
- `P2-01 — Knowledge Platform Architecture`

**Completed P2-00 deliverables:**

- `P2-00.1 — Product & Business Architecture`
- `P2-00.2 — Phase 1 Product Portfolio & Commercial Architecture`

**Completed P2-01 deliverables:**

- `P2-01.0 — Architecture Brief & Scope`
- `P2-01.1 — System Context & Platform Boundary`
- `P2-01 — Knowledge Platform Architecture`

**Next milestone:**

`P2-02 — Knowledge Data Layer`

**Status:** 🟡 NEXT

P2-01 Knowledge Platform Architecture has been completed and released.

The approved P2-01 architecture and the S1-04 Knowledge Foundation are the principal architectural inputs for P2-02.

P2-02 must establish the detailed Knowledge Data Layer architecture and specification before implementation begins.

The project must not proceed to uncontrolled Knowledge Data Layer implementation before the P2-02 architecture and specification have been completed, reviewed, and approved.

---

# 14. Knowledge System Current State

The following documents exist under:

```text
35. Knowledge System/
```

- Evidence Standard.md
- Knowledge Asset Standard.md
- Knowledge Dependency & Relationship Standard.md
- Knowledge Engineering Framework.md
- Knowledge Lifecycle Standard.md
- Medical Taxonomy.md

Current released standards:

- KAS v1.0
- KEF v1.0
- MTS v1.0
- ES v1.0
- KLS v1.0
- KDRS v1.0

All six standards are individually released.

The integrated Knowledge Foundation has been reviewed and approved.

**S1-04: COMPLETE**

---

# 15. Current Position

```text
AMAR SMART DOCTOR
│
├── PHASE 1 — FOUNDATION
│   │
│   ├── S1-01 Repository Foundation       ✅
│   ├── S1-02 ASM Brain Foundation        ✅
│   ├── S1-03 Organization Foundation     ✅
│   └── S1-04 Knowledge Foundation         ✅
│       │
│       ├── KAS v1.0                      ✅
│       ├── KEF v1.0                      ✅
│       ├── MTS v1.0                      ✅
│       ├── ES v1.0                       ✅
│       ├── KLS v1.0                      ✅
│       ├── KDRS v1.0                     ✅
│       └── Integration Review            ✅
│
├── PHASE 2 — PLATFORM ENGINEERING        🟢
│   │
│   ├── P2-00 Product & Business Architecture ✅
│   │   ├── P2-00.1 Product & Business Architecture ✅
│   │   └── P2-00.2 Phase 1 Product Portfolio & Commercial Architecture ✅
│   │
│   ├── P2-01 Knowledge Platform Architecture ✅
│   │   ├── P2-01.0 Architecture Brief & Scope ✅
│   │   ├── P2-01.1 System Context & Platform Boundary ✅
│   │   └── P2-01 Architecture Specification ✅
│   │
│   ├── P2-02 Knowledge Data Layer         🟡 NEXT
│   ├── P2-03 Knowledge API                ⬜
│   ├── P2-04 AI Workforce Infrastructure ⬜
│   └── P2-05 Search & Retrieval           ⬜
│
├── PHASE 3 — MVP PUBLIC PRODUCT           ⬜
│   │
│   ├── Public Website
│   ├── Search
│   ├── Knowledge Experience
│   ├── SEO Architecture
│   ├── Analytics
│   └── Editorial/Admin
│
├── PHASE 4 — AI KNOWLEDGE OPERATIONS      ⬜
│   │
│   ├── Research
│   ├── Curation
│   ├── Knowledge Engineering
│   ├── Medical Review
│   ├── Content
│   ├── Translation
│   ├── SEO
│   ├── Publishing
│   └── Analytics
│
├── PHASE 5 — SCALE & ECOSYSTEM            🔭
│   │
│   ├── Mobile
│   ├── Doctor Platform
│   ├── Hospital Platform
│   ├── Education
│   ├── Research
│   └── Enterprise API
│
└── PHASE 6 — GLOBAL PLATFORM              🔭
    │
    ├── Multilingual
    ├── Multi-country
    ├── Regional Governance
    └── Global Knowledge Platform
```

---

# 16. Immediate Next Action

The next project milestone is:

> **P2-02 — Knowledge Data Layer**

P2-01 Knowledge Platform Architecture has been completed, reviewed, committed, tagged, and pushed.

P2-02 will translate the approved P2-01 architecture and the S1-04 Knowledge Foundation into the detailed architecture, specification, and implementation foundation for the Knowledge Data Layer.

P2-02 is a platform engineering milestone.

The project must not begin uncontrolled data-layer implementation before the P2-02 architecture and specification have been properly defined, reviewed, and approved.

The execution sequence is:

```text
P2-01 Knowledge Platform Architecture
      ↓
P2-01 Release
      ↓
P2-02 Knowledge Data Layer
      ↓
P2-02 Data Architecture / Specification
      ↓
Architecture Review
      ↓
Approval
      ↓
Implementation
      ↓
Verification
      ↓
Release
```

---

# 17. Roadmap Execution Rule

Only the currently active milestone is considered implementation scope.

Future milestones are planning references only.

The existence of a future item in this roadmap does not authorize its implementation before its scheduled milestone.

For example, while P2-02 is active:

**CURRENT**

`P2-02 Knowledge Data Layer`

The following remain **NOT NOW**:

- Knowledge API implementation
- AI Workforce implementation
- Search & Retrieval implementation
- Knowledge Graph implementation beyond the approved P2-02 scope
- Public Website implementation
- Mobile Application
- Doctor Platform
- Hospital Platform
- Future product implementation

This rule exists to prevent scope creep and premature implementation.

P2-02 must remain focused on establishing the governed Knowledge Data Layer according to the approved P2-01 architecture and the S1-04 Knowledge Foundation.

---

# 18. Decision Discipline

### Rule 1 — Do not invent milestones casually

New milestones must have a documented reason.

### Rule 2 — Do not duplicate governance

If an existing standard already governs a concern, do not create another document merely because the topic has a new name.

### Rule 3 — Prefer integration over document proliferation

A mature system is not measured by the number of Markdown files.

### Rule 4 — Complete before expanding

A milestone must satisfy its acceptance criteria and release requirements before the next major milestone begins.

For the current P2-02 milestone, architecture and specification must be reviewed and approved before implementation begins.

### Rule 5 — MVP scope is controlled

Long-term architecture must not become an excuse to delay the public MVP indefinitely.

### Rule 6 — Quality over quantity

Medical knowledge quality and governance take priority over content volume.

### Rule 7 — AI remains subordinate to governance

AI can accelerate knowledge work but cannot silently become the source of truth.

### Rule 8 — The roadmap is updated after meaningful milestone changes

When a milestone is completed, the roadmap must be updated before or alongside the release checkpoint.

---

# 19. Roadmap Change Control

Changes to the roadmap should be deliberate.

A roadmap change should document:

- what changed
- why it changed
- what existing milestone is affected
- whether scope increased or decreased
- whether dependencies changed
- whether the public MVP target is affected

Significant roadmap changes should be recorded in the project Decision Log.

---

# 20. Change History

| Version | Date       | Change                                                                                                                                                                                                                                                                                                                                                                                  | Status     |
| ------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| 1.0     | 2026-08-08 | Formalized the Master Roadmap as the controlling project roadmap; incorporated S1-04 progress; added KDRS; replaced standalone Knowledge Versioning milestone with cross-cutting version governance; established S1-04.7 integration review; documented Phase 2–6 roadmap and MVP target                                                                                                | Superseded |
| 1.1     | 2026-08-08 | Closed S1-04 and S1-04.7 in the roadmap; removed obsolete “Integration Review — NEXT” state; corrected current position; advanced roadmap to Phase 2 / P2-01; documented the remaining S1-04 Git release-checkpoint requirement                                                                                                                                                         | Superseded |
| 1.2     | 2026-08-12 | Reconciled the roadmap with the completed S1-04 aggregate release and completed P2-00 Product & Business Architecture; incorporated P2-00.1 and P2-00.2; clarified the P2-00 → P2-01 architectural relationship; updated the Phase 2 sequence, current project state, Git release baseline, immediate next action, and removed the obsolete separate S1-04.7 Git checkpoint requirement | Superseded |
| 1.3     | 2026-08-15 | Reconciled the Master Roadmap with the completed and released P2-01 Knowledge Platform Architecture; advanced P2-01 to complete, advanced P2-02 to next, updated the current project state, current position, immediate next action, roadmap execution scope, and Git release baseline.                                                                                                 | Active     |

---

# 21. Final Principle

Amar Smart Doctor should be built progressively.

We do not build everything before launching.

We do not launch before the foundation is trustworthy.

We do not allow the website to become the source of truth.

We do not allow AI to become the source of truth.

We build:

```text
Governed Knowledge
      ↓
Reliable Platform
      ↓
Useful Products
      ↓
AI-Native Operations
      ↓
    Scale
```

The objective is not to build the largest system first.

The objective is to build the **right system in the right order**.

---

# End of Document