# Medical Taxonomy Standard (MTS)

> **Document Status:** Released
> **Version:** 1.0
> **Owner:** Amar Smart Doctor
> **System:** ASM Brain — Knowledge System
> **Document Type:** Knowledge System Standard

---

## 1. Purpose

The Medical Taxonomy Standard (MTS) defines how Amar Smart Doctor classifies, organizes, and identifies medical concepts within its Knowledge System.

The purpose of the Medical Taxonomy is to provide a consistent conceptual framework through which medical knowledge can be:

- classified
- organized
- discovered
- related
- reused
- translated
- searched
- maintained
- processed by humans and AI systems

The taxonomy provides the conceptual organization layer of the Knowledge System.

It enables Amar Smart Doctor to maintain a consistent understanding of medical concepts independently of individual webpages, articles, languages, search keywords, or content formats.

---

## 2. Scope

The Medical Taxonomy Standard governs:

- medical concept classification
- concept identity
- concept types
- taxonomy concepts
- classification hierarchy
- parent-child relationships
- controlled terminology
- specialty relationships
- taxonomic relationships
- semantic / knowledge relationship foundations
- multilingual concept representation
- taxonomy governance
- taxonomy versioning
- taxonomy extensibility
- external terminology mapping principles

The Medical Taxonomy does not define:

- Knowledge Asset structure
- evidence quality
- knowledge engineering workflow
- knowledge lifecycle management
- website navigation
- SEO keyword strategy
- database implementation
- API architecture
- AI model architecture
- complete ontology or knowledge graph architecture

Those responsibilities belong to other parts of the Amar Smart Doctor architecture.

---

## 3. Relationship to the Knowledge System

The Medical Taxonomy is one component of the broader Amar Smart Doctor Knowledge System.

The major responsibilities are separated as follows:

### Knowledge Asset Standard (KAS)

Defines:

> What is a Knowledge Asset?

### Knowledge Engineering Framework (KEF)

Defines:

> How is knowledge engineered into Knowledge Assets?

### Medical Taxonomy Standard (MTS)

Defines:

> How are medical concepts classified, organized, and identified?

### Evidence Standard

Defines:

> How is evidence evaluated and trusted?

### Knowledge Lifecycle

Defines:

> How are Knowledge Assets maintained and evolved over time?

These standards are complementary and should not duplicate one another.

---

## 4. Core Principle

The central principle of the Medical Taxonomy is:

> **Every Taxonomy Concept must have a stable conceptual identity, a defined conceptual type, controlled terminology, and consistent classification within the Amar Smart Doctor Knowledge System.**

The taxonomy should make medical knowledge easier to organize without unnecessarily restricting the relationships between concepts.

---

## 5. Taxonomy Is a Classification System

The Medical Taxonomy is a controlled classification system.

It answers questions such as:

- What type of medical concept is this?
- Where does this concept belong?
- What broader concept contains it?
- What narrower concepts belong beneath it?
- Which specialties are associated with it?
- What terminology represents the concept?

The taxonomy is not intended to become:

- a medical encyclopedia
- a content hierarchy
- a website menu
- an SEO structure
- a list of every medical fact

Its purpose is conceptual organization.

---

## 6. Taxonomy and Ontology

The Medical Taxonomy should be distinguished from a full medical ontology.

### Taxonomy

Primarily answers:

> **Where does this concept belong?**

### Ontology

Answers a broader question:

> **What is this concept, and how does it relate to other concepts?**

For example, a taxonomic classification may represent:

- Polycystic Ovary Syndrome
- classified as
- Condition

Whereas richer conceptual relationships may include:

- Polycystic Ovary Syndrome
- affects
- Ovary

- Polycystic Ovary Syndrome
- associated-with
- Insulin Resistance

- Polycystic Ovary Syndrome
- may-present-with
- Irregular Menstruation

The Medical Taxonomy establishes the foundation for classification and controlled relationships.

A full ontology or knowledge graph is outside the scope of this milestone.

---

## 7. Concept Model

The taxonomy distinguishes three related but different concepts:

### 7.1 Concept Type

A Concept Type identifies the general kind of medical concept.

Examples:

- Condition
- Symptom / Sign
- Anatomy
- Medication / Therapeutic Agent

A Concept Type is a classification category.

It is not necessarily a specific medical entity.

---

### 7.2 Taxonomy Concept

A Taxonomy Concept is a specific controlled concept represented within the Medical Taxonomy.

Examples:

- Polycystic Ovary Syndrome
- Ovary
- Ultrasound
- Metformin
- Gynecology

A Taxonomy Concept may belong to a Concept Type and may participate in one or more classification relationships.

---

### 7.3 Classification Relationship

A Classification Relationship defines how one Taxonomy Concept is positioned relative to another within the taxonomy.

Examples:

- Polycystic Ovary Syndrome
- is-a / narrower-than
- Endocrine Disorder

The three-layer distinction is therefore:

Concept Type
↓
Taxonomy Concept
↓
Classification Relationship

This distinction prevents Concept Types from being confused with individual medical concepts or hierarchy nodes.

---

## 8. Stable Concept Identity

Every Taxonomy Concept must have a stable conceptual identity.

The identity should remain independent of:

- webpage URL
- page title
- article title
- language
- spelling variation
- SEO keyword
- content format
- publication channel

For example:

Concept:

Polycystic Ovary Syndrome

English term:

Polycystic Ovary Syndrome

Common abbreviation:

PCOS

Bangla representation:

পলিসিস্টিক ওভারি সিনড্রোম

Website URL:

May change

Concept identity:

Should remain stable

The concept is therefore treated as a knowledge entity rather than as a webpage.

---

## 9. Concept Identifier

Every Taxonomy Concept must have a stable internal identifier.

The identifier should:

- uniquely identify the concept
- remain stable across content formats
- remain independent of URLs
- remain independent of language
- support future database implementation
- support future knowledge graph implementation

The exact identifier syntax is an implementation decision and is not fixed by this standard.

For example, a future implementation might use:

concept_id:
med-condition-pcos

The example is illustrative only.

---

## 10. Core Concept Types

The initial Medical Taxonomy should support a controlled set of core Concept Types.

The proposed core Concept Types are:

1. Condition
2. Symptom / Sign
3. Finding
4. Anatomy
5. Procedure / Intervention
6. Investigation / Diagnostic Test
7. Medication / Therapeutic Agent
8. Risk Factor
9. Prevention / Health Concept
10. Specialty
11. Other Controlled Medical Concept

These Concept Types represent the initial conceptual foundation.

They are not intended to represent every possible medical entity.

The taxonomy may introduce additional Concept Types through controlled future revisions.

---

## 11. Other Controlled Medical Concept

Other Controlled Medical Concept is an exception category rather than a general-purpose miscellaneous bucket.

It may temporarily accommodate medically meaningful concepts that do not yet have an appropriate core Concept Type.

Use of this category should trigger governance awareness.

If repeated or significant use demonstrates that a new Concept Type is required, the taxonomy should be revised rather than allowing the exception category to expand indefinitely.

The category should therefore be treated as:

Unclassified / Exceptional Concept
↓
Governance Review
↓
Remain exceptional

OR

Create appropriate Concept Type

---

## 12. Condition

A Condition represents a recognized medical disease, disorder, syndrome, injury, or other clinically meaningful pathological state.

Examples include:

- Polycystic Ovary Syndrome
- Diabetes Mellitus
- Hypertension
- Endometriosis
- Asthma
- Migraine

Conditions may have:

- parent classifications
- child classifications
- associated symptoms
- associated findings
- anatomical relationships
- risk factors
- diagnostic procedures
- treatments
- specialty relationships

The detailed relationship model belongs to the broader Knowledge System architecture.

---

## 13. Symptom / Sign

A Symptom / Sign represents a clinically observable or reported manifestation associated with a medical condition or state.

Examples include:

- abdominal pain
- headache
- fever
- irregular menstruation
- shortness of breath

Symptoms and signs should maintain stable conceptual identities even when their wording differs across languages or content formats.

---

## 14. Finding

A Finding represents an observed result or clinically meaningful observation.

Examples may include:

- elevated blood glucose
- enlarged ovary
- abnormal laboratory result
- imaging finding

A Finding should be distinguished from a Symptom / Sign because a finding may be discovered through:

- examination
- laboratory investigation
- imaging
- pathology
- other diagnostic processes

---

## 15. Anatomy

An Anatomy concept represents a body structure, organ, tissue, anatomical region, or other recognized anatomical entity.

Examples include:

- ovary
- uterus
- liver
- heart
- pancreas
- breast

Anatomical concepts provide important anchors for medical relationships.

---

## 16. Procedure / Intervention

A Procedure / Intervention represents a medical procedure, therapeutic intervention, surgical procedure, diagnostic intervention, or other clinically meaningful action.

Examples include:

- laparoscopic surgery
- biopsy
- physical therapy
- cesarean delivery
- endoscopy

The exact classification of procedures may be expanded in future taxonomy versions.

---

## 17. Investigation / Diagnostic Test

An Investigation / Diagnostic Test represents a method or test used to obtain diagnostic information.

Examples include:

- blood glucose test
- ultrasound
- MRI
- CT scan
- complete blood count

The distinction between a test, test method, test result, and finding should be preserved where meaningful.

---

## 18. Medication / Therapeutic Agent

A Medication / Therapeutic Agent represents a medicinal product, active therapeutic agent, or recognized pharmacological treatment concept.

Examples may include:

- metformin
- insulin
- antibiotics
- antihypertensive agents

The taxonomy establishes the concept category.

Detailed drug databases, prescribing information, dosage rules, contraindications, and clinical treatment guidance are outside the scope of the Medical Taxonomy Standard.

---

## 19. Risk Factor

A Risk Factor represents a characteristic, exposure, behavior, condition, or circumstance associated with an increased probability of a medical outcome.

Examples may include:

- smoking
- obesity
- family history
- age
- physical inactivity

A risk factor is not automatically a cause.

The taxonomy should preserve the conceptual distinction between:

- risk factor
- association
- cause
- protective factor

Detailed evidence interpretation belongs to the Evidence Standard and Knowledge Engineering Framework.

---

## 20. Prevention / Health Concept

This Concept Type may include recognized concepts relating to:

- prevention
- screening
- health promotion
- lifestyle
- protective factors
- health maintenance

This category should remain controlled and should not become a general container for arbitrary health content.

---

## 21. Specialty

A Specialty represents a recognized medical specialty, subspecialty, or clinical domain.

Examples include:

- Gynecology
- Obstetrics
- Cardiology
- Neurology
- Endocrinology
- Dermatology

Specialties provide classification and discovery relationships.

A medical condition should not necessarily be assigned to only one specialty.

---

## 22. Classification Hierarchy

The taxonomy may use hierarchical relationships to represent broader and narrower concepts.

The fundamental hierarchy is:

Broader Taxonomy Concept
↓
Narrower Taxonomy Concept

For example:

Medical Condition
↓
Endocrine Disorder
↓
Polycystic Ovary Syndrome

In this example:

- Condition is a Concept Type.
- Medical Condition may function as a Taxonomy Concept or classification concept.
- Endocrine Disorder is a Taxonomy Concept.
- Polycystic Ovary Syndrome is a Taxonomy Concept.

The hierarchy should represent meaningful conceptual relationships.

It should not be designed primarily around:

- website navigation
- SEO categories
- content publishing convenience

---

## 23. Parent-Child Classification

A parent-child classification relationship indicates that one Taxonomy Concept is broader than another.

For example:

Endocrine Disorder
↓
Polycystic Ovary Syndrome

The relationship may be represented conceptually as:

Endocrine Disorder
↓
broader-than
↓
Polycystic Ovary Syndrome

or equivalently:

Polycystic Ovary Syndrome
↓
narrower-than
↓
Endocrine Disorder

The exact technical representation is an implementation concern.

---

## 24. Classification and Relationships Are Separate

Classification and conceptual relationships must not be treated as identical.

For example:

PCOS
│
├── classification → Condition
│
├── specialty → Gynecology
├── specialty → Endocrinology
├── affects → Ovary
├── associated-with → Insulin Resistance
└── may-present-with → Irregular Menstruation

The classification identifies the concept's taxonomy position.

The other relationships describe meaningful relationships between concepts.

This separation is fundamental to the architecture.

---

## 25. Taxonomic Relationships

Taxonomic relationships describe the position of concepts within the classification structure.

Examples include:

- broader-than
- narrower-than
- is-a
- classified-as

These relationships should be controlled and consistently interpreted.

They are the primary relationship family owned by the Medical Taxonomy.

---

## 26. Semantic / Knowledge Relationships

Semantic / Knowledge Relationships describe meaningful connections between medical concepts that go beyond classification.

Examples include:

- affects
- associated-with
- symptom-of
- finding-of
- risk-factor-for
- treated-by
- investigated-by
- managed-by
- part-of
- related-to

For example:

PCOS
↓
affects
↓
Ovary

or:

PCOS
↓
associated-with
↓
Insulin Resistance

These relationships form a controlled foundation for the future Knowledge Model / Knowledge Graph.

They do not constitute the complete ontology.

The final relationship vocabulary, semantics, cardinality, provenance, and validation rules should be defined in a future Knowledge Model / Knowledge Graph architecture.

---

## 27. Multiple Specialty Relationships

A concept may legitimately relate to multiple specialties.

For example:

Polycystic Ovary Syndrome
│
├── Gynecology
├── Endocrinology
└── Reproductive Medicine

The taxonomy should therefore avoid forcing every concept into a single specialty branch.

Specialty relationships should represent meaningful medical associations rather than arbitrary organizational choices.

---

## 28. Controlled Terminology

Each Taxonomy Concept should maintain controlled terminology.

This may include:

- preferred term
- synonyms
- abbreviations
- alternative spellings
- common terms
- historical terms
- multilingual equivalents

Terminology should support consistent identification of the same concept.

For example:

Preferred:

Polycystic Ovary Syndrome

Abbreviation:

PCOS

Alternative:

Polycystic ovarian syndrome

---

## 29. Multilingual Representation

The taxonomy must support multiple languages.

A concept should maintain one stable identity while supporting multiple linguistic representations.

For example:

Concept ID:

[stable internal identifier]

English:

Polycystic Ovary Syndrome

Bangla:

পলিসিস্টিক ওভারি সিনড্রোম

Language variants should represent the same underlying concept where they are true conceptual equivalents.

Translation should not create duplicate concepts merely because the language differs.

---

## 30. Synonyms and Concept Identity

Different terms may refer to the same underlying concept.

The taxonomy should distinguish between:

Different term
≠
Different concept

For example, abbreviations and accepted synonyms may map to one concept.

However, similar terms must not automatically be merged.

Concept equivalence should be determined using appropriate medical and taxonomy governance.

---

## 31. Concept Boundaries

Each Taxonomy Concept should have a clear conceptual boundary.

The taxonomy should avoid creating concepts that are:

- excessively broad
- excessively narrow
- ambiguous
- duplicate representations
- dependent on a particular webpage

For example:

Women's Health

may be too broad to represent a single medical condition.

Whereas:

Polycystic Ovary Syndrome

represents a more clearly bounded medical concept.

The appropriate boundary depends on the concept type and intended Knowledge System use.

---

## 32. Taxonomy Is Not an Evidence System

Taxonomic classification does not establish medical truth.

For example:

PCOS
↓
Condition

This classification does not by itself establish:

- prevalence
- treatment effectiveness
- causation
- prognosis
- diagnostic criteria

Those claims require appropriate evidence and Knowledge Engineering.

The taxonomy organizes concepts.

It does not validate medical claims.

---

## 33. Taxonomy Is Not an SEO System

The taxonomy must not be designed primarily around search-engine keywords.

SEO may use taxonomy information.

However:

Medical Concept
↓
Taxonomy
↓
Knowledge Asset
↓
SEO / Content / Website Output

not:

SEO Keyword
↓
Medical Taxonomy

The Knowledge Layer remains the source of truth.

---

## 34. Taxonomy Is Not Website Navigation

The Medical Taxonomy may influence website organization but must not be identical to it.

For example:

Medical Taxonomy
↓
Knowledge Assets
↓
Website Information Architecture
↓
SEO / User Experience

A website may choose to present concepts differently from the underlying taxonomy.

This separation allows the website to evolve without corrupting the Knowledge Layer.

---

## 35. Taxonomy and Knowledge Assets

Knowledge Assets may reference one or more Taxonomy Concepts.

The relationship is:

Knowledge Asset
↓
references
↓
Taxonomy Concept
↓
Medical Taxonomy

Taxonomy provides the conceptual organization.

KAS defines the structure of the Knowledge Asset.

KEF defines how the knowledge is engineered.

These responsibilities must remain separate.

---

## 36. Taxonomy and Knowledge Engineering

KEF may use the Medical Taxonomy during:

- Knowledge Engineering Objective definition
- concept identification
- classification
- structuring
- relationship assignment
- terminology normalization

KEF does not modify taxonomy definitions arbitrarily.

Taxonomy changes should follow taxonomy governance.

---

## 37. Taxonomy Governance

Changes to the taxonomy should be controlled.

Possible taxonomy changes include:

- adding a Concept Type
- adding a Taxonomy Concept
- changing a classification
- adding a synonym
- merging duplicate concepts
- splitting a concept
- changing a relationship type
- deprecating a concept

Significant changes should be reviewed according to the applicable governance process.

Medical significance should receive appropriate qualified review.

---

## 38. Duplicate Concepts

The taxonomy should actively prevent duplicate representations of the same medical concept.

Potential duplicate signals may include:

- identical concepts with different names
- language duplicates
- spelling variations
- unnecessary abbreviations
- overlapping concept definitions

When duplicates are discovered, the system should determine whether the concepts should:

- be merged
- remain separate
- be mapped as synonyms
- be related but distinct

This decision should be documented where significant.

---

## 39. Concept Deprecation

A concept may become deprecated when:

- it is obsolete
- it was created incorrectly
- it duplicates another concept
- terminology has changed
- the classification model has changed

Deprecated concepts should not simply disappear.

Where practical, they should retain a relationship to the preferred replacement concept.

For example:

Deprecated Concept
↓
replaced-by
↓
Preferred Concept

This preserves historical traceability.

---

## 40. Taxonomy Versioning

The Medical Taxonomy must be versioned.

Versioning should allow the system to identify:

- when taxonomy changes occurred
- what changed
- why the change occurred
- which concepts were affected
- whether existing Knowledge Assets require review

Taxonomy versions should remain compatible with Knowledge System governance.

The exact technical version-control implementation will be defined later.

---

## 41. Taxonomy Change Impact

A taxonomy change may affect existing Knowledge Assets.

For example:

Taxonomy Change
↓
Affected Concepts
↓
Affected Knowledge Assets
↓
Impact Assessment
↓
Update if required

The Knowledge Lifecycle should manage the broader maintenance process.

KEF may be invoked if substantive knowledge engineering is required.

---

## 42. Extensibility

The taxonomy should be extensible without requiring a redesign of the entire Knowledge System.

Future versions may add:

- additional Concept Types
- additional Taxonomy Concepts
- additional relationship types
- additional terminology systems
- additional languages
- specialized medical domains
- standardized external mappings

Expansion should be driven by real Knowledge System requirements.

New structures should not be added merely because they are theoretically possible.

---

## 43. External Terminology and Standards

The Amar Smart Doctor taxonomy may support mappings to recognized external medical terminology or classification systems where useful.

Potential examples include:

- ICD
- SNOMED CT
- MeSH
- LOINC
- RxNorm

These are examples of potential interoperability mappings, not committed dependencies.

Different external standards serve different purposes.

For example:

- ICD may support disease classification and coding.
- SNOMED CT may support clinical terminology.
- MeSH may support biomedical literature indexing.
- LOINC may support laboratory and clinical observations.
- RxNorm may support medication terminology.

The choice of external mappings should be determined later according to actual platform requirements, interoperability needs, licensing considerations, and implementation feasibility.

External codes or identifiers must not replace the stable internal Amar Smart Doctor concept identity.

---

## 44. AI and Taxonomy

AI systems may assist with taxonomy-related tasks such as:

- concept identification
- duplicate detection
- synonym discovery
- classification suggestions
- terminology normalization
- relationship suggestions

AI-generated taxonomy decisions must not automatically become authoritative.

Where taxonomy changes have significant medical or structural implications, appropriate human review is required.

The governing principle remains:

> **AI may recommend classification; governance establishes classification.**

---

## 45. Taxonomy Quality Principles

The Medical Taxonomy should prioritize:

### Stability

Concept identities should remain stable.

### Clarity

Concept definitions and classifications should be understandable.

### Consistency

Similar concepts should follow consistent classification rules.

### Non-Duplication

The taxonomy should minimize unnecessary duplicate concepts.

### Extensibility

The taxonomy should support future growth.

### Interoperability

Where useful, concepts should be capable of mapping to recognized external standards.

### Language Independence

Concept identity should not depend on a single language.

### Medical Validity

Taxonomic classifications should remain medically meaningful.

### Maintainability

The taxonomy should remain manageable as the knowledge base grows.

---

## 46. Relationship to Search

The taxonomy may support future search capabilities by enabling:

- concept-aware search
- synonym matching
- multilingual search
- related-concept discovery
- specialty filtering
- structured navigation

Search implementation is outside the scope of MTS.

The taxonomy provides the conceptual signals that future search systems may consume.

---

## 47. Relationship to Knowledge Graph

The Medical Taxonomy establishes a foundation that can later support a richer Knowledge Graph.

The future architecture may evolve toward:

Medical Concepts
↓
Controlled Relationships
↓
Knowledge Graph
↓
AI / Search / Product Experiences

MTS does not define the complete graph model.

That decision belongs to a future platform architecture milestone after sufficient real Knowledge Assets exist to justify it.

---

## 48. Governance Principle

The Medical Taxonomy should evolve through evidence and practical use.

The governing principle is:

> **Start with a controlled core, validate it against real Knowledge Assets, and expand only when the evidence requires expansion.**

The taxonomy should not attempt to achieve theoretical completeness before Amar Smart Doctor has real knowledge to organize.

---

## 49. Acceptance Criteria

Medical Taxonomy v1.0 may be approved when:

- [x] Purpose and scope are clearly defined
- [x] Taxonomy responsibility is clearly defined
- [x] Relationship to KAS is defined
- [x] Relationship to KEF is defined
- [x] Relationship to Evidence Standard is defined
- [x] Relationship to Knowledge Lifecycle is defined
- [x] Taxonomy is clearly distinguished from ontology
- [x] Stable concept identity is defined
- [x] Concept identifier principles are defined
- [x] Concept Type and Taxonomy Concept are clearly distinguished
- [x] Core Concept Types are defined
- [x] Exception category governance is defined
- [x] Classification hierarchy is defined
- [x] Parent-child classification is defined
- [x] Classification is separated from conceptual relationships
- [x] Taxonomic relationships are defined
- [x] Semantic / Knowledge relationship principles are defined
- [x] Multiple specialty relationships are supported
- [x] Controlled terminology principles are defined
- [x] Multilingual representation is defined
- [x] Synonym handling is defined
- [x] Concept boundary principles are defined
- [x] Duplicate handling is defined
- [x] Deprecation principles are defined
- [x] Taxonomy governance is defined
- [x] Taxonomy versioning is defined
- [x] Change impact principles are defined
- [x] Extensibility principles are defined
- [x] External terminology mapping principles are defined
- [x] AI responsibilities are defined
- [x] Technology independence is preserved
- [x] Website and SEO boundaries are preserved
- [x] Knowledge Graph boundary is preserved
- [x] The document has been reviewed against the broader ASM Brain architecture

---

## 50. Document Control

| Field | Value |
|---|---|
| Document | Medical Taxonomy Standard |
| Short Name | MTS |
| Version | 1.0 |
| Status | Released |
| Owner | Amar Smart Doctor |
| System | ASM Brain |
| Domain | Knowledge System |
| Document Type | Standard |
| Previous Version | 0.2 |
| Release Milestone | S1-04.3 |

---

# End of Document