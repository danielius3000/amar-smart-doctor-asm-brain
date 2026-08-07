# Knowledge Dependency & Relationship Standard

**Document ID:** KDRS-001
**Document Name:** Knowledge Dependency & Relationship Standard
**Version:** 1.0
**Status:** Release Candidate
**Owner:** Amar Smart Doctor
**System:** ASM Brain
**Knowledge System:** Amar Smart Doctor Knowledge System
**Related Standards:** Knowledge Asset Standard (KAS), Knowledge Engineering Framework (KEF), Medical Taxonomy Standard (MTS), Evidence Standard (ES), Knowledge Lifecycle Standard (KLS)
**Created:** 2026-08-08
**Updated:** 2026-08-08

---

# 1. Purpose

The Knowledge Dependency & Relationship Standard (KDRS) defines how relationships between Knowledge Assets, evidence, medical concepts, and other governed knowledge objects are represented within ASM Brain.

The purpose of KDRS is to ensure that relationships between knowledge objects are:

- intentional
- semantically defined
- independently identifiable
- directional where appropriate
- distinguishable by relationship type
- traceable
- governed
- reusable
- capable of supporting impact analysis

Knowledge within ASM Brain must not become a collection of isolated documents.

The system must be able to understand how one knowledge object relates to another and why that relationship exists.

---

# 2. Scope

This standard defines the conceptual architecture for:

- knowledge relationships
- relationship identifiers
- relationship types
- relationship assertions
- relationship categories
- directional relationships
- dependency relationships
- association relationships
- derivation relationships
- relationship semantics
- relationship authority
- relationship provenance
- relationship governance
- dependency tracing
- impact propagation
- relationship lifecycle considerations
- relationship integrity
- relationship versioning
- relationship reassessment
- relationship retirement and invalidation
- relationship inclusion
- controlled relationship-category extension
- inferred relationship boundaries
- historical relationship preservation

This standard does not define:

- database schemas
- graph database technology
- API architecture
- graph algorithms
- user interface design
- search implementation
- AI model architecture
- Experience Layer implementation

Those concerns belong to future implementation specifications.

---

# 3. Architectural Position

KDRS extends the Knowledge System established by the existing standards.

The relationship between the core standards is:

Knowledge Asset Standard (KAS)
↓
Defines governed Knowledge Assets
↓
Knowledge Engineering Framework (KEF)
↓
Defines how knowledge is engineered
↓
Medical Taxonomy Standard (MTS)
↓
Defines medical classification and conceptual relationships
↓
Evidence Standard (ES)
↓
Defines evidence and evidence relationships
↓
Knowledge Lifecycle Standard (KLS)
↓
Defines how knowledge changes over time
↓
Knowledge Dependency & Relationship Standard (KDRS)
↓
Defines how governed knowledge objects relate to one another

KDRS therefore acts as a relationship architecture connecting the other Knowledge System components.

KDRS does not replace the authority of any existing standard.

---

# 4. Core Principle

Knowledge relationships are part of the knowledge architecture.

A relationship must not be treated as an arbitrary hyperlink.

The conceptual model is:

Source Object
↓
Governed Relationship Assertion
↓
Target Object

The relationship has meaning in its own right.

For example:

Knowledge Asset A
──depends_on──>
Evidence Claim B

is different from:

Knowledge Asset A
──related_to──>
Knowledge Asset B

The system must preserve that distinction.

---

# 5. Relationship Architecture

KDRS distinguishes between three related concepts:

1. Relationship Category
2. Relationship Type
3. Relationship Assertion

These concepts must not be collapsed into one.

The architecture is:

Relationship Category
↓
groups related relationship meanings
↓
Relationship Type
↓
defines a specific semantic relationship
↓
Relationship Assertion
↓
applies that meaning to specific governed objects

Every governed Relationship Assertion that requires independent identification has a Relationship Identifier.

The Relationship Identifier is not a separate knowledge object.

---

# 6. Relationship Category

A Relationship Category provides a broad semantic grouping for Relationship Types.

KDRS establishes three foundational categories:

1. Dependency
2. Association
3. Derivation

A Relationship Category is not itself an individual relationship.

It provides the higher-level semantic classification under which Relationship Types are governed.

For example:

Dependency
↓
depends_on

Association
↓
related_to

Derivation
↓
derived_from

The category hierarchy allows the Knowledge System to reason about relationships at both broad and specific levels.

---

# 7. Foundational Relationship Categories

## 7.1 Dependency

A Dependency relationship represents a material dependency between one governed object and another.

Example:

Knowledge Asset A
──depends_on──>
Evidence Claim B

---

## 7.2 Association

An Association relationship represents a meaningful connection that does not necessarily imply dependency or derivation.

Example:

Medical Concept A
──related_to──>
Medical Concept B

---

## 7.3 Derivation

A Derivation relationship represents the origin or transformation of knowledge from another governed object.

Example:

Knowledge Asset A
──derived_from──>
Evidence Synthesis B

---

# 8. Relationship Category Extension

Dependency, Association, and Derivation are the foundational KDRS categories.

They are not intended to prevent future architectural evolution.

A new Relationship Category may be introduced only when:

1. the proposed relationship semantics cannot be correctly represented by an existing category;
2. the new category provides meaningful architectural value;
3. introducing a new category reduces semantic ambiguity rather than creating it;
4. the category has a formally defined purpose;
5. the change passes the applicable ASM Brain architecture governance process.

New categories must not be created merely to accommodate isolated use cases.

The default principle is:

**Reuse an existing category when its semantics are sufficient.**

Category expansion is therefore controlled rather than arbitrary.

---

# 9. Relationship Type

A Relationship Type defines the specific semantic meaning of a relationship.

Examples include:

- depends_on
- related_to
- derived_from
- supported_by
- contradicted_by
- classified_by

A Relationship Type is not an individual relationship between two governed objects.

It is a reusable semantic definition.

For example:

`depends_on`

means that the source object has a material dependency on the target object according to the defined semantics of that Relationship Type.

A Relationship Type is a governed vocabulary definition.

A Relationship Assertion is a governed instance of that definition.

A Relationship Type must never be interpreted as evidence that any specific relationship exists.

---

# 10. Relationship Type Governance

Relationship Types must use a controlled vocabulary.

Arbitrary relationship names should not be created freely by:

- individual authors
- content editors
- applications
- AI systems
- Experience Layer systems

A Relationship Type must have an approved semantic definition before it becomes part of the authoritative relationship vocabulary.

The controlled vocabulary provides:

- consistency
- semantic clarity
- machine interpretability
- reusable relationships
- reliable querying
- impact analysis
- governance

---

# 11. Relationship Assertion

A Relationship Assertion states that a specific relationship exists between specific governed objects.

Conceptually:

Source Object
+
Relationship Type
+
Target Object
=
Relationship Assertion

For example:

Knowledge Asset A
+
depends_on
+
Evidence Claim B
=
Relationship Assertion

The assertion is a specific governed claim within the Knowledge System.

A Relationship Assertion instantiates the semantics defined by a Relationship Type.

The existence of a Relationship Type alone does not establish any Relationship Assertion.

---

# 12. Relationship Identifier

A governed Relationship Assertion that requires independent governance should have a Relationship Identifier.

The Relationship Identifier uniquely identifies that specific Relationship Assertion.

Conceptually:

Relationship Category
↓
Relationship Type
↓
Relationship Assertion
↓
Relationship Identifier

The identifier belongs to the Relationship Assertion.

It is not an independent Knowledge Asset or separate knowledge object.

A Relationship Identifier allows the system to:

- audit a relationship
- track its history
- attach provenance
- record validation
- determine relationship status
- identify changes
- preserve historical context
- distinguish individual relationship assertions

The exact technical identifier format is outside the scope of this standard.

---

# 13. Minimum Relationship Assertion Model

A governed Relationship Assertion should conceptually contain, or be capable of resolving, the following minimum information:

- Relationship Identifier
- Source Object
- Relationship Type
- Target Object
- Status
- Provenance
- Governance Information

These elements define the minimum conceptual contract.

This is not a database schema.

The technical representation may vary by implementation.

---

# 14. Governance Information

Governance Information records information necessary to establish and maintain the validity of a Relationship Assertion.

Depending on the Relationship Type and governance requirements, this may include:

- validation state
- validator or reviewer
- validation date
- governance authority
- supersession information
- invalidation information
- relevant review history

Not every Relationship Assertion requires identical governance metadata.

Requirements should be determined according to the semantics and significance of the Relationship Type.

---

# 15. Relationship Identifier Does Not Create Authority

A Relationship Identifier exists to identify and govern a relationship.

It does not create authority over either connected object.

Therefore:

Relationship Identifier
�
Knowledge Authority

and:

Relationship
�
Authority Transfer

Authority remains governed by the relevant Knowledge System standards.

---

# 16. Relationship Hierarchy

The canonical hierarchy is:

Relationship Category
↓
Relationship Type
↓
Relationship Assertion
↓
Relationship Identifier

For example:

Dependency
↓
depends_on
↓
Knowledge Asset A → Evidence Claim B
↓
Relationship Identifier

This hierarchy must be preserved across future implementations.

A Relationship Identifier identifies the assertion.

A Relationship Type defines its meaning.

A Relationship Category groups related Relationship Types.

---

# 17. Directional Relationships

Relationships should be directional where their meaning depends on source and target.

The basic structure is:

Source
──relationship──>
Target

For example:

Knowledge Asset A
──depends_on──>
Knowledge Asset B

is not necessarily equivalent to:

Knowledge Asset B
──depends_on──>
Knowledge Asset A

Direction therefore forms part of relationship semantics.

---

# 18. Inverse Relationships

Some relationships may have meaningful inverse interpretations.

For example:

Knowledge Asset A
──depends_on──>
Evidence Claim B

may be viewed inversely as:

Evidence Claim B
──supports──>
Knowledge Asset A

The system may maintain inverse relationships where this improves semantic clarity and queryability.

However, inverse relationships must not create contradictory or duplicated meaning.

The authoritative Relationship Type definition must determine whether an inverse relationship exists.

---

# 19. Dependency Relationships

A dependency relationship exists when the validity, interpretation, operation, or governance of one knowledge object materially depends on another object.

Conceptually:

Object A
──depends_on──>
Object B

Examples may include:

Knowledge Asset
──depends_on──>
Evidence Claim

Knowledge Claim
──depends_on──>
Medical Concept

Knowledge Asset
──depends_on──>
Guideline

Dependency indicates that a meaningful change to the target may require reassessment of the source.

---

# 20. Dependency Principle

A dependency should only be declared when the relationship has material significance.

Not every relationship is a dependency.

For example:

Knowledge Asset A
──related_to──>
Knowledge Asset B

does not automatically mean:

Knowledge Asset A
──depends_on──>
Knowledge Asset B

This distinction prevents the dependency graph from becoming noisy and unreliable.

---

# 21. Dependency Impact

The primary architectural value of dependency relationships is impact analysis.

Conceptually:

Dependency Target Changes
↓
Identify Dependents
↓
Assess Impact
↓
Identify Affected Knowledge
↓
Trigger Lifecycle Review

For example:

Evidence Claim
↓
changes
↓
Knowledge Claim
↓
affects
↓
Knowledge Asset
↓
KLS Reassessment

This provides a controlled pathway between knowledge change and lifecycle governance.

---

# 22. Association Relationships

An association represents a meaningful relationship between knowledge objects without necessarily implying dependency.

Examples may include:

- related_to
- associated_with
- contrasts_with
- commonly_coexists_with

An association answers:

**How are these objects meaningfully connected?**

It does not necessarily answer:

**What object depends on what other object?**

---

# 23. Association Does Not Imply Dependency

The system must not infer dependency merely because an association exists.

For example:

Diabetes
──associated_with──>
Obesity

does not automatically mean:

Diabetes
──depends_on──>
Obesity

Similarly:

Hypertension
──related_to──>
Cardiovascular Disease

does not automatically mean that one Knowledge Asset is dependent on the other.

Relationship semantics must remain explicit.

---

# 24. Derivation Relationships

A derivation relationship represents the origin or transformation of knowledge from another governed object.

Conceptually:

Source Knowledge
↓
derived_from
↓
Derived Knowledge

Examples may include:

Evidence Synthesis
──derived_from──>
Evidence Claims

Knowledge Claim
──derived_from──>
Evidence Synthesis

Knowledge Asset
──derived_from──>
Knowledge Claims

Derivation relationships are particularly important for provenance.

---

# 25. Dependency vs Derivation

Dependency and derivation are distinct.

A derived object may continue to depend on its source.

However:

**derived_from = origin relationship**

while:

**depends_on = ongoing material dependency**

For example:

Knowledge Claim
──derived_from──>
Evidence Synthesis

and:

Knowledge Claim
──depends_on──>
Evidence Synthesis

may both be valid when the semantics require both.

The two relationships should not be collapsed into one generic relationship.

---

# 26. Relationship Semantics

Every controlled Relationship Type should have a defined semantic meaning.

At minimum, the definition should establish:

- relationship name
- relationship category
- direction
- semantic meaning
- permitted source types
- permitted target types
- whether inverse representation is applicable
- whether the relationship implies dependency
- whether provenance is required
- whether lifecycle impact is possible

The exact registry format will be defined in a future specification.

---

# 27. Relationship Source and Target

Every directional Relationship Assertion should identify:

- Source Object
- Relationship Type
- Target Object

The source and target must be identifiable governed objects.

The system must avoid ambiguous relationships such as:

Object A
↓
related
↓
Object B

without defining what "related" means.

---

# 28. Permitted Object Types

Relationships may eventually connect different governed knowledge object types.

Examples include:

- Knowledge Assets
- Knowledge Claims
- Evidence Claims
- Evidence Bodies
- Evidence Syntheses
- Medical Concepts
- Taxonomy Entities
- Guidelines
- Sources
- Other governed knowledge objects

The exact object-type matrix should be defined separately from the relationship architecture.

KDRS provides the conceptual framework.

---

# 29. Knowledge Asset Relationships

Knowledge Assets may have relationships to:

- evidence
- other Knowledge Assets
- medical concepts
- taxonomy entities
- guidelines
- sources
- dependencies
- derived knowledge

Examples:

Knowledge Asset
──supported_by──>
Evidence

Knowledge Asset
──classified_by──>
Medical Taxonomy Entity

Knowledge Asset
──related_to──>
Knowledge Asset

Knowledge Asset
──depends_on──>
Knowledge Asset

These relationships should use governed semantics.

---

# 30. Evidence Relationships

Evidence relationships must remain compatible with the Evidence Standard.

Examples include:

Knowledge Claim
──supported_by──>
Evidence Claim

Evidence Synthesis
──derived_from──>
Evidence Claims

Knowledge Asset
──supported_by──>
Evidence Synthesis

KDRS does not redefine evidence methodology.

It defines the relationship architecture through which evidence objects connect to other governed knowledge objects.

---

# 31. Taxonomy Relationships

Medical taxonomy relationships are governed primarily by the Medical Taxonomy Standard.

KDRS must not replace taxonomy semantics.

For example:

Knowledge Asset
──classified_by──>
Medical Concept

is different from:

Medical Concept A
──broader_than──>
Medical Concept B

The first is a Knowledge System relationship.

The second is a taxonomy relationship.

KDRS must respect the authority of MTS for taxonomy semantics.

---

# 32. Lifecycle Relationships

Knowledge relationships must remain compatible with the Knowledge Lifecycle Standard.

A relationship may influence lifecycle governance.

For example:

Evidence Claim
↓
changes
↓
Knowledge Asset dependency
↓
KLS reassessment

However, a relationship change does not automatically imply a lifecycle transition.

The relationship change must first be evaluated according to applicable governance rules.

---

# 33. Relationship Change vs Lifecycle Change

These are distinct events.

Relationship Change:

Knowledge Asset A
──depends_on──>
Evidence B

becomes:

Knowledge Asset A
──depends_on──>
Evidence C

Lifecycle Change:

Monitoring
↓
Update Required

A relationship change may trigger a lifecycle reassessment, but the two events must not be treated as identical.

---

# 34. Relationship Assertion Governance

Relationship Assertions require governance appropriate to their significance.

A controlled governance model is:

Candidate
↓
Validated
↓
Active

Additional states may include:

Deprecated
Retired
Invalidated

These states apply to Relationship Assertions, not to Knowledge Assets.

A relationship may become invalid while both connected Knowledge Assets remain valid.

---

# 35. Candidate Relationship

A Candidate Relationship is a proposed relationship that has not yet achieved the required validation status.

Candidates may originate from:

- human knowledge engineering
- evidence review
- taxonomy work
- automated analysis
- AI-assisted analysis
- dependency analysis

A Candidate Relationship must not automatically be treated as authoritative.

---

# 36. Validated Relationship

A Validated Relationship has undergone the required governance or review for its Relationship Type.

Validation confirms that:

- the source is valid
- the target is valid
- the Relationship Type is appropriate
- the relationship semantics are satisfied
- required evidence or provenance exists
- applicable governance requirements are satisfied

Validation does not necessarily mean the relationship can never change.

---

# 37. Active Relationship

An Active Relationship is a currently valid Relationship Assertion within the Knowledge System.

Active means the relationship is presently recognized as valid for its intended scope.

It does not mean:

- permanent
- universally applicable
- medically authoritative in isolation
- immune to future reassessment

An Active Relationship remains subject to Knowledge System governance.

---

# 38. Deprecated Relationship

A Deprecated Relationship is a relationship that should no longer be used for new knowledge but may need to remain available for historical context.

Deprecation may occur because:

- relationship semantics changed
- a better relationship replaced it
- governance rules changed
- the relationship is no longer preferred

Deprecated does not necessarily mean historically false.

---

# 39. Retired Relationship

A Retired Relationship is no longer active and should no longer participate in current knowledge interpretation.

Its historical record may remain preserved.

Retirement is different from silent deletion.

---

# 40. Invalidated Relationship

An Invalidated Relationship is a relationship that has been determined not to be valid.

Examples include:

- incorrect assertion
- incorrect source-target pairing
- unsupported semantic interpretation
- erroneous AI-generated relationship
- superseded interpretation where the original relationship is no longer valid

Invalidation must not automatically invalidate either connected object.

The invalidated relationship remains traceable where historical governance requires it.

---

# 41. Relationship Authority

Relationships must have an identifiable authority appropriate to their semantics.

Depending on the Relationship Type, authority may come from:

- Knowledge Engineering
- Evidence Governance
- Medical Taxonomy Governance
- Knowledge Lifecycle Governance
- Medical Review
- other formally authorized governance processes

AI-generated relationships must not automatically become authoritative relationships.

---

# 42. KDRS Authority Boundary

KDRS governs the architecture and structural semantics of relationships between governed knowledge objects.

KDRS does not override the domain authority of another ASM Brain standard.

The standard responsible for the connected knowledge domain retains authority over the substantive meaning and governance of that domain.

For example:

- MTS governs medical taxonomy semantics.
- ES governs evidence semantics and evidence governance.
- KLS governs lifecycle decisions.
- KEF governs knowledge engineering processes.
- KAS governs Knowledge Asset identity and structure.

KDRS governs how these governed objects are related.

Therefore:

**KDRS relationship architecture**
�
**domain authority of connected knowledge objects**

This boundary must remain explicit across future implementations.

---

# 43. No Authority Transfer

A relationship does not create, transfer, or elevate authority.

For example:

Knowledge Asset A
──supported_by──>
Evidence B

does not mean that the relationship itself makes Evidence B authoritative.

Likewise:

Knowledge Asset A
──related_to──>
Knowledge Asset B

does not make B authoritative over A.

Authority remains governed by the applicable Knowledge System standard and lifecycle state of each object.

Therefore:

Relationship
�
Authority

and:

Relationship
�
Authority Transfer

---

# 44. Relationship Provenance

Some relationships require provenance.

Examples may include:

- supported_by
- derived_from
- depends_on
- contradicted_by
- validated_by

Where a relationship represents a substantive knowledge assertion, its provenance should be traceable.

Provenance may identify:

- source
- evidence
- author
- reviewer
- method
- date
- governing process

The exact provenance model remains governed by KAS, ES, and future governance specifications.

---

# 45. Relationship Validation and AI

AI may assist in identifying Candidate Relationships.

Examples include:

- discovering likely dependencies
- detecting possible associations
- suggesting evidence support
- identifying derivation paths
- detecting possible contradictions
- identifying impacted Knowledge Assets

The architecture must preserve the distinction:

AI Candidate Relationship
�
Validated Relationship
�
Active Relationship

Where governance requires validation:

AI Suggestion
↓
Candidate
↓
Review
↓
Validation
↓
Active

AI must not silently create authoritative medical relationships.

---

# 46. Inferred Relationship Boundary

A relationship may sometimes be inferred from existing knowledge or relationship paths.

For example:

A
──depends_on──>
B

and:

B
──supports──>
C

may allow a system to identify A and C as potentially connected.

However, an inferred connection does not automatically establish a new authoritative Relationship Assertion.

The rule is:

**Inference may support discovery, analysis, recommendation, or impact assessment.**

It does not automatically create:

- a Validated Relationship
- an Active Relationship
- an authoritative medical relationship

An inferred relationship must undergo the applicable governance process before becoming an Active Relationship Assertion.

Therefore:

Inferred Relationship
�
Authoritative Relationship

This rule applies regardless of whether the inference is generated by:

- AI
- graph traversal
- rules
- search
- statistical analysis
- human reasoning

---

# 47. Relationship Integrity

A Relationship Assertion should only become Active when:

1. The source object exists.
2. The target object exists.
3. The Relationship Type is valid.
4. The source type is permitted.
5. The target type is permitted.
6. The relationship direction is valid.
7. Required governance conditions are satisfied.
8. Required provenance exists where applicable.
9. The assertion has achieved the required validation state.

Invalid relationships must not become authoritative knowledge.

---

# 48. Orphan Relationships

A relationship must not remain Active when its source or target no longer exists as a valid governed object.

If an object is:

- superseded
- archived
- withdrawn
- invalidated

the relationships involving that object may require reassessment.

Historical relationships may remain preserved for provenance.

Current Active Relationships must reflect current governance.

---

# 49. Relationship Versioning

Material changes to Relationship Assertions or Relationship Type semantics should be historically traceable.

For example:

Relationship Assertion v1
↓
Relationship Assertion v2

rather than silently overwriting a materially different assertion.

Likewise, changes to a Relationship Type definition must be governed separately from changes to individual assertions.

The exact technical implementation is outside the scope of this standard.

---

# 50. Material Change

A material change is a change that may reasonably affect the:

- meaning
- validity
- interpretation
- applicability
- dependency

represented by a Relationship Assertion.

A change should be treated as material when it may alter the semantic basis on which the relationship is considered valid.

Materiality is therefore determined by relationship meaning and context rather than by the size of a textual or technical change.

Examples may include:

- a change in the evidence conclusion underlying a support relationship
- a change in the medical concept to which an asset is classified
- a change in a guideline that materially alters a dependency
- a change in a Knowledge Asset that removes or introduces a substantive dependency

Not every change to an object is material to every relationship.

---

# 51. Referenced Object Version Changes

A material version change to a source or target object may affect the validity of a Relationship Assertion.

Therefore:

Referenced Object Version Changes
↓
Relationship Reassessment
↓
Determine Current Validity

The reassessment may result in:

- relationship remains valid
- relationship is updated
- relationship is invalidated
- relationship requires further review

A version change must not automatically invalidate every relationship.

Likewise, a version change must not automatically preserve every relationship.

The effect depends on the semantics and materiality of the change.

---

# 52. Source Version Changes

When the source object changes materially, its outgoing relationships may require reassessment.

Example:

Knowledge Asset v1
──depends_on──>
Evidence Claim v1

becomes:

Knowledge Asset v2
──depends_on──>
Evidence Claim v1

The relationship must be evaluated to determine whether the dependency remains valid for v2.

---

# 53. Target Version Changes

When the target object changes materially, incoming relationships may require reassessment.

Example:

Knowledge Asset v1
──depends_on──>
Evidence Claim v1

becomes:

Knowledge Asset v1
──depends_on──>
Evidence Claim v2

The system must determine whether the relationship remains valid for the new target version.

This is particularly important for evidence and guideline dependencies.

---

# 54. Version Reassessment Principle

The principle is:

Version Change
�
Automatic Relationship Invalidation

and:

Version Change
�
Automatic Relationship Preservation

Instead:

Version Change
↓
Materiality Assessment
↓
Relationship Reassessment
↓
Governed Decision

This prevents unnecessary relationship churn while preserving integrity.

---

# 55. Relationship Type Change vs Assertion Change

These are distinct.

Relationship Type Change:

depends_on
↓
semantic definition revised

Relationship Assertion Change:

Asset A
──depends_on──>
Evidence B

becomes:

Asset A
──depends_on──>
Evidence C

The first changes the meaning or governance of the Relationship Type.

The second changes an individual Relationship Assertion.

Both must be governed appropriately.

---

# 56. Relationship Deletion

Relationships should generally be retired or invalidated rather than silently deleted when they have historical significance.

For example:

Old Relationship
↓
No Longer Valid
↓
Retired / Invalidated

The historical record should remain available where required.

This supports auditability and provenance.

---

# 57. Object Deletion and Historical Relationship Preservation

Deletion, retirement, supersession, withdrawal, or invalidation of a governed object must not silently erase historically significant Relationship Assertions.

Where a relationship is relevant to:

- provenance
- auditability
- historical interpretation
- lifecycle interpretation
- dependency analysis
- governance history

the historical Relationship Assertion should remain traceable even when the connected object is no longer active.

Therefore:

Object Retirement
↓
Relationship Assessment
↓
Preserve Historical Relationship Where Required

Current validity and historical traceability are separate concerns.

An inactive object may therefore continue to have historically significant relationships without those relationships being considered Active current relationships.

---

# 58. Contradictory Relationships

The system must allow for the possibility that governed knowledge objects may have relationships that represent disagreement or contradiction.

For example:

Knowledge Claim A
──contradicted_by──>
Evidence Claim B

Contradictory relationships must not be treated as system errors merely because they disagree.

They represent a knowledge condition requiring governance and interpretation.

The Evidence Standard and Knowledge Engineering Framework govern how conflicting evidence is assessed.

---

# 59. Relationship Confidence

KDRS does not require a generic numerical confidence score for every relationship.

Confidence should not be added merely because it appears useful.

Where confidence or certainty is required, it should be defined according to the semantics of the specific Relationship Type and governed by the relevant standard.

This prevents a meaningless universal "confidence" field from becoming a substitute for evidence quality.

---

# 60. Relationship Inclusion Principle

Not every discoverable relationship should become a governed Relationship Assertion.

A relationship should be recorded as a governed Relationship Assertion only when it provides meaningful value such as:

- semantic value
- dependency value
- provenance value
- governance value
- retrieval value
- impact-analysis value

The existence of a technically detectable connection is not sufficient justification for recording it as an authoritative relationship.

This principle is particularly important for AI-assisted relationship discovery.

AI systems may identify a large number of possible relationships.

The Knowledge System should prefer:

**meaningful governed relationships**

over:

**maximum relationship volume**

---

# 61. Relationship Density

The system should avoid creating relationships merely for completeness.

A high number of weak relationships can reduce rather than increase knowledge quality.

Therefore:

Meaningful Relationship
>
Maximum Number of Relationships

Relationship creation should prioritize:

- semantic value
- dependency significance
- provenance
- impact usefulness
- governance relevance

Relationship Inclusion Principle must be applied before Candidate Relationships become governed relationships.

---

# 62. Relationship Reusability

Controlled Relationship Types should be reusable across the Knowledge System.

For example:

`supported_by`

may be used consistently across appropriate governed object types.

This enables:

- consistent search
- impact analysis
- reporting
- AI reasoning
- knowledge traversal
- governance

Relationship semantics should therefore remain stable and documented.

---

# 63. Relationship Vocabulary Governance

The controlled Relationship Vocabulary should itself be governed.

A future Relationship Registry may define:

- Relationship Type ID
- Relationship Name
- Category
- Definition
- Direction
- Allowed Source Types
- Allowed Target Types
- Inverse Relationship
- Dependency Implication
- Provenance Requirement
- Lifecycle Impact
- Status

The registry is a future implementation/governance artifact.

KDRS establishes the requirement for controlled relationship semantics.

---

# 64. Relationship Graph Concept

The Knowledge System may conceptually be represented as a graph.

Nodes:

Knowledge Objects

Edges:

Governed Relationship Assertions

Conceptually:

Evidence
↓
supports
↓
Knowledge Claim
↓
belongs_to
↓
Knowledge Asset
↓
classified_by
↓
Medical Concept

The graph is a conceptual architecture.

KDRS does not mandate a graph database.

---

# 65. Knowledge Graph Principle

The purpose of a knowledge graph within ASM Brain is not merely to connect objects.

It is to represent meaningful semantic relationships that can support:

- knowledge discovery
- dependency analysis
- impact analysis
- provenance
- governance
- AI reasoning
- structured retrieval

The graph must therefore be semantically governed.

---

# 66. Relationship Traversal

Future systems may traverse relationships to answer questions such as:

- What evidence supports this Knowledge Asset?
- Which Knowledge Assets depend on this evidence?
- Which medical concepts classify this knowledge?
- What knowledge would be affected if this source changes?
- Which Knowledge Assets are related to this concept?
- What knowledge was derived from this evidence?

KDRS establishes the conceptual foundation for these capabilities.

---

# 67. Relationship Impact Propagation

KDRS establishes the architecture for impact propagation.

The conceptual flow is:

Change
↓
Affected Relationship
↓
Dependent Objects
↓
Affected Knowledge
↓
Lifecycle Reassessment

Impact propagation should support both direct and indirect dependencies.

For example:

Evidence Source
↓
Evidence Claim
↓
Knowledge Claim
↓
Knowledge Asset
↓
Experience Layer Output

A change at the source may therefore have downstream consequences.

---

# 68. Direct Dependency

A direct dependency exists when one object explicitly depends on another.

Example:

Knowledge Claim A
──depends_on──>
Evidence Claim B

The dependency can be traced directly.

---

# 69. Indirect Dependency

An indirect dependency exists when dependency is propagated through multiple governed relationships.

Example:

Evidence Source
↓
Evidence Claim
↓
Knowledge Claim
↓
Knowledge Asset

The Knowledge Asset may therefore be indirectly affected by a change to the Evidence Source.

Indirect impact must be evaluated carefully.

The existence of a graph path does not automatically mean that every downstream object requires revision.

Impact must be governed by Relationship Type semantics and change significance.

---

# 70. Impact Is Not Automatically Revision

A critical architectural principle is:

Relationship Impact
�
Automatic Revision

Instead:

Change Detected
↓
Impact Analysis
↓
Governance Assessment
↓
Decision
↓
No Action
or
Monitoring
or
Update Required
or
Restriction / Withdrawal

This prevents excessive automated churn.

---

# 71. Relationship Impact and KLS

KDRS provides the dependency information.

KLS provides the lifecycle response.

The relationship is:

KDRS
↓
Dependency Detection
↓
Impact Analysis
↓
Affected Knowledge Asset
↓
KLS
↓
Lifecycle Decision

Possible outcomes include:

- No lifecycle change
- Continue Monitoring
- Update Required
- Controlled Revision
- Publication Restriction
- Withdrawal
- Supersession

KDRS does not make the lifecycle decision itself.

---

# 72. Relationship Impact and ES

The Evidence Standard governs evidence quality and status.

KDRS provides the connection between evidence and dependent knowledge.

Therefore:

ES
↓
Evidence Change
↓
KDRS
↓
Dependency Impact
↓
KLS

This creates a governed pathway from evidence change to knowledge lifecycle reassessment.

---

# 73. Relationship Impact and MTS

Medical taxonomy changes may affect Knowledge Assets.

Conceptually:

MTS
↓
Taxonomy Change
↓
Affected Concepts
↓
KDRS
↓
Affected Knowledge Assets
↓
KLS Reassessment

KDRS provides relationship tracing rather than defining taxonomy semantics.

---

# 74. Relationship Impact and KEF

KEF governs knowledge engineering activities.

When dependency analysis identifies affected knowledge:

KDRS
↓
Affected Knowledge
↓
KEF
↓
Controlled Re-engineering
↓
KLS
↓
Review / Approval / Publication

This creates a controlled feedback loop.

---

# 75. Relationship Impact and KAS

KAS defines the Knowledge Asset.

KDRS defines how the asset connects to other governed objects.

Therefore:

KAS
↓
Knowledge Asset
↓
KDRS
↓
Relationships
↓
Knowledge Network

KDRS must not redefine the Knowledge Asset itself.

---

# 76. Relationship and Experience Layer

Experience Layer outputs may be derived from Knowledge Assets.

However, Experience Layer outputs should not become authoritative relationship nodes unless explicitly governed.

For example:

Knowledge Asset
↓
generates / informs
↓
Web Page

does not mean:

Web Page
↓
becomes
↓
Knowledge Asset

The Knowledge System remains authoritative.

---

# 77. Relationship and Content Generation

A webpage, social post, video, or AI answer may be generated from one or more Knowledge Assets.

The relationship between source knowledge and output may be recorded for provenance.

Conceptually:

Knowledge Asset
↓
generates / informs
↓
Content Output

Such output relationships belong to the broader Knowledge-to-Experience architecture.

They must not redefine the underlying medical knowledge relationship model.

---

# 78. Relationship Authority Across Standards

KDRS must respect the authority boundaries of the existing Knowledge System.

KAS governs:

Knowledge Asset definition and structure.

KEF governs:

Knowledge engineering processes.

MTS governs:

Medical taxonomy semantics.

ES governs:

Evidence semantics and evidence governance.

KLS governs:

Knowledge lifecycle and lifecycle decisions.

KDRS governs:

Relationships between governed knowledge objects.

No standard should silently assume the authority of another.

---

# 79. Relationship and Knowledge Authority

A relationship may connect two authoritative objects without becoming the source of authority itself.

For example:

Evidence Claim
──supports──>
Knowledge Claim

The Evidence Claim derives its authority from the Evidence Standard and its governing evidence process.

The Knowledge Claim derives its authority from the applicable knowledge engineering and review process.

The relationship merely represents the governed connection.

---

# 80. Relationship Integrity Across Versions

When a Knowledge Asset is revised, relationships must be evaluated for continued validity.

For example:

Knowledge Asset v1
──depends_on──>
Evidence Claim A

After revision:

Knowledge Asset v2
──depends_on──>
Evidence Claim B

The previous relationship must remain historically traceable.

The current version must expose the relationships relevant to its current governed state.

---

# 81. Relationship Change and Supersession

When a Knowledge Asset is superseded, relationships must preserve historical context.

Example:

Knowledge Asset v1
──supported_by──>
Evidence A

v1 becomes:

Superseded

while:

Knowledge Asset v2
──supported_by──>
Evidence B

The system should preserve both historical relationship structures where required.

---

# 82. Relationship Change and Archival

Archived Knowledge Assets may retain their historical relationships.

Historical graph:

Archived Asset
↓
Historical Evidence
↓
Historical Relationship

should remain distinguishable from:

Current Asset
↓
Current Evidence
↓
Current Relationship

This prevents historical knowledge from contaminating current knowledge interpretation.

---

# 83. Relationship Governance Rules

The following rules apply:

1. Relationships must use controlled semantics.
2. Relationship Categories must provide broad semantic classification.
3. Relationship Types must define specific semantic meaning.
4. Relationship Assertions must apply Relationship Types to actual governed objects.
5. Governed Relationship Assertions must have independent Relationship Identifiers where required.
6. A Relationship Identifier identifies the assertion and is not a separate knowledge object.
7. A Relationship Type is a reusable semantic definition and does not itself establish a specific relationship.
8. A Relationship Assertion is a governed instance of a Relationship Type between a source and target object.
9. Direction must be explicit where direction affects meaning.
10. Dependency must be distinguished from association.
11. Derivation must be distinguished from dependency.
12. Relationship meaning must be explicit.
13. Material relationships must be traceable.
14. Dependency enables impact analysis.
15. Impact does not automatically mean revision.
16. Relationship changes and lifecycle changes are distinct.
17. Relationship Assertions require appropriate governance.
18. AI may propose relationships but does not automatically establish authority.
19. Inferred relationships do not automatically become authoritative Relationship Assertions.
20. Inferred relationships must undergo applicable governance before becoming Active.
21. Relationships do not create or transfer authority.
22. KDRS does not override the domain authority of KAS, KEF, MTS, ES, or KLS.
23. Historical relationships must remain traceable where required.
24. Taxonomy relationships remain governed by MTS.
25. Evidence relationships remain governed by ES.
26. Lifecycle consequences remain governed by KLS.
27. Knowledge engineering consequences remain governed by KEF.
28. KAS remains authoritative for the Knowledge Asset itself.
29. Experience Layer outputs do not become authoritative knowledge automatically.
30. The knowledge graph is conceptual and technology-independent.
31. Relationship quality is more important than relationship quantity.
32. Relationship governance must prevent arbitrary semantic links.
33. Relationship semantics must remain reusable.
34. Relationship status must reflect current governance.
35. Invalid relationship assertions must not become authoritative current knowledge.
36. Material source or target version changes require relationship reassessment.
37. Version changes do not automatically invalidate or preserve relationships.
38. Relationship Type changes must be governed separately from Relationship Assertion changes.
39. Historical relationship information must be preserved where required.
40. A material change is determined by its potential effect on relationship meaning, validity, interpretation, applicability, or dependency.
41. Not every discoverable relationship should become a governed Relationship Assertion.
42. Relationship inclusion should prioritize meaningful semantic, dependency, provenance, governance, retrieval, or impact-analysis value.
43. New Relationship Categories require formal architecture governance.
44. Existing Relationship Categories should be reused whenever their semantics are sufficient.
45. Deletion, retirement, supersession, withdrawal, or invalidation of an object must not silently erase historically significant relationships.
46. Historical Relationship Assertions must remain traceable where required for provenance, auditability, lifecycle interpretation, or governance history.

---

# 84. Technology Independence

KDRS must remain independent of implementation technology.

It does not prescribe:

- relational database
- graph database
- RDF
- property graph
- Neo4j
- PostgreSQL
- JSON-LD
- API framework
- search engine

Those decisions belong to future engineering architecture.

The semantic relationship model must survive regardless of implementation technology.

---

# 85. Future Extensions

Future specifications may define:

- formal Relationship Registry
- complete Relationship Type vocabulary
- relationship assertion implementation schema
- relationship identifier format
- source/target type matrix
- relationship validation rules
- dependency scoring
- impact propagation algorithms
- graph storage architecture
- relationship APIs
- relationship query language
- automated dependency analysis
- relationship visualization
- relationship audit model
- relationship versioning implementation
- Experience Layer relationship tracking
- controlled inference rules

These are intentionally outside KDRS v1.0.

---

# 86. Design Principles Summary

KDRS is governed by the following principles:

1. Knowledge relationships are semantic knowledge.
2. Relationships use controlled vocabulary.
3. Relationship Categories provide broad semantic grouping.
4. Relationship Types define specific semantic meaning.
5. Relationship Assertions apply semantic meaning to actual objects.
6. A Relationship Type is a reusable semantic definition, not a relationship instance.
7. A Relationship Assertion is a governed instance connecting specific source and target objects.
8. Governed Relationship Assertions have independent identifiers.
9. The Relationship Identifier is not a separate knowledge object.
10. Relationships are directional where meaning requires direction.
11. Dependency is distinct from association.
12. Derivation is distinct from dependency.
13. Relationship meaning must be explicit.
14. Relationships connect governed knowledge objects.
15. Material relationships must be traceable.
16. Dependency enables impact analysis.
17. Impact does not automatically mean revision.
18. Relationship changes and lifecycle changes are distinct.
19. Relationship Assertions require appropriate governance.
20. AI may propose relationships but does not automatically establish authority.
21. Inferred relationships do not automatically become authoritative relationships.
22. Relationships do not create or transfer authority.
23. KDRS does not override domain authority of other Knowledge System standards.
24. Historical relationships must remain traceable where required.
25. Material version changes may require relationship reassessment.
26. Version changes do not automatically invalidate or preserve relationships.
27. Taxonomy relationships remain governed by MTS.
28. Evidence relationships remain governed by ES.
29. Lifecycle consequences remain governed by KLS.
30. Knowledge engineering consequences remain governed by KEF.
31. KAS remains authoritative for the Knowledge Asset itself.
32. Experience Layer outputs do not become authoritative knowledge automatically.
33. The knowledge graph is conceptual and technology-independent.
34. Relationship quality is more important than relationship quantity.
35. Relationship governance must prevent arbitrary semantic links.
36. Relationship semantics must remain reusable.
37. Relationship status must reflect current governance.
38. Invalid relationship assertions must not become authoritative current knowledge.
39. Material change must be assessed according to relationship semantics and context.
40. Relationship inclusion must prioritize meaningful governed value.
41. Relationship Category expansion must be controlled through architecture governance.
42. Historical relationship information must be preserved when required for governance, provenance, auditability, or lifecycle interpretation.
43. Object deletion or retirement must not silently erase historically significant relationships.

---

# 87. Acceptance Criteria

KDRS v1.0 is considered architecturally complete when it:

- defines the purpose of relationship governance
- defines relationship as a governed semantic concept
- establishes Relationship Categories
- establishes controlled Relationship Types
- establishes Relationship Assertions
- explicitly defines Category → Type → Assertion hierarchy
- distinguishes Relationship Types from Relationship Assertions
- establishes Relationship Identifiers
- defines the Relationship Identifier as an identifier of the assertion rather than a separate object
- defines the minimum conceptual Relationship Assertion model
- establishes directional relationships
- distinguishes dependency from association
- distinguishes derivation from dependency
- defines source and target concepts
- establishes relationship semantics
- establishes relationship governance
- establishes relationship assertion governance
- defines Candidate, Validated, and Active relationship states
- defines Deprecated, Retired, and Invalidated relationship handling
- establishes relationship provenance requirements
- establishes dependency impact analysis
- distinguishes direct and indirect dependency
- prevents automatic revision from dependency impact
- establishes the principle that relationships do not transfer authority
- establishes the authority boundary between KDRS and other Knowledge System standards
- defines relationship integrity principles
- addresses contradictory relationships
- addresses relationship versioning
- defines material change
- addresses source version changes
- addresses target version changes
- establishes material version-change reassessment
- establishes inferred relationship boundaries
- prevents inferred relationships from automatically becoming authoritative
- addresses relationship retirement
- addresses relationship invalidation
- establishes relationship inclusion principles
- prevents uncontrolled relationship proliferation
- establishes controlled Relationship Category extension
- establishes AI relationship-generation boundaries
- establishes the conceptual knowledge graph model
- connects dependency impact to KLS
- connects evidence relationships to ES
- connects taxonomy relationships to MTS
- connects knowledge engineering to KEF
- preserves KAS authority
- preserves Experience Layer boundaries
- establishes historical relationship preservation
- addresses object deletion and retirement without silent historical relationship loss
- remains technology-independent
- provides a foundation for future dependency and graph implementation

---

# 88. Status

**Version:** 1.0
**Status:** Release Candidate
**Architecture Stage:** Final Architecture
**Previous Version:** 0.3
**Architecture Review:** Completed
**Review Result:** Approved with four controlled changes integrated
**Next Stage:** Formal Release Review

---

# 89. Change History

| Version | Date | Change | Status |
|---|---|---|---|
| 0.1 | 2026-08-08 | Initial Knowledge Dependency & Relationship architecture | Superseded |
| 0.2 | 2026-08-08 | Added Relationship Identity, Relationship Type vs Assertion distinction, Relationship Assertion Governance, and No Authority Transfer principle | Superseded |
| 0.3 | 2026-08-08 | Replaced Relationship Identity with Relationship Identifier; defined minimum Relationship Assertion model; established Category → Type → Assertion hierarchy; added material version-change reassessment | Superseded |
| 1.0 | 2026-08-08 | Defined Material Change; established Relationship Inclusion Principle; established controlled Relationship Category extension | Superseded |
| 1.0 Final | 2026-08-08 | Clarified authority boundary; strengthened Type vs Assertion separation; established inferred relationship boundary; strengthened historical relationship preservation | Release Candidate |

---

# End of Document
