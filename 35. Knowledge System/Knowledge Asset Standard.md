# Knowledge Asset Standard (KAS)

> **Document Status:** Approved  
> **Version:** 1.0  
> **Owner:** Amar Smart Doctor  
> **System:** ASM Brain — Knowledge System  
> **Document Type:** Knowledge System Standard

---

## 1. Purpose

Amar Smart Doctor is being built as a structured healthcare knowledge platform.

The primary organizational asset is not the webpage, article, application, or AI response.

The primary asset is **trusted, structured, reusable knowledge**.

Knowledge Assets provide the foundational units through which medical knowledge can be:

- researched
- structured
- reviewed
- governed
- connected
- maintained
- published
- retrieved
- reused across multiple products and channels

The Knowledge Asset Standard (KAS) establishes the canonical definition and logical structure of a Knowledge Asset within Amar Smart Doctor.

---

## 2. Scope

This standard defines:

- what constitutes a Knowledge Asset
- the characteristics of a valid Knowledge Asset
- Knowledge Asset identity
- Knowledge Asset types
- logical asset structure
- metadata
- evidence traceability
- relationships
- governance
- versioning
- lifecycle principles
- quality requirements
- human and machine consumption

This standard is intentionally **technology-independent**.

It defines the logical knowledge model rather than a:

- database schema
- API specification
- website template
- search implementation
- AI prompt
- software architecture

Those concerns belong to later Knowledge System and Engineering specifications.

---

## 3. Definition of a Knowledge Asset

A **Knowledge Asset** is a:

> **Bounded, identifiable, structured, governed, evidence-traceable, and reusable unit of knowledge maintained within the Amar Smart Doctor Knowledge System.**

### 3.1 Bounded Knowledge

A Knowledge Asset represents a defined knowledge concept with a clear scope.

It should be possible to independently:

- identify it
- reference it
- govern it
- review it
- version it
- relate it to other assets
- reuse it

A Knowledge Asset should not represent an unnecessarily broad collection of unrelated knowledge.

For example, `PCOS` may be a Knowledge Asset.

Whereas `Everything About Women's Health` would generally be too broad to function as a single Knowledge Asset.

### 3.2 Knowledge Asset Is Not Content

A Knowledge Asset is not the same thing as a:

- webpage
- article
- social media post
- video script
- AI response
- advertisement
- presentation

These are **outputs or presentations** that may be generated from, derived from, or informed by one or more Knowledge Assets.

The conceptual relationship is:

**Research → Evidence → Knowledge Engineering → Knowledge Asset → Product / Content / AI Output**

---

## 4. Core Principles

Every Knowledge Asset should follow the following principles.

### 4.1 Structured

Knowledge should be represented in a consistent structure rather than existing only as free-form prose.

### 4.2 Bounded

Each asset should represent a defined knowledge concept with a clear scope.

### 4.3 Reusable

A Knowledge Asset should be usable across multiple outputs and products.

### 4.4 Evidence-Traceable

Significant medical claims should be traceable to appropriate supporting evidence.

### 4.5 Governed

Knowledge must have defined ownership, review, approval, and maintenance responsibilities.

### 4.6 Versioned

Changes to important knowledge must be trackable over time.

### 4.7 Relational

Knowledge should be capable of being connected to related concepts and approved entities.

### 4.8 Human-Readable

Knowledge must remain understandable and reviewable by qualified humans.

### 4.9 Machine-Readable

The logical structure should allow future software and AI systems to consume the knowledge reliably.

### 4.10 Presentation-Independent

Knowledge should not depend on a particular website, application, document format, or user interface.

### 4.11 Safety-Oriented

Medical knowledge must prioritize:

- accuracy
- appropriate evidence
- responsible wording
- appropriate uncertainty
- avoidance of unsafe interpretation

---

## 5. Knowledge Asset Identity

Every Knowledge Asset must have a unique identity within the Knowledge System.

At minimum, an asset should have:

| Property | Purpose |
|---|---|
| Asset ID | Unique identity |
| Canonical Name | Primary name of the concept |
| Asset Type | Defines the type of knowledge represented |
| Status | Defines the current governance state |
| Version | Identifies the current version |

### 5.1 Stable Identity

The Asset ID should remain stable throughout the normal lifecycle of the asset.

Changing the presentation title of an asset should not automatically create a new asset.

The identity represents the **underlying knowledge concept**, not a particular presentation of that concept.

---

## 6. Knowledge Asset Types

The Knowledge System should support multiple categories of Knowledge Assets.

The initial categories establish the foundation and may evolve as the system matures.

### 6.1 Clinical Knowledge Assets

Examples include:

- Disease
- Condition
- Symptom
- Sign
- Risk Factor
- Complication
- Diagnosis Concept
- Treatment Concept
- Procedure Concept
- Medicine Concept
- Prevention Concept
- Anatomy Concept

### 6.2 Educational Knowledge Assets

Examples include:

- Health Education Topic
- Patient Education Concept
- Health Guidance Topic
- Frequently Asked Question

### 6.3 Other Knowledge Assets

Future categories may be introduced where they represent legitimate bounded knowledge concepts.

Examples may include:

- Clinical Guideline Concept
- Medical Classification Concept
- Evidence Concept
- Medical Rule

The asset type system must remain extensible.

New types should be introduced through controlled governance rather than arbitrary creation.

---

## 7. Knowledge Entities

Healthcare entities such as people and organizations are related to the Knowledge System but are **not automatically classified as Knowledge Assets** under this standard.

Examples include:

- Doctors
- Hospitals
- Clinics
- Healthcare Organizations

These represent real-world entities about which Amar Smart Doctor may maintain structured information.

For example:

**Disease: Diabetes**  
→ `treated_by` → **Doctor: Dr. Example**

The disease and the doctor participate in the same knowledge ecosystem, but they represent fundamentally different kinds of objects.

The final model for:

- Doctor entities
- Hospital entities
- Clinic entities
- Healthcare organization entities

will be defined separately as the Amar Smart Doctor Entity Model evolves.

Until that model is formally established, these entities must not be assumed to be Knowledge Asset types.

---

## 8. Knowledge Asset Structure

A Knowledge Asset consists of several logical layers.

These layers define the conceptual structure of an asset.

They do **not** prescribe a technical implementation.

The logical structure is:

**Knowledge Asset**

1. Identity Layer
2. Knowledge Layer
3. Evidence Layer
4. Relationship Layer
5. Governance Layer
6. Lifecycle Layer

---

### 8.1 Identity Layer

Defines what the asset is.

Typical elements include:

- Asset ID
- Canonical Name
- Asset Type
- Alternate Names
- Language
- Status
- Version

---

### 8.2 Knowledge Layer

Contains the knowledge represented by the asset.

Depending on the asset type, this may include:

- Definition
- Description
- Characteristics
- Symptoms
- Causes
- Risk Factors
- Diagnosis
- Treatment
- Prevention
- Complications
- Clinical Considerations
- Patient Education Information

The exact fields depend on the asset type.

Not every asset type will contain every field.

---

### 8.3 Evidence Layer

Records the evidence supporting the knowledge represented by the asset.

The evidence layer should allow the system to identify:

- supporting source
- source type
- publication or update information where applicable
- relevant evidence
- citation or reference
- verification status
- review information

Where practical, significant medical claims should be traceable to the specific evidence supporting those claims.

The detailed evidence hierarchy, source credibility, citation requirements, and verification rules will be defined in the **Evidence Standard**.

---

### 8.4 Relationship Layer

Defines connections between the asset and:

- other Knowledge Assets
- approved system entities

Examples include:

- Diabetes → `has_symptom` → Increased Thirst
- Diabetes → `associated_with` → Obesity
- Diabetes → `treated_by` → Insulin
- Diabetes → `related_specialty` → Endocrinology

Relationships should use controlled relationship types rather than relying only on informal textual references.

---

### 8.5 Governance Layer

Defines how the asset is controlled.

May include:

- Creator
- Reviewer
- Approver
- Owner
- Review Status
- Approval Date
- Last Review Date
- Required Review Date

---

### 8.6 Lifecycle Layer

Defines the current state of the asset.

Examples include:

- Draft
- Under Review
- Approved
- Published
- Under Maintenance
- Archived

The detailed lifecycle model will be defined separately in the **Knowledge Lifecycle** specification.

---

## 9. Metadata Standard

Each Knowledge Asset should contain sufficient metadata to support:

- identification
- classification
- governance
- retrieval
- maintenance
- version control
- interoperability

### 9.1 Identity Metadata

- Asset ID
- Canonical Name
- Asset Type
- Language

### 9.2 Classification Metadata

- Category
- Specialty
- Taxonomy Identifiers
- Relevant Classification Terms

### 9.3 Governance Metadata

- Owner
- Creator
- Reviewer
- Approver
- Status

### 9.4 Version Metadata

- Version
- Created Date
- Updated Date
- Review Date

### 9.5 Evidence Metadata

- Evidence Status
- Source References
- Verification Information

The exact machine-readable field specification will be defined later during technical architecture.

---

## 10. Evidence and Source Traceability

Medical Knowledge Assets must maintain traceability to their supporting evidence.

The system should allow an authorized reviewer to determine:

> **Where did this knowledge come from?**

Evidence should be associated with the claims or knowledge elements it supports wherever practical.

For example:

- Claim A → Evidence Source 1
- Claim B → Evidence Source 2
- Claim C → Evidence Source 3

This is preferable to attaching a collection of sources to an entire asset without identifying what each source supports.

The exact technical implementation of claim-level evidence traceability will be determined later.

### 10.1 AI and Evidence

AI-generated text is **not**, by itself, considered authoritative medical evidence.

AI may assist with:

- research
- extraction
- synthesis
- transformation
- quality checking

However, medical knowledge must ultimately be traceable to appropriate external or approved authoritative sources.

The detailed rules will be defined in the **Evidence Standard**.

---

## 11. Knowledge Relationships

Knowledge Assets should be capable of forming a structured network.

Relationships may represent concepts such as:

- `related_to`
- `has_symptom`
- `has_risk_factor`
- `caused_by`
- `diagnosed_by`
- `treated_by`
- `prevented_by`
- `complication_of`
- `associated_with`
- `part_of`
- `related_specialty`

Relationships may also connect Knowledge Assets with approved real-world entities.

For example:

**Disease** → `treated_by` → **Doctor Entity**

Relationship types must eventually be controlled by the Knowledge System rather than created arbitrarily.

This structure enables future development of:

- knowledge graphs
- semantic search
- recommendation systems
- AI retrieval
- related-topic navigation
- structured SEO relationships

---

## 12. Governance

Every Knowledge Asset must have clear governance responsibility.

The Knowledge System must distinguish between the following roles.

### Creator

The person or system that creates or prepares the asset.

### Reviewer

The qualified person responsible for reviewing the asset.

### Approver

The authority responsible for approving the asset for its applicable status.

### Owner

The role responsible for ongoing maintenance of the asset.

These roles may be performed by the same or different individuals depending on the organizational model and asset type.

### 12.1 AI Governance

AI systems may assist with:

- research
- drafting
- transformation
- analysis
- quality checks

However:

> **AI output does not replace required human authority for medically significant approval.**

---

## 13. Versioning

Knowledge Assets must support controlled versioning.

A version represents a defined state of the asset at a particular point in its development or maintenance.

Version changes should allow the system to determine:

- what changed
- when it changed
- why it changed
- who changed it
- whether review was required
- whether approval was required

Minor corrections and substantial changes may require different versioning treatment.

Detailed versioning rules will be established as the Knowledge System matures.

---

## 14. Lifecycle

The Knowledge Asset lifecycle describes the governed states through which an asset may progress.

The conceptual lifecycle is:

**Draft → Under Review → Approved → Published → Under Maintenance → Archived**

An asset may move between states according to defined governance rules.

For example, an approved asset may return to an appropriate review state when new evidence requires substantive revision.

### 14.1 Research Is Not a Lifecycle State

Research is not treated as a Knowledge Asset lifecycle state.

Research is a production activity governed by the **Knowledge Engineering Framework**.

Therefore:

**Research → Evidence → Knowledge Engineering → Knowledge Asset → Lifecycle Management**

The detailed lifecycle rules will be defined in the **Knowledge Lifecycle** specification.

---

## 15. Quality Requirements

A Knowledge Asset intended for medical use should satisfy the following quality principles.

### 15.1 Accuracy

The information should accurately represent the available evidence.

### 15.2 Evidence Adequacy

Significant medical claims should have appropriate supporting evidence.

### 15.3 Clarity

The information should be understandable to its intended audience.

### 15.4 Completeness

The asset should contain the information required for its defined asset type and intended use.

### 15.5 Consistency

Terminology and structure should remain consistent across related assets.

### 15.6 Traceability

Significant claims should be traceable to supporting evidence.

### 15.7 Currency

The asset should be reviewed and updated when evidence or accepted medical practice changes.

### 15.8 Safety

The asset should avoid:

- misleading certainty
- unsupported claims
- unsafe interpretation
- presentation that could reasonably cause harmful misunderstanding

---

## 16. Human and AI Consumption

Knowledge Assets must be designed for both human and machine consumption.

### 16.1 Human Consumers

May include:

- Researchers
- Medical Reviewers
- Editors
- Content Teams
- Product Teams
- Administrators

### 16.2 Machine Consumers

May include:

- Search Systems
- AI Retrieval Systems
- AI Agents
- Recommendation Systems
- Content Generation Systems
- APIs
- Future Applications

Machine readability must not come at the expense of:

- medical accuracy
- human reviewability
- evidence traceability
- understandable presentation

---

## 17. Separation Between Knowledge and Presentation

A Knowledge Asset must remain independent from the way it is presented.

The same asset may produce or support:

**Knowledge Asset**
→ Website Page  
→ SEO Content  
→ FAQ  
→ Social Media Content  
→ Video Script  
→ AI Response  
→ Future Application

Changes to presentation should not require unnecessary duplication of the underlying knowledge.

This principle protects the **Knowledge Layer as the primary organizational asset**.

---

## 18. Separation Between Knowledge and Research

Research and Knowledge Assets are related but are not identical.

Research is the process and supporting activity used to:

- discover information
- locate evidence
- evaluate sources
- understand findings
- prepare information for knowledge engineering

A Knowledge Asset is the governed structured representation of approved knowledge.

Therefore:

**Research → Evidence → Knowledge Engineering → Knowledge Asset**

The **Knowledge Engineering Framework (KEF)** will define this transformation in detail.

---

## 19. Separation Between Knowledge Asset and Content Output

A website page or content item is a presentation or distribution output.

A Knowledge Asset is a knowledge-layer object.

Therefore:

> **One Knowledge Asset may support multiple outputs, and one output may draw from multiple Knowledge Assets.**

For example:

**Knowledge Assets**
→ Website Article  
→ Disease Page  
→ FAQ  
→ Social Content  
→ Video  
→ AI Response

This prevents the Knowledge System from becoming dependent on the website architecture.

---

## 20. Implementation Boundary

KAS defines the **logical standard only**.

Future engineering work may represent Knowledge Assets using:

- structured documents
- databases
- JSON
- APIs
- search indexes
- knowledge graphs
- other appropriate technologies

The implementation must preserve the logical requirements established by this standard.

Technical implementation decisions must not redefine the meaning of a Knowledge Asset without appropriate architecture review.

---

## 21. Extensibility

The Knowledge Asset Standard is designed to evolve.

New:

- asset types
- metadata
- relationship types
- governance requirements

may be introduced as Amar Smart Doctor develops.

However, changes should be:

- documented
- versioned
- reviewed
- backward-compatible where practical

The system should favor **controlled evolution over unnecessary complexity**.

---

## 22. Relationship to Other Knowledge System Components

The Knowledge Asset Standard is one component of the broader Knowledge System.

Its relationship with the other components is:

**Knowledge Asset Standard**
→ Defines **WHAT** an Asset is

**Knowledge Engineering Framework**
→ Defines **HOW** Assets are produced

**Medical Taxonomy**
→ Defines **HOW** knowledge is classified

**Evidence Standard**
→ Defines **HOW** evidence is evaluated

**Knowledge Lifecycle**
→ Defines **HOW** Assets are maintained

Together, these components establish the foundation of the Amar Smart Doctor Knowledge System.

---

## 23. Acceptance Criteria

KAS v1.0 may be approved when:

- [ ] Knowledge Asset is clearly defined
- [ ] Asset boundedness is clearly defined
- [ ] Purpose and scope are established
- [ ] Core principles are documented
- [ ] Asset identity is defined
- [ ] Initial asset types are established
- [ ] Healthcare entities are appropriately separated from Knowledge Assets
- [ ] Logical asset structure is defined
- [ ] Metadata requirements are established
- [ ] Evidence traceability is established
- [ ] Significant medical claims can be conceptually traced to evidence
- [ ] Relationships are defined conceptually
- [ ] Governance responsibilities are established
- [ ] Versioning principles are established
- [ ] Lifecycle principles are established
- [ ] Research is separated from the asset lifecycle
- [ ] Quality requirements are established
- [ ] Human and AI consumption requirements are established
- [ ] Knowledge is separated from presentation
- [ ] Technical implementation boundaries are clear
- [ ] The document can support future technical implementation
- [ ] The document has been reviewed and approved by the project architecture owner

---

## 24. Document Control

| Field            | Value                    |
| ---------------- | ------------------------ |
| Document         | Knowledge Asset Standard |
| Short Name       | KAS                      |
| Version          | 1.0                      |
| Status           | Approved                 |
| Owner            | Amar Smart Doctor        |
| System           | ASM Brain                |
| Domain           | Knowledge System         |
| Previous Version | 0.2                      |
| Next Review      |                          |

---

# End of Document