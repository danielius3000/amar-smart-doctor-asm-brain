# Knowledge Lifecycle Standard

**Document ID:** KLS-001  
**Document Name:** Knowledge Lifecycle Standard  
**Version:** 1.0  
**Status:** Release Candidate  
**Owner:** Amar Smart Doctor  
**System:** ASM Brain  
**Knowledge System:** Amar Smart Doctor Knowledge System  
**Parent Standard:** Knowledge Asset Standard (KAS)  
**Related Standards:** Knowledge Engineering Framework (KEF), Medical Taxonomy Standard (MTS), Evidence Standard (ES)  
**Previous Version:** 0.2  
**Created:** 2026-08-07  

---

# 1. Purpose

The Knowledge Lifecycle Standard (KLS) defines how a Knowledge Asset is created, reviewed, approved, published, monitored, revised, superseded, restricted, withdrawn, and archived within Amar Smart Doctor.

The purpose of KLS is to ensure that medical knowledge is not treated as static content.

Knowledge must exist within a controlled lifecycle that preserves:

- quality
- medical governance
- evidence integrity
- provenance
- version history
- accountability
- publication control
- ongoing monitoring
- controlled change
- safety

KLS therefore establishes the lifecycle architecture governing Knowledge Assets throughout their useful life.

---

# 2. Scope

This standard applies to all governed Knowledge Assets maintained within ASM Brain.

It covers:

- lifecycle states
- lifecycle transitions
- transition triggers
- transition authority
- transition conditions
- approval
- publication
- monitoring
- revision
- publication restriction
- publication withdrawal
- supersession
- archival
- historical preservation
- lifecycle auditability
- evidence-triggered lifecycle changes
- risk-based lifecycle controls
- monitoring and review profiles
- AI participation within lifecycle processes
- separation between knowledge governance and Experience Layer deployment

This standard does not define:

- the detailed structure of a Knowledge Asset
- the complete knowledge engineering process
- medical taxonomy
- evidence assessment methodology
- website publishing workflows
- editorial calendars
- software development workflows
- database implementation
- API implementation
- AI model architecture
- Experience Layer deployment architecture

Those responsibilities belong to other standards or implementation specifications.

---

# 3. Architectural Position

The Knowledge Lifecycle Standard is one component of the Amar Smart Doctor Knowledge System.

The relationship between the major standards is:

Knowledge Asset Standard
        ↓
Defines what a Knowledge Asset is
        ↓
Knowledge Engineering Framework
        ↓
Defines how knowledge is engineered
        ↓
Medical Taxonomy Standard
        ↓
Defines how medical knowledge is classified
        ↓
Evidence Standard
        ↓
Defines how evidence is governed
        ↓
Knowledge Lifecycle Standard
        ↓
Defines how knowledge is governed throughout its life

Together these standards establish the foundation for structured medical knowledge within ASM Brain.

---

# 4. Core Principle

A Knowledge Asset is not a one-time publication.

It is a governed knowledge object with a lifecycle.

The conceptual lifecycle is:

Create
  ↓
Review
  ↓
Approve
  ↓
Publish
  ↓
Monitor
  ↓
Revise when required
  ↓
Republish
  ↓
Eventually supersede or archive

The lifecycle must therefore support both:

1. controlled creation
2. controlled change

---

# 5. Authoritative Lifecycle State

The lifecycle state recorded for a Knowledge Asset is the authoritative representation of its current governance condition.

The authoritative lifecycle state belongs to the Knowledge System.

Publication availability, workflow status, review activity, operational processing status, or Experience Layer deployment status must not independently redefine the Knowledge Asset's lifecycle state.

The governing principle is:

Knowledge System
    ↓
Authoritative Lifecycle State

while:

Workflow
    ↓
Operational Activity

and:

Experience Layer
    ↓
Publication / Deployment State

remain separate concerns.

This separation prevents external systems or operational processes from silently changing the governance status of a Knowledge Asset.

---

# 6. Lifecycle and Workflow Separation

Lifecycle state and workflow activity are separate concepts.

## 6.1 Lifecycle State

A lifecycle state describes the authoritative current governance condition of a Knowledge Asset.

Examples include:

- Draft
- In Review
- Approved
- Published
- Monitoring
- Update Required
- Superseded
- Archived

A lifecycle state answers:

> What is the current governed condition of this Knowledge Asset?

---

## 6.2 Workflow

A workflow describes activities performed to create, evaluate, modify, publish, monitor, or govern a Knowledge Asset.

Examples include:

- evidence review
- knowledge extraction
- knowledge structuring
- medical review
- technical validation
- change assessment
- publication preparation
- evidence monitoring
- guideline monitoring
- safety monitoring

A workflow answers:

> What work is currently being performed in relation to this Knowledge Asset?

---

## 6.3 Architectural Rule

Lifecycle states must not become a catalogue of every operational task.

The distinction is:

Lifecycle State
=
Current governed condition

Workflow
=
Activities performed within or between states

Therefore:

Monitoring State
    ↓
May contain or trigger
    ↓
Evidence Monitoring Workflow
Guideline Monitoring Workflow
Safety Monitoring Workflow
Review Workflow

This preserves the separation between lifecycle architecture and operational workflow.

---

# 7. Lifecycle State Model

The core lifecycle states are:

1. Draft
2. In Review
3. Approved
4. Published
5. Monitoring
6. Update Required
7. Superseded
8. Archived

These states represent the authoritative lifecycle condition of a Knowledge Asset.

The core state model intentionally remains small.

Operational activities must not be unnecessarily converted into lifecycle states.

---

# 8. Lifecycle State Definitions

## 8.1 Draft

A Knowledge Asset is in Draft when it is being created, substantially revised, or otherwise prepared for governance review.

A Draft Knowledge Asset:

- is not approved for public use
- must not be treated as authoritative production knowledge
- may contain incomplete information
- may contain unresolved evidence or structural issues
- remains subject to the applicable Knowledge Engineering Framework

Possible activities include:

- evidence intake
- evidence assessment
- knowledge extraction
- knowledge structuring
- taxonomy assignment
- claim development
- provenance construction
- internal quality checks

A Draft may represent either:

- an initial Knowledge Asset
- a new revision of an existing Knowledge Asset

---

## 8.2 In Review

A Knowledge Asset enters In Review when it has reached the required stage for formal governance assessment.

Review may include:

- evidence review
- knowledge quality review
- medical review
- taxonomy validation
- provenance validation
- safety review
- consistency review

The specific review activities depend on the nature and risk of the Knowledge Asset.

A Knowledge Asset in Review is not yet approved for publication.

---

## 8.3 Approved

A Knowledge Asset enters Approved when it has successfully completed the required governance controls.

Approval means:

> The Knowledge Asset has been authorized as governed knowledge for the intended use and publication context.

Approval does not necessarily mean that the asset is already publicly available.

Approval and publication are separate lifecycle states.

An Approved Knowledge Asset represents an authorized version that may be published through an approved Experience Layer.

---

## 8.4 Published

A Knowledge Asset enters Published when an approved version has been made available through an authorized Experience Layer or other approved consumption mechanism.

Possible consumers include:

- public website
- search system
- AI system
- API
- future mobile applications
- other governed products

Publication must only occur from an Approved Knowledge Asset version.

Publication does not transfer authority from the Knowledge System to the Experience Layer.

The Knowledge Asset within ASM Brain remains the authoritative governed object.

---

## 8.5 Monitoring

A published Knowledge Asset enters the Monitoring state after publication.

Monitoring is a lifecycle state representing the condition in which the Knowledge Asset remains subject to defined monitoring and review controls.

Monitoring is not itself a workflow.

Activities performed while the Knowledge Asset is in Monitoring may include:

- checking new evidence
- checking guideline changes
- checking source retractions
- checking medical consensus changes
- reviewing safety signals
- reviewing user or reviewer feedback
- checking taxonomy changes
- evaluating dependency changes

These are monitoring or review workflows operating within the Monitoring lifecycle state.

The Monitoring state therefore means:

> The Knowledge Asset is currently published and remains under ongoing governance surveillance.

---

## 8.6 Update Required

A Knowledge Asset enters Update Required when a material change has been identified that may affect its validity, safety, accuracy, relevance, or governance status.

Possible triggers include:

- significant new evidence
- evidence retraction
- updated clinical guidance
- identified factual error
- changed medical consensus
- changed safety information
- taxonomy change affecting interpretation
- outdated recommendation
- material source change
- dependency change

Update Required is a governance condition indicating that controlled revision is required.

It does not itself modify the Knowledge Asset.

---

## 8.7 Superseded

A Knowledge Asset or version becomes Superseded when a newer governed Knowledge Asset or version has replaced it as the current representation of the relevant knowledge.

Supersession must preserve:

- historical identity
- previous version
- reason for supersession
- effective date
- successor relationship
- provenance

Superseded knowledge must not be silently deleted.

---

## 8.8 Archived

A Knowledge Asset enters Archived when it is no longer intended to function as current governed knowledge but must be retained for historical, provenance, audit, legal, or organizational purposes.

An Archived Knowledge Asset is not considered current knowledge.

Archival does not imply deletion.

---

# 9. Lifecycle State Characteristics

The following conceptual model applies:

| State | Current Production Knowledge | Publicly Usable | Revision Allowed | Requires Governance |
|---|---|---|---|---|
| Draft | No | No | Yes | Yes |
| In Review | No | No | Controlled | Yes |
| Approved | Yes for authorized use | Not necessarily | Controlled | Yes |
| Published | Yes | Yes, where published | Through revision process | Yes |
| Monitoring | Yes | Yes, unless restricted | Through revision process | Yes |
| Update Required | Potentially affected | Risk-dependent | Yes | Yes |
| Superseded | No | Normally no | Historical only | Yes |
| Archived | No | No | Historical only | Yes |

Publication availability may be temporarily restricted when a risk event requires controlled action.

---

# 10. Lifecycle State and Transition Model

A lifecycle state is not sufficient by itself to govern knowledge.

A controlled lifecycle transition consists of:

1. Current lifecycle state
2. Transition
3. Transition trigger
4. Transition conditions
5. Transition authority
6. Resulting lifecycle state
7. Audit record

Conceptually:

Current State
+
Transition Trigger
+
Transition Conditions
+
Authorized Authority
+
Required Validation
+
Audit Record
↓
New State

A lifecycle transition must never be treated as an arbitrary status change.

---

# 11. Lifecycle Transition Principles

The following principles apply to all lifecycle transitions:

1. A transition must originate from a valid current state.
2. A transition must have a defined trigger.
3. Required conditions must be satisfied.
4. Appropriate authority must authorize the transition.
5. The resulting state must be explicitly recorded.
6. The transition must be auditable.
7. Failed transitions must not falsely produce the target state.
8. Material lifecycle changes must preserve historical context.
9. AI assistance must not bypass required governance authority.
10. Emergency safety mechanisms may temporarily restrict publication without corrupting the underlying lifecycle history.

---

# 12. Primary Lifecycle Flow

The primary lifecycle is:

Draft
   ↓
In Review
   ↓
Approved
   ↓
Published
   ↓
Monitoring

When material change is identified:

Monitoring
   ↓
Update Required
   ↓
Draft
   ↓
In Review
   ↓
Approved
   ↓
Published
   ↓
Monitoring

This creates a controlled revision loop.

---

# 13. Transition Matrix

The core transition model is:

| Current State | Transition | Target State | General Condition |
|---|---|---|---|
| Draft | Submit for Review | In Review | Required preparation completed |
| In Review | Approve | Approved | Required governance checks passed |
| In Review | Return for Revision | Draft | Review identifies required changes |
| Approved | Publish | Published | Authorized publication initiated |
| Published | Enter Monitoring | Monitoring | Publication completed |
| Monitoring | Require Update | Update Required | Material issue identified |
| Update Required | Begin Revision | Draft | Controlled revision initiated |
| Published | Supersede | Superseded | New governed replacement established |
| Monitoring | Supersede | Superseded | New governed replacement established |
| Superseded | Archive | Archived | Historical retention required |
| Published | Archive | Archived | Governance authorizes retirement |
| Monitoring | Archive | Archived | Governance authorizes retirement |

The transition matrix is conceptual.

Implementation-level permissions and workflow rules will be defined later.

---

# 14. Draft → In Review

A Knowledge Asset may transition from Draft to In Review when the required preparation conditions have been satisfied.

Typical conditions may include:

- required structure is complete
- required metadata exists
- relevant taxonomy assignments exist
- evidence relationships are established
- required claims are defined
- provenance is available
- required internal validation is complete

The transition must be recorded.

---

# 15. In Review → Approved

A Knowledge Asset may transition from In Review to Approved only after the required governance checks have been completed successfully.

Approval requirements may depend on:

- Knowledge Asset type
- medical risk
- evidence strength
- intended use
- publication context
- applicable governance rules

Approval authority must be defined by the applicable governance model.

AI systems must not independently grant medical approval unless an explicitly governed future system authorizes such behavior.

---

# 16. In Review → Draft

A Knowledge Asset may return to Draft when review identifies material changes that must be made before approval.

Typical reasons include:

- insufficient evidence
- unsupported claim
- incorrect taxonomy
- incomplete provenance
- medical review concerns
- safety concerns
- structural defects
- unresolved conflicting evidence

The return must preserve the review history.

---

# 17. Approved → Published

Only an Approved Knowledge Asset may transition to Published.

Publication means the approved asset has been exposed through an authorized Experience Layer.

The publication event should preserve:

- Knowledge Asset identity
- Knowledge Asset version
- publication timestamp
- publication destination
- publishing authority
- applicable configuration
- publication status

Publication must not alter the underlying knowledge without creating an appropriate governed revision.

---

# 18. Knowledge Version vs Experience Layer Deployment State

Knowledge version and Experience Layer deployment state are separate concepts.

A Knowledge Asset may have a current governed version that is not yet deployed to every Experience Layer.

For example:

Knowledge Asset v2
        ↓
Approved

while:

Experience Layer
        ↓
Still serving v1

This may occur during controlled publication or deployment processes.

Therefore:

> A Knowledge Asset's version does not automatically define the deployment state of every Experience Layer.

Similarly:

> An Experience Layer deployment event does not independently change the authoritative lifecycle state of the Knowledge Asset.

The Knowledge System remains authoritative for knowledge identity, version, and lifecycle.

The Experience Layer remains responsible for its own publication and deployment status.

---

# 19. Published → Monitoring

A published Knowledge Asset enters Monitoring after successful publication.

The Monitoring state establishes continuing governance.

The monitoring activities may be:

- scheduled
- event-driven
- evidence-driven
- risk-driven
- manually initiated
- automatically assisted

The monitoring activity itself does not change the lifecycle state unless a governed transition is triggered.

---

# 20. Monitoring as State, Not Workflow

Monitoring must remain architecturally distinct from monitoring activities.

The lifecycle state is:

Monitoring

The workflows may include:

- Evidence Monitoring
- Guideline Monitoring
- Safety Monitoring
- Source Monitoring
- Taxonomy Monitoring
- Dependency Monitoring
- User Feedback Review

Therefore:

Monitoring State
      ↓
Monitoring Workflows
      ↓
Potential Finding
      ↓
Lifecycle Decision

A monitoring workflow may conclude that no action is required.

In that case:

Monitoring
      ↓
Monitoring

A monitoring activity therefore does not automatically create a lifecycle transition.

---

# 21. Monitoring → Update Required

A Knowledge Asset should enter Update Required when monitoring identifies a material issue.

A material issue may include:

- evidence invalidation
- evidence retraction
- important new evidence
- guideline change
- safety warning
- material factual error
- changed clinical consensus
- outdated recommendation
- significant taxonomy change
- dependency change
- other governance-defined trigger

The decision to mark a Knowledge Asset as Update Required must itself be auditable.

---

# 22. Monitoring and Review Profiles

Every Published Knowledge Asset must eventually be associated with an applicable Monitoring / Review Profile.

The profile provides the governance mechanism for determining how the Knowledge Asset should be monitored and reviewed.

A Monitoring / Review Profile may eventually define:

- risk category
- evidence volatility
- monitoring frequency
- formal review frequency
- evidence sensitivity
- escalation requirements
- responsible authority
- review triggers
- applicable safety controls

The exact risk model and profile taxonomy are outside the scope of KLS.

KLS establishes the architectural hook.

Conceptually:

Knowledge Asset
      ↓
Risk / Volatility Profile
      ↓
Monitoring / Review Profile
      ↓
Monitoring Controls
      ↓
Review Schedule / Triggers

A Monitoring / Review Profile may be updated independently of the Knowledge Asset when governance requirements change.

However, material changes affecting the knowledge itself must follow the Knowledge Asset lifecycle.

---

# 23. Review Cadence

Review cadence should be risk-based rather than universally identical.

For example, two Knowledge Assets may have different requirements because of differences in:

- clinical risk
- evidence volatility
- treatment implications
- public impact
- source stability
- emergency relevance

KLS does not prescribe specific review intervals.

The future governance model may define profiles such as:

- high-frequency monitoring
- periodic monitoring
- low-frequency monitoring
- event-triggered monitoring

The important architectural requirement is that review cadence must be governed rather than accidental.

---

# 24. Update Required → Draft

When a Knowledge Asset requires modification, a new revision should be created rather than silently modifying the published version.

Conceptually:

Published Knowledge Asset v1
            ↓
Update Required
            ↓
New Revision
            ↓
Draft v2

The previous version remains historically preserved.

---

# 25. Revision Principle

Knowledge revision must be non-destructive.

The system should preserve:

Version 1
   ↓
Version 2
   ↓
Version 3

rather than:

Version 1
   ↓
overwritten

Each governed version should remain identifiable.

Historical versions may be restricted from normal public use while remaining available for governance and provenance.

---

# 26. Versioning

KLS recognizes versioning as a lifecycle requirement.

The exact versioning syntax may be defined by a separate implementation specification.

At the conceptual level:

- a revision creates a distinguishable version
- material changes must create a new governed version
- minor and major changes may follow different review requirements
- published versions must remain traceable
- historical versions must preserve provenance

Versioning must never be used to conceal substantive changes.

---

# 27. Publication Restriction and Withdrawal

A Published or Monitoring Knowledge Asset may require temporary restriction or withdrawal when continued publication creates unacceptable risk.

Publication restriction or withdrawal is a governance control applied to publication availability.

It is intentionally not defined as a permanent core lifecycle state.

This preserves a lean lifecycle state model while allowing urgent safety intervention.

Conceptually:

Published / Monitoring
        ↓
Risk Event
        ↓
Publication Restriction / Withdrawal
        ↓
Review / Revision
        ↓
Resolution
        ↓
Publication Restored or Knowledge Superseded

A restriction or withdrawal may occur when:

- serious medical error is identified
- major safety concern is discovered
- critical source retraction occurs
- information becomes materially misleading
- governance failure is detected
- other urgent risk conditions are established

The underlying Knowledge Asset lifecycle history must remain intact.

---

# 28. Publication Restriction Is Not Knowledge Deletion

Publication restriction or withdrawal means:

> The Knowledge Asset should not currently be exposed through one or more Experience Layers.

It does not mean:

> The Knowledge Asset no longer exists.

The authoritative knowledge record must remain preserved unless separate retention rules explicitly require otherwise.

---

# 29. Emergency Safety Principle

When an immediate medical safety concern exists, publication availability may be restricted before the complete revision lifecycle is finished.

This allows:

Risk Event
    ↓
Immediate Restriction
    ↓
Formal Review
    ↓
Controlled Resolution

rather than forcing the system to wait for the complete normal revision process before preventing potentially harmful exposure.

Emergency actions must remain auditable.

---

# 30. Supersession

Supersession occurs when a newer Knowledge Asset or version replaces an older one.

Example:

Knowledge Asset A v1
        ↓
Knowledge Asset A v2
        ↓
v1 = Superseded
v2 = Current

Supersession may also occur between distinct Knowledge Assets when one concept or representation replaces another.

The relationship should be explicitly recorded.

---

# 31. Supersession vs Archival

These concepts are different.

## Superseded

Means:

> A newer knowledge representation has replaced this one.

## Archived

Means:

> This knowledge is no longer current or active, but is intentionally retained.

A Knowledge Asset may therefore follow:

Published
   ↓
Superseded
   ↓
Archived

if governance policy requires historical archival after supersession.

---

# 32. Publication Withdrawal

A published Knowledge Asset may require immediate withdrawal where continued publication creates unacceptable risk.

Potential triggers include:

- serious medical error
- major safety concern
- source retraction
- materially misleading information
- governance failure

Withdrawal should be implemented through the Publication Restriction / Withdrawal mechanism defined in this standard.

The system must support controlled withdrawal without destroying historical records.

The exact emergency withdrawal procedure should be defined in future Knowledge Governance and Safety specifications.

---

# 33. Evidence-Triggered Lifecycle Change

The Evidence Standard and Knowledge Lifecycle Standard must remain connected.

A material evidence event may trigger lifecycle reassessment.

Conceptually:

Evidence Source
      ↓
Evidence Claim
      ↓
Evidence Assessment
      ↓
Change Detected
      ↓
Affected Knowledge Claim
      ↓
Affected Knowledge Asset
      ↓
Lifecycle Reassessment

This creates a feedback loop between evidence governance and knowledge governance.

---

# 34. Source Retraction

A source retraction is a particularly important lifecycle trigger.

Example:

Source Retraction
       ↓
Evidence Claim affected
       ↓
Evidence Body affected
       ↓
Evidence Synthesis affected
       ↓
Knowledge Claim affected
       ↓
Knowledge Asset reassessment

The existence of a retracted source must not be silently removed from historical provenance.

The system should preserve the historical relationship while clearly representing the retraction status.

---

# 35. Risk-Based Lifecycle Controls

Not all Knowledge Assets have identical risk profiles.

A Knowledge Asset may require different lifecycle controls depending on:

- medical subject
- potential harm
- intended use
- evidence volatility
- treatment implications
- emergency relevance
- public impact
- regulatory sensitivity

KLS therefore supports risk-based lifecycle governance.

However, KLS does not define the complete medical risk classification system.

That should be established separately if required.

KLS provides the lifecycle mechanism through which such risk classifications can influence:

- review requirements
- approval authority
- monitoring frequency
- update urgency
- publication restrictions

---

# 36. AI Participation

AI may participate in lifecycle activities as an assistant.

Appropriate AI activities may include:

- detecting potentially outdated evidence
- identifying possible contradictions
- finding candidate sources
- comparing versions
- identifying affected Knowledge Assets
- suggesting updates
- drafting revisions
- generating review summaries
- monitoring defined signals

AI must not be treated as the authoritative lifecycle authority by default.

In particular:

AI suggestion
      ≠
Medical approval

and:

AI-generated revision
      ≠
Approved Knowledge

Human governance and formally authorized system controls remain responsible for authoritative lifecycle decisions.

---

# 37. Human Governance

Lifecycle authority must remain attributable.

Important lifecycle decisions should be associated with:

- responsible actor
- role
- timestamp
- decision
- relevant Knowledge Asset
- relevant version
- reason
- supporting evidence where applicable

This creates an auditable governance history.

---

# 38. Auditability

Every material lifecycle transition should be auditable.

A lifecycle audit record should conceptually contain:

- Knowledge Asset ID
- Version
- Previous State
- New State
- Transition
- Trigger
- Actor
- Actor Role
- Timestamp
- Reason
- Supporting Evidence
- Review Reference

The exact technical representation belongs to implementation architecture.

---

# 39. Lifecycle Metadata

A Knowledge Asset should eventually be capable of exposing lifecycle metadata such as:

- lifecycle state
- version
- created date
- last modified date
- approved date
- publication date
- last review date
- next review date where applicable
- superseded date
- archived date
- current/replaced status
- monitoring / review profile
- publication restriction status where applicable
- responsible governance authority

The exact metadata schema is governed by KAS and future implementation specifications.

---

# 40. Relationship with KAS

KAS defines the Knowledge Asset itself.

KLS governs the Asset's lifecycle.

Conceptually:

KAS
 ↓
Knowledge Asset Structure
 ↓
KLS
 ↓
Knowledge Asset Lifecycle

KLS must not redefine the Knowledge Asset model established by KAS.

---

# 41. Relationship with KEF

KEF defines the process through which knowledge is engineered.

KLS defines the governed lifecycle state of the resulting Knowledge Asset.

The relationship is:

KEF
 ↓
Knowledge Engineering
 ↓
Knowledge Asset
 ↓
KLS
 ↓
Lifecycle Governance

KEF and KLS therefore complement each other rather than duplicate each other.

---

# 42. Relationship with MTS

MTS defines how medical concepts are classified and related.

Taxonomy changes may affect Knowledge Assets.

Therefore:

MTS Change
    ↓
Potential Knowledge Impact
    ↓
Lifecycle Reassessment

KLS provides the mechanism for handling that impact.

---

# 43. Relationship with ES

ES governs evidence.

KLS governs the lifecycle of knowledge derived from that evidence.

The relationship is:

Evidence Standard
        ↓
Evidence
        ↓
Knowledge Claim
        ↓
Knowledge Asset
        ↓
Knowledge Lifecycle Standard

Changes in evidence may therefore trigger lifecycle events.

---

# 44. Relationship with Experience Layer

The Experience Layer consumes approved knowledge.

Examples include:

- website
- search
- AI assistant
- mobile applications
- APIs
- future products

The relationship must remain:

Knowledge Asset
      ↓
Approved
      ↓
Published
      ↓
Experience Layer

Experience-layer content must not become the authoritative source of knowledge.

---

# 45. Lifecycle Integrity Principle

The authoritative lifecycle belongs to the Knowledge System.

A webpage being deleted does not mean that the Knowledge Asset has been deleted.

A social media post being published does not mean that the underlying Knowledge Asset has been approved.

An AI response being generated does not mean that new medical knowledge has been created.

Therefore:

Experience Event
      ≠
Knowledge Lifecycle Event

unless explicitly governed as such.

---

# 46. Knowledge System vs Experience Layer Authority

ASM Brain is the authoritative system for:

- Knowledge Asset identity
- Knowledge Asset version
- Knowledge Asset lifecycle state
- knowledge provenance
- governed approval
- historical knowledge record

The Experience Layer is responsible for:

- consuming approved knowledge
- rendering knowledge
- publishing approved knowledge
- deployment of its own technical representation
- managing its own delivery state

The Experience Layer must not independently:

- approve knowledge
- redefine lifecycle state
- overwrite authoritative knowledge
- create authoritative medical claims outside the governed system

This separation is fundamental to the architecture.

---

# 47. Controlled Change Principle

Any material change to an approved Knowledge Asset must pass through the appropriate lifecycle controls.

The system must prevent:

Approved
   ↓
Silent modification

Instead:

Approved Version
      ↓
Controlled Revision
      ↓
Review
      ↓
Approval
      ↓
New Published Version

This protects the integrity of the knowledge record.

---

# 48. Lifecycle Integrity During Failure

If a workflow fails during a transition, the system must not falsely represent the Knowledge Asset as having completed that transition.

For example:

Draft
   ↓
Review Process Failed

must not result in:

Approved

without an actual successful approval event.

Lifecycle state must represent the governed truth of the Knowledge Asset.

---

# 49. Lifecycle and Automation

Automation may assist lifecycle management.

Examples:

- scheduled monitoring
- evidence change detection
- review reminders
- stale knowledge detection
- dependency analysis
- publication synchronization
- audit logging
- impact analysis

Automation must operate within defined lifecycle rules.

Automation must not bypass governance controls.

---

# 50. Lifecycle and Dependencies

A Knowledge Asset may depend on:

- evidence claims
- evidence bodies
- evidence syntheses
- medical concepts
- other Knowledge Assets
- taxonomy entities
- guidelines
- external sources

Changes to dependencies may trigger lifecycle reassessment.

Therefore dependency relationships should eventually support impact analysis.

Example:

Evidence Claim X
      ↓
Knowledge Claim Y
      ↓
Knowledge Asset Z

If Evidence Claim X is materially changed:

X changes
   ↓
Y reassessment
   ↓
Z lifecycle review

---

# 51. Lifecycle Closure

A Knowledge Asset's lifecycle is not complete merely because it has been published.

The lifecycle remains active until the asset is:

- superseded
- archived
- otherwise formally retired

Therefore:

Published
    ↓
Monitoring

is a continuing state of governance.

---

# 52. Transition Governance

Every state transition must have:

1. a defined initiating event
2. defined conditions
3. authorized authority
4. required validation
5. recorded outcome
6. audit trail

This prevents lifecycle state from becoming an informal label.

---

# 53. Non-Destructive Governance

ASM Brain must preserve the history of governed knowledge.

The following principle applies:

> Never destroy historical knowledge merely because current knowledge has changed.

Historical records may be restricted, deprecated, superseded, or archived, but their provenance should remain recoverable where policy permits.

---

# 54. Safety Principle

When uncertainty exists about whether a Knowledge Asset remains safe or valid, the system should favor controlled review over silent continuation.

The lifecycle should therefore support:

Potential Problem
      ↓
Flag
      ↓
Assess
      ↓
Restrict / Withdraw if necessary
      ↓
Review
      ↓
Resolve

This principle is particularly important for medical knowledge with potential patient harm.

---

# 55. Governance Boundary

KLS defines the lifecycle architecture.

It does not define every governance rule.

Future governance specifications may define:

- medical review authority
- risk classification
- emergency withdrawal procedures
- review frequency
- publication authorization
- legal retention
- regulatory requirements
- escalation procedures

KLS provides the framework within which those controls operate.

---

# 56. Implementation Boundary

This standard intentionally does not prescribe:

- programming language
- framework
- database
- graph database
- API architecture
- queue system
- event bus
- workflow engine
- CMS
- deployment platform

Implementation decisions belong to the Platform Engineering phase.

The lifecycle model must remain technology-independent.

---

# 57. Design Principles Summary

The Knowledge Lifecycle Standard is governed by the following principles:

1. Knowledge has a lifecycle.
2. Lifecycle state and workflow are separate.
3. The Knowledge System is authoritative for lifecycle state.
4. Approval and publication are separate.
5. Published knowledge remains monitored.
6. Material changes require controlled revision.
7. Historical versions must be preserved.
8. Supersession is not deletion.
9. Archival is not deletion.
10. Evidence changes can trigger knowledge review.
11. Risk may influence lifecycle controls.
12. Monitoring is a lifecycle state, while monitoring activities remain workflows.
13. Publication restriction and withdrawal are governance controls, not permanent core lifecycle states.
14. Every Published Knowledge Asset has an applicable Monitoring / Review Profile.
15. AI may assist but does not automatically become the authority.
16. Lifecycle transitions must be auditable.
17. Experience-layer outputs do not become the source of truth.
18. Knowledge version and Experience Layer deployment state are separate concepts.
19. Lifecycle governance must remain technology-independent.
20. Medical safety takes precedence over publication convenience.
21. Material changes must be non-destructive and historically traceable.
22. Lifecycle state must always represent the governed truth of the Knowledge Asset.
23. Experience Layer deployment must not independently redefine Knowledge Asset governance.
24. Lifecycle architecture must remain lean and avoid unnecessary states.

---

# 58. Future Extensions

The following may be defined in future specifications:

- formal risk classification model
- Monitoring / Review Profile taxonomy
- detailed transition permissions
- lifecycle event model
- lifecycle API specification
- database representation
- automated monitoring architecture
- dependency impact analysis
- knowledge expiration rules
- regulatory retention rules
- emergency withdrawal procedure
- lifecycle dashboard
- governance reporting
- lifecycle notification system
- Experience Layer deployment synchronization
- publication-state management

These are intentionally outside the scope of KLS v1.0.

---

# 59. Acceptance Criteria

KLS v1.0 is considered complete when it:

- defines the purpose of Knowledge Lifecycle governance
- distinguishes lifecycle from workflow
- establishes the Knowledge System as the authoritative lifecycle authority
- defines the major lifecycle states
- formally distinguishes states from transitions
- defines transition triggers conceptually
- defines transition conditions conceptually
- defines transition authority conceptually
- separates approval from publication
- establishes monitoring as a lifecycle state
- keeps monitoring activities as workflows
- establishes controlled revision
- establishes publication restriction and withdrawal controls
- preserves historical versions
- distinguishes supersession from archival
- connects evidence changes to lifecycle reassessment
- establishes a Monitoring / Review Profile hook
- provides risk-based lifecycle hooks
- defines AI participation boundaries
- establishes auditability requirements
- distinguishes Knowledge Asset version from Experience Layer deployment state
- defines the authority boundary between Knowledge System and Experience Layer
- defines relationships with KAS, KEF, MTS and ES
- maintains technology independence
- avoids unnecessary lifecycle states
- preserves non-destructive knowledge history
- provides a foundation for future implementation architecture

---

# 60. Release Status

**Version:** 1.0  
**Status:** Release Candidate  
**Architecture Decisions:** KLS-01 through KLS-05 locked  
**v0.2 Review Changes:** KLS-REV-01 through KLS-REV-04 incorporated  
**v1.0 Refinements:** KLS-FR-01 and KLS-FR-02 incorporated  
**Next Stage:** Final Architecture Review and Release Approval  

---

# 61. Change History

| Version | Date | Change | Status |
|---|---|---|---|
| 0.1 | 2026-08-07 | Initial Knowledge Lifecycle Standard architecture | Superseded |
| 0.2 | 2026-08-07 | Formalized state/transition model, clarified Monitoring, added publication restriction/withdrawal mechanism, and added Monitoring / Review Profile hook | Superseded |
| 1.0 | 2026-08-07 | Established authoritative lifecycle-state ownership and separated Knowledge Version from Experience Layer deployment state | Release Candidate |

---

# End of Document