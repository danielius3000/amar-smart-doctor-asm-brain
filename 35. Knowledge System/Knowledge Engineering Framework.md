# Knowledge Engineering Framework (KEF)

> **Document Status:** Approved  
> **Version:** 1.0 
> **Owner:** Amar Smart Doctor  
> **System:** ASM Brain — Knowledge System  
> **Document Type:** Knowledge System Framework

---

## 1. Purpose

The Amar Smart Doctor Knowledge Engineering Framework (KEF) defines the controlled process through which evidence and research are transformed into governed, reusable Knowledge Assets.

The purpose of KEF is to establish a repeatable knowledge production system that can support:

- human knowledge workers
- medical reviewers
- AI-assisted research
- knowledge engineers
- future AI agents
- structured knowledge production
- continuous knowledge improvement

KEF exists to ensure that knowledge is not created as isolated content.

Instead, knowledge should move through a controlled engineering process:

**Evidence → Knowledge Engineering → Knowledge Asset**

The resulting Knowledge Asset can then serve as the source for multiple products and experiences.

---

## 2. Scope

KEF governs the process of:

- defining a Knowledge Engineering Objective
- receiving evidence and research inputs
- assessing source suitability
- extracting relevant information
- identifying knowledge claims
- structuring knowledge
- synthesizing information across sources
- handling contradictory evidence
- preserving appropriate uncertainty
- performing human review
- obtaining required medical approval
- creating Knowledge Assets according to KAS
- maintaining provenance and traceability
- handing approved assets into the Knowledge Lifecycle

KEF does not define:

- what a Knowledge Asset is
- the complete medical taxonomy
- the evidence hierarchy
- long-term asset maintenance
- website publishing
- SEO implementation
- database architecture
- API architecture
- AI model architecture

Those responsibilities belong to other components of the Amar Smart Doctor architecture.

---

## 3. Relationship to the Knowledge System

KEF is one component of the broader Amar Smart Doctor Knowledge System.

The major responsibilities are separated as follows:

### Knowledge Asset Standard (KAS)

Defines:

> **What is a Knowledge Asset?**

### Knowledge Engineering Framework (KEF)

Defines:

> **How is a Knowledge Asset created or substantially revised?**

### Medical Taxonomy

Defines:

> **How is knowledge classified and organized?**

### Evidence Standard

Defines:

> **How is evidence evaluated and trusted?**

### Knowledge Lifecycle

Defines:

> **How is a Knowledge Asset maintained over time?**

Together, these components form the foundation of the Knowledge System.

---

## 4. Core Principle

The central principle of KEF is:

> **Transform evidence into governed, reusable Knowledge Assets through a controlled, traceable, human-supervised engineering process.**

KEF is therefore a knowledge production framework rather than a conventional content production workflow.

---

## 5. Knowledge Engineering Objective

Every Knowledge Engineering effort should begin with a clearly defined objective.

The Knowledge Engineering Objective establishes:

- what knowledge is being created or revised
- the intended Knowledge Asset
- the scope of the engineering effort
- the intended knowledge boundaries
- the reason the work is being performed
- the expected outcome

The objective prevents uncontrolled research and unnecessary knowledge expansion.

The conceptual relationship is:

**Knowledge Engineering Objective → Evidence Requirements → Knowledge Engineering → Knowledge Asset**

For example:

> **Objective:** Create a governed Knowledge Asset for Polycystic Ovary Syndrome (PCOS).

The objective defines the target.

It does not itself define the final Knowledge Asset structure. That responsibility remains with KAS.

---

## 6. Knowledge Engineering Pipeline

The canonical KEF pipeline is:

**Knowledge Engineering Objective → Evidence Intake → Assessment → Extraction → Structuring → Synthesis → Review → Approval → Asset Creation → Lifecycle Handoff**

The pipeline supports both:

- creation of new Knowledge Assets
- substantive revision of existing Knowledge Assets

The process must support rejection, revision, and uncertainty.

Information must not automatically progress to Knowledge Asset creation merely because it has entered the system.

---

## 7. Process Stages

KEF process stages describe the activities performed during knowledge engineering.

The major stages are:

1. Knowledge Engineering Objective
2. Evidence Intake
3. Evidence and Source Assessment
4. Knowledge Extraction
5. Knowledge Structuring
6. Knowledge Synthesis
7. Human Review
8. Approval
9. Knowledge Asset Creation
10. Lifecycle Handoff

These are **process stages**, not automatically quality gates.

A process stage describes:

> **What work is performed?**

A quality gate describes:

> **Is the result acceptable to proceed?**

This distinction is important because not every activity requires a separate governance gate.

---

## 8. Evidence Intake

Evidence and research materials enter the Knowledge Engineering process.

Potential inputs may include:

- clinical guidelines
- systematic reviews
- peer-reviewed research
- authoritative medical organizations
- government health sources
- recognized medical reference materials
- approved internal knowledge
- existing Knowledge Assets requiring substantive revision

Each input should retain sufficient provenance to identify its origin.

The detailed source hierarchy and credibility requirements belong to the Evidence Standard.

---

## 9. Evidence and Source Assessment

Evidence entering the system should be assessed before it is used to create knowledge.

Assessment may consider:

- source authority
- relevance
- recency
- methodological quality
- applicability
- consistency with other evidence
- known limitations

Two related but distinct questions should be preserved:

### Source Assessment

> **Is this source suitable and trustworthy enough to use?**

### Evidence Assessment

> **Does the evidence adequately support the knowledge claim or intended conclusion?**

These questions should not be treated as identical.

Evidence may be:

- accepted for further processing
- accepted with limitations
- placed on hold
- rejected

KEF defines the assessment process.

The detailed evidence-ranking rules belong to the Evidence Standard.

---

## 10. Knowledge Extraction

Relevant information is extracted from accepted evidence.

Extraction may include identifying:

- facts
- findings
- clinical claims
- definitions
- relationships
- recommendations
- limitations
- population-specific findings
- uncertainties

The objective is not simply to copy source text.

The objective is to identify the knowledge contained within the evidence that is relevant to the Knowledge Engineering Objective.

AI may assist with extraction, but extracted information must remain traceable to its source.

---

## 11. Evidence, Knowledge Claims, and Knowledge Assets

KEF distinguishes three important conceptual layers.

### Evidence

Evidence is information originating from an identified source.

Examples include:

- published research
- clinical guidelines
- systematic reviews
- authoritative reference materials

### Knowledge Claim

A Knowledge Claim is a specific proposition, finding, relationship, recommendation, or other meaningful statement derived from one or more evidence sources.

A Knowledge Claim should be traceable to its supporting evidence.

### Knowledge Asset

A Knowledge Asset is the governed, structured unit of knowledge defined by the Knowledge Asset Standard.

The conceptual relationship is:

**Evidence → Knowledge Claim → Synthesized Knowledge → Knowledge Asset**

A Knowledge Asset may contain or organize multiple Knowledge Claims.

A Knowledge Claim does not automatically become a Knowledge Asset.

---

## 12. Knowledge Structuring

Extracted information and Knowledge Claims are organized into a structured representation.

Structuring may include:

- identifying the knowledge concept
- defining boundaries
- assigning an asset type
- organizing knowledge fields
- identifying relationships
- associating evidence
- identifying missing information
- identifying uncertainty
- organizing relevant Knowledge Claims

The resulting structure should conform to the principles established by the Knowledge Asset Standard.

KEF does not redefine the KAS structure.

It applies it.

---

## 13. Knowledge Synthesis

Knowledge may need to be synthesized from multiple evidence sources.

Synthesis involves:

- comparing evidence
- comparing Knowledge Claims
- identifying agreement
- identifying disagreement
- resolving compatible findings
- preserving important differences
- identifying limitations
- determining appropriate wording
- maintaining traceability

Synthesis must not create unsupported conclusions.

Where evidence is insufficient, the resulting knowledge should preserve the appropriate level of uncertainty.

---

## 14. Contradictory Evidence

Medical evidence may contain disagreement.

KEF must explicitly support contradictory evidence.

When sources or Knowledge Claims disagree, the process should:

1. identify the contradiction
2. identify the claims involved
3. identify the supporting sources
4. assess source quality and authority
5. assess methodological differences
6. determine whether the findings can be reconciled
7. preserve meaningful disagreement when necessary
8. obtain appropriate human review
9. document the resulting decision

The system must not resolve contradictions simply by selecting the most convenient answer.

It must not manufacture consensus where the evidence does not support one.

---

## 15. Uncertainty

Medical knowledge frequently contains uncertainty.

Examples include:

- limited evidence
- emerging evidence
- conflicting findings
- population-specific results
- incomplete evidence
- changing clinical guidance

KEF must preserve meaningful uncertainty throughout the engineering process.

The system should avoid transforming:

- uncertain evidence into certainty
- limited evidence into strong claims
- association into causation
- preliminary findings into established medical guidance

The detailed evidence and confidence model will be defined in the Evidence Standard.

---

## 16. Human Review

Knowledge produced through KEF must undergo appropriate human review before receiving the required approval status.

Review may evaluate:

- factual accuracy
- evidence support
- completeness
- logical consistency
- clinical appropriateness
- wording
- uncertainty
- relationships
- safety
- intended audience

The required level of review may depend on the asset type and risk level.

KEF establishes the review requirement as part of the engineering process.

The detailed risk classification framework may be defined separately as the Knowledge System matures.

---

## 17. Medical Review

Medical knowledge intended for public or clinical-facing use may require qualified medical review according to the applicable governance rules.

The medical reviewer is responsible for evaluating whether the knowledge accurately represents the available evidence and is appropriate for the intended use.

AI-generated content does not constitute medical approval.

---

## 18. Approval

Approval is a governance decision.

Approval confirms that the Knowledge Asset has satisfied the applicable requirements for its intended status.

Approval should only occur after required:

- evidence assessment
- knowledge processing
- review
- quality checks
- medical review where required

have been completed.

Approval authority is defined by the organizational governance model.

---

## 19. Knowledge Asset Creation

Once the knowledge has passed the required quality and approval requirements, it can be represented as a Knowledge Asset according to the Knowledge Asset Standard.

The relationship is:

**KEF creates the Knowledge Asset.**

**KAS defines the Knowledge Asset.**

KEF must not create a structure that conflicts with KAS.

The resulting asset should include the applicable:

- identity
- knowledge
- evidence
- relationships
- governance information
- lifecycle information

defined by KAS.

---

## 20. Provenance and Traceability

Knowledge Engineering must preserve provenance.

The system should be able to establish:

> **Where did this knowledge come from?**

Where practical, significant Knowledge Claims should be traceable to the evidence supporting them.

A Knowledge Asset should therefore be capable of maintaining relationships such as:

**Knowledge Asset → Knowledge Claim → Evidence Source**

The engineering process should also preserve relevant production history, including:

- source inputs
- extraction
- synthesis
- review
- approval
- significant changes

The exact technical implementation of provenance will be defined during later engineering architecture.

---

## 21. Human and AI Responsibilities

KEF is designed to support both human and AI-assisted knowledge engineering.

AI may assist with:

- research
- source discovery
- extraction
- comparison
- classification
- structuring
- synthesis assistance
- contradiction detection
- quality checks
- drafting
- identifying missing information

AI must not automatically become the final authority for medically significant knowledge.

The governing principle is:

> **AI accelerates knowledge engineering; human governance establishes authority.**

---

## 22. Human-in-the-Loop Principle

Human involvement must be proportional to the risk and significance of the knowledge being produced.

The conceptual model is:

**AI Assistance → Human Review → Medical Approval Where Required → Governed Knowledge Asset**

AI may perform substantial work before human review.

However, automation must not bypass required governance controls.

---

## 23. Roles

KEF may involve the following roles.

### Knowledge Researcher

Responsible for gathering and organizing relevant research inputs.

### Knowledge Engineer

Responsible for transforming evidence into structured knowledge according to the Knowledge System standards.

### Medical Reviewer

Responsible for reviewing medically significant knowledge.

### Medical Approver

Responsible for granting approval where medical approval is required.

### Knowledge Owner

Responsible for ongoing ownership and accountability of the resulting Knowledge Asset.

### AI / Automated Systems

Responsible for approved assistance activities such as:

- research assistance
- extraction
- structuring
- comparison
- analysis
- quality support

AI systems do not automatically inherit human governance authority.

---

## 24. Quality Gates

Quality gates are decision points used to determine whether the result of a process stage is acceptable to proceed.

A quality gate should exist only where a meaningful decision is required.

The initial conceptual quality gates are:

### Gate 0 — Objective Validity

Confirm that the Knowledge Engineering Objective is sufficiently defined and has a legitimate target.

### Gate 1 — Source Suitability

Confirm that the evidence sources are suitable for the intended engineering objective.

### Gate 2 — Evidence Sufficiency

Determine whether the available evidence adequately supports continued engineering.

### Gate 3 — Knowledge Quality

Determine whether the extracted and structured Knowledge Claims are sufficiently accurate, relevant, and traceable.

### Gate 4 — Synthesis Quality

Determine whether synthesis has appropriately handled agreement, contradiction, limitation, and uncertainty.

### Gate 5 — Human Review

Confirm that required human review has been completed successfully.

### Gate 6 — Medical Approval

Confirm medical approval where required.

### Gate 7 — Asset Readiness

Confirm that the resulting knowledge satisfies the applicable KAS requirements and is ready to exist as a governed Knowledge Asset.

### Gate 8 — Lifecycle Handoff

Confirm that the completed asset and required supporting information can enter the Knowledge Lifecycle.

These gates are conceptual and may be refined as the Knowledge System matures.

---

## 25. Rejection, Revision, and Hold States

KEF must support situations in which knowledge cannot safely proceed.

At appropriate stages, information may be:

- rejected
- returned for additional research
- returned for revision
- placed on hold
- escalated for expert review

Examples include:

- insufficient evidence
- unreliable sources
- unresolved contradiction
- missing critical information
- unacceptable uncertainty
- failed review
- safety concerns

The existence of a failed gate should not be treated as a system failure.

Controlled rejection and revision are essential characteristics of a trustworthy knowledge system.

---

## 26. Knowledge Revision Engineering

KEF supports not only the creation of new Knowledge Assets but also the engineering of substantive changes to existing assets.

The conceptual process is:

**Existing Knowledge Asset → New Evidence → Impact Assessment → Knowledge Revision → Review → Approval → Updated Knowledge Asset**

The distinction between KEF and Knowledge Lifecycle is:

**Knowledge Lifecycle identifies and manages the need for change.**

**KEF performs the knowledge engineering required to implement the change.**

**KAS defines the resulting Knowledge Asset.**

---

## 27. Lifecycle Handoff

Once a Knowledge Asset has completed the required engineering and approval process, it is handed into the Knowledge Lifecycle.

The lifecycle becomes responsible for ongoing maintenance activities such as:

- monitoring
- review scheduling
- update requirements
- revalidation
- archival

KEF may be invoked again whenever substantive knowledge engineering is required.

Therefore the relationship is cyclical rather than one-directional.

**Knowledge Lifecycle → identifies change → KEF → engineers change → Knowledge Asset → Lifecycle**

---

## 28. Quality Principles

All KEF processes should prioritize:

### Accuracy

Knowledge should accurately represent the supporting evidence.

### Traceability

Significant Knowledge Claims should remain traceable to appropriate evidence.

### Consistency

Knowledge should use consistent terminology and structures.

### Completeness

Important information required for the intended asset should not be omitted without justification.

### Transparency

Important uncertainty, limitations, contradictions, and decisions should be visible to appropriate reviewers.

### Safety

The process must prioritize responsible medical communication.

### Reproducibility

Another qualified knowledge worker should be able to understand how the resulting knowledge was produced.

### Maintainability

The engineering process should support future revision rather than producing static content that is difficult to update.

---

## 29. Knowledge Engineering Is Not Content Production

KEF produces structured knowledge, not finished marketing content.

The output may later be transformed into:

- website pages
- SEO content
- FAQs
- social media content
- video scripts
- educational materials
- AI responses
- future product experiences

These outputs belong to downstream product and content systems.

The conceptual relationship is:

**Evidence → KEF → Knowledge Asset → Product / Content / AI Output**

This separation protects the Knowledge Layer from becoming dependent on a particular presentation format.

---

## 30. Technology Independence

KEF is a logical and operational framework.

It does not prescribe a specific:

- database
- programming language
- API
- search engine
- knowledge graph technology
- AI model
- workflow automation platform
- CMS
- frontend framework

Technical implementation must preserve the principles and governance requirements defined by KEF.

Technology decisions will be made during later engineering architecture.

---

## 31. Extensibility

KEF should support the future expansion of Amar Smart Doctor.

The framework may eventually support:

- additional medical domains
- additional Knowledge Asset types
- multilingual knowledge engineering
- automated quality systems
- advanced AI agents
- knowledge graphs
- large-scale evidence processing
- continuous evidence monitoring

However, new capabilities should be introduced through controlled architectural decisions.

The framework should favor simplicity and maintainability over premature complexity.

---

## 32. KEF Outputs

The primary output of the Knowledge Engineering Framework is a governed Knowledge Asset.

Supporting outputs may include:

- evidence references
- provenance information
- structured Knowledge Claims
- review records
- approval records
- change rationale
- identified limitations
- unresolved issues
- engineering metadata

These supporting records improve auditability and future maintenance.

---

## 33. KEF and the ASM Brain

KEF operates within ASM Brain as a core Knowledge System standard.

The Knowledge System should serve as the organizational framework through which Amar Smart Doctor's knowledge can be consistently produced and governed.

The intended hierarchy is:

**ASM Brain**

→ **Knowledge System**

→ **Knowledge Asset Standard**

→ **Knowledge Engineering Framework**

→ **Medical Taxonomy**

→ **Evidence Standard**

→ **Knowledge Lifecycle**

The exact repository structure and technical implementation may evolve while preserving these conceptual responsibilities.

---

## 34. Future Automation

Future Amar Smart Doctor systems may automate portions of the KEF process.

Potential automation areas include:

- evidence discovery
- source classification
- evidence extraction
- duplicate detection
- contradiction detection
- Knowledge Claim extraction
- knowledge structuring
- completeness checking
- terminology normalization
- citation validation
- change detection

Automation must remain subordinate to the governance model.

The objective is not maximum automation.

The objective is:

> **Reliable knowledge production with appropriate human oversight.**

---

## 35. Safety Principle

Healthcare knowledge carries a higher responsibility than ordinary informational content.

Therefore:

> **When accuracy, evidence, or safety is uncertain, the system must favor controlled review over automated publication.**

The Knowledge Engineering Framework must never be optimized solely for:

- speed
- volume
- SEO output
- AI throughput
- publishing frequency

Trustworthiness takes priority.

---

## 36. Acceptance Criteria

KEF v1.0 may be approved when:

- [ ] Purpose and scope are clearly defined
- [ ] KEF's relationship with KAS is clearly defined
- [ ] KEF boundaries are clearly defined
- [ ] The Knowledge Engineering Objective is defined
- [ ] The canonical knowledge engineering pipeline is established
- [ ] Process stages are clearly distinguished from quality gates
- [ ] Evidence intake is defined
- [ ] Source assessment responsibilities are defined
- [ ] Evidence assessment responsibilities are defined
- [ ] Knowledge Extraction is defined
- [ ] Knowledge Claims are conceptually defined
- [ ] Knowledge Structuring is defined
- [ ] Knowledge Synthesis is defined
- [ ] Contradictory evidence handling is defined
- [ ] Uncertainty handling is defined
- [ ] Human review is defined
- [ ] Medical approval is defined
- [ ] AI responsibilities are defined
- [ ] Human governance authority is preserved
- [ ] Provenance and traceability principles are defined
- [ ] Quality gates are defined
- [ ] Rejection and revision mechanisms are defined
- [ ] Revision engineering is defined
- [ ] Lifecycle handoff is defined
- [ ] KEF is clearly separated from content production
- [ ] Technology independence is preserved
- [ ] Extensibility principles are defined
- [ ] Safety principles are established
- [ ] The document has been reviewed against the broader ASM Brain architecture

---

## 37. Document Control

| Field            | Value                                           |
| ---------------- | ----------------------------------------------- |
| Document         | Knowledge Engineering Framework                 |
| Short Name       | KEF                                             |
| Version          | 1.0                                             |
| Status           | Approved                                        |
| Owner            | Amar Smart Doctor                               |
| System           | ASM Brain                                       |
| Domain           | Knowledge System                                |
| Document Type    | Framework                                       |
| Previous Version | 0.2                                             |
| Next Review      | To be determined by Knowledge System governance |

---

# End of Document