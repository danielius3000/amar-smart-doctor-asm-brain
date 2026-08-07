# Evidence Standard

> **Document Status:** Released
> **Version:** 1.0
> **Owner:** Amar Smart Doctor
> **System:** ASM Brain — Knowledge System
> **Document Type:** Knowledge System Standard
> **Milestone:** S1-04.4

---

# 1. Purpose

The Evidence Standard (ES) defines how Amar Smart Doctor identifies, evaluates, records, verifies, synthesizes, cites, and maintains evidence supporting medical knowledge.

The purpose of the Evidence Standard is to establish a trustworthy evidence foundation for the Amar Smart Doctor Knowledge System.

It enables the system to answer:

> **Why should this medical claim be trusted?**

The Evidence Standard provides the rules for connecting medical claims to their supporting evidence while preserving provenance, uncertainty, limitations, contextual boundaries, recommendations, conflicting evidence, and evidence synthesis.

The standard is designed to ensure that:

- medical claims are traceable to supporting evidence
- evidence sources are identifiable
- evidence claims are distinguishable from their source documents
- evidence claim scope is preserved
- evidence quality can be evaluated consistently
- evidence strength is not confused with knowledge confidence
- conflicting evidence is preserved and assessed
- multiple pieces of evidence can be evaluated collectively
- evidence synthesis is distinguishable from individual evidence claims
- evidence claims are distinguishable from recommendations
- citations support specific claims
- evidence remains reviewable over time
- AI does not become the authority for medical truth

---

# 2. Scope

The Evidence Standard governs:

- evidence source identification
- evidence claim identification
- evidence claim scope
- evidence classification
- source credibility
- evidence assessment
- evidence body construction
- evidence synthesis
- evidence strength
- relevance
- applicability
- currency
- consistency
- evidence limitations
- conflicting evidence
- evidence provenance
- citation principles
- evidence verification
- human medical review
- AI-assisted evidence work
- evidence versioning
- evidence lifecycle
- evidence governance
- distinction between evidence and recommendations

The Evidence Standard does not define:

- Knowledge Asset structure
- Knowledge Engineering workflow
- Medical Taxonomy
- Knowledge Asset lifecycle
- website architecture
- SEO architecture
- content writing standards
- database implementation
- API implementation
- AI model architecture
- search engine implementation
- clinical decision-support algorithms

Those responsibilities belong to other components of the Amar Smart Doctor architecture.

---

# 3. Relationship to the Knowledge System

The Evidence Standard is one component of the Amar Smart Doctor Knowledge System.

The major responsibilities are separated as follows.

## Knowledge Asset Standard

Defines:

> What is a Knowledge Asset?

## Knowledge Engineering Framework

Defines:

> How is evidence transformed into governed knowledge?

## Medical Taxonomy Standard

Defines:

> How are medical concepts classified and organized?

## Evidence Standard

Defines:

> How is the evidence supporting knowledge identified, evaluated, synthesized, and governed?

## Knowledge Lifecycle

Defines:

> How does governed knowledge evolve over time?

These standards are complementary.

No standard should silently assume responsibilities belonging to another standard.

---

# 4. Core Principle

The central principle of the Evidence Standard is:

> **Medical knowledge should be traceable to identifiable evidence that has been appropriately evaluated for quality, relevance, applicability, currency, and consistency.**

Evidence provides support for knowledge.

Evidence does not automatically become knowledge.

Similarly:

> **AI-generated information is not evidence merely because an AI system produced it.**

---

# 5. Evidence Architecture

The evidence architecture is:

    Evidence Source
           ↓
    Evidence Claim
           ↓
    Evidence Claim Scope
           ↓
    Evidence Assessment
           ↓
    Evidence Body
           ↓
    Evidence Synthesis
           ↓
    Knowledge Claim
           ↓
    Knowledge Asset

A more detailed representation is:

    Evidence Source
           │
           ├── Source Metadata
           ├── Source Type
           ├── Publisher
           ├── Publication Date
           ├── Version
           └── Citation Information
                    │
                    ▼
             Evidence Claim
                    │
                    ├── Claim
                    ├── Population
                    ├── Condition / Context
                    ├── Intervention / Exposure
                    ├── Comparator
                    ├── Outcome
                    ├── Timeframe
                    ├── Setting
                    └── Limitations
                    │
                    ▼
            Evidence Assessment
                    │
                    ▼
              Evidence Body
                    │
                    ├── Evidence Claim A
                    ├── Evidence Claim B
                    ├── Evidence Claim C
                    └── Evidence Claim D
                    │
                    ▼
            Evidence Synthesis
                    │
                    ├── Supporting Findings
                    ├── Contradictory Findings
                    ├── Evidence Gaps
                    ├── Limitations
                    └── Overall Interpretation
                    │
                    ▼
              Knowledge Claim
                    │
                    ▼
              Knowledge Asset

Recommendations remain a distinct concept:

    Evidence Body
           ↓
    Evidence Synthesis
           ↓
    Knowledge Claim
           ↓
    Recommendation Claim
           ↓
    Governance / Review

Evidence does not automatically become a recommendation.

---

# 6. Evidence Source

An Evidence Source is an identifiable external or internal source from which evidence or medical claims are obtained.

Examples include:

- clinical practice guidelines
- systematic reviews
- meta-analyses
- randomized controlled trials
- observational studies
- government health publications
- recognized professional organizations
- academic publications
- medical reference resources
- regulatory authorities
- institutional evidence resources

An Evidence Source is not itself a Knowledge Asset.

A single Evidence Source may support many Evidence Claims.

---

# 7. Evidence Source Identity

Every Evidence Source should be uniquely identifiable.

Where available, source identity should include:

- title
- author or organization
- publication
- publisher
- publication date
- version
- identifier
- DOI or equivalent identifier
- URL or persistent location
- access date where relevant

The exact technical representation will be defined during implementation.

The principle is:

> **A reviewer should be able to identify the original source from the stored evidence record.**

---

# 8. Evidence Source Types

The Evidence Standard should support classification of Evidence Sources by type.

Initial source types include:

1. Clinical Practice Guideline
2. Systematic Review
3. Meta-analysis
4. Randomized Controlled Trial
5. Cohort Study
6. Case-Control Study
7. Cross-Sectional Study
8. Case Series
9. Case Report
10. Diagnostic Study
11. Qualitative Research
12. Government / Public Health Publication
13. Professional Organization Publication
14. Regulatory / Official Publication
15. Medical Reference Source
16. Expert Consensus
17. Other Controlled Source

This list is an initial architecture baseline.

It may be expanded through governance.

---

# 9. Evidence Claim

An Evidence Claim is a specific medical proposition extracted from or supported by an Evidence Source.

This distinction is fundamental.

One source may contain many claims.

For example:

    Evidence Source
          ↓
    Clinical Guideline
          │
          ├── Claim A
          ├── Claim B
          ├── Claim C
          └── Claim D

Therefore:

> **Evidence Source and Evidence Claim must remain separate concepts.**

---

# 10. Claim-Level Evidence

Where practical, evidence should be attached to the specific claim it supports rather than only to a general document or Knowledge Asset.

For example:

    Knowledge Claim:
    "Condition X is associated with Y."

should be linked to:

    Evidence Claim:
    "Study / guideline reports an association between X and Y."

which is linked to:

    Evidence Source:
    Original publication.

This allows reviewers to understand exactly what the source supports.

---

# 11. Evidence Claim Scope

An Evidence Claim must preserve the contextual boundaries necessary for correct interpretation.

Evidence should not be generalized beyond the population, condition, intervention, comparator, outcome, timeframe, or setting actually supported by the source.

The conceptual scope model is:

    Evidence Claim
          │
          ├── Population
          ├── Condition / Context
          ├── Intervention / Exposure
          ├── Comparator
          ├── Outcome
          ├── Timeframe
          └── Setting

Not every Evidence Claim will require every element.

The principle is:

> **The evidence record must preserve the contextual boundaries necessary to interpret the claim correctly.**

This prevents a valid finding from being transformed into an unsupported universal statement.

---

# 12. Population

Population describes who or what the evidence applies to.

Where relevant, this may include:

- age group
- sex
- demographic characteristics
- disease status
- disease severity
- risk group
- clinical characteristics
- inclusion criteria
- exclusion criteria

Population boundaries should be preserved when they materially affect interpretation.

---

# 13. Condition / Context

Condition / Context describes the medical condition, exposure, clinical situation, or circumstance to which the evidence applies.

Examples include:

- specific disease
- symptom
- risk state
- pregnancy
- postoperative state
- chronic condition
- acute condition
- screening context
- diagnostic context

The evidence should not be detached from the condition or context that gives the claim meaning.

---

# 14. Intervention / Exposure

Where relevant, the Evidence Claim should identify the intervention, treatment, diagnostic approach, exposure, or other factor being evaluated.

Examples include:

- medication
- procedure
- surgery
- lifestyle intervention
- diagnostic test
- environmental exposure
- behavioral intervention

The exact nature of the intervention or exposure should be preserved when it affects interpretation.

---

# 15. Comparator

Where relevant, the Evidence Claim should preserve the comparator used by the source.

Examples include:

- placebo
- standard care
- no treatment
- another treatment
- another diagnostic method
- baseline condition
- control population

A treatment effect cannot always be interpreted correctly without understanding what it was compared against.

---

# 16. Outcome

The outcome represents what was measured or observed.

Examples include:

- mortality
- symptom improvement
- disease progression
- diagnostic accuracy
- adverse events
- quality of life
- laboratory outcome
- hospitalization

Outcomes should preserve relevant measurement definitions where necessary.

---

# 17. Timeframe

The timeframe describes the relevant period associated with the Evidence Claim.

This may include:

- study duration
- follow-up period
- treatment period
- observation period
- publication period
- guideline validity period

Timeframe may materially affect interpretation.

For example, short-term improvement does not automatically establish long-term benefit.

---

# 18. Setting

Setting describes the context in which the evidence was generated or intended to apply.

Examples include:

- primary care
- hospital
- specialist care
- community setting
- laboratory setting
- geographic region
- healthcare system

Setting should be preserved where it affects applicability.

---

# 19. Evidence Claim Context

An Evidence Claim should be interpreted within its appropriate context.

Where relevant, the evidence record should preserve:

- population
- condition
- intervention or exposure
- comparator
- outcome
- timeframe
- setting
- study limitations

The purpose is to prevent a claim from being interpreted more broadly than the underlying evidence permits.

---

# 20. Evidence Assessment

Evidence Assessment evaluates how suitable an Evidence Claim is for supporting a Knowledge Claim.

The initial assessment model is multidimensional.

The principal dimensions are:

- methodological quality
- relevance
- applicability
- currency
- consistency
- transparency
- limitations
- independence where relevant

No single dimension should automatically determine the overall assessment in every situation.

---

# 21. Methodological Quality

Methodological Quality evaluates the quality of the methods used to produce the evidence.

Considerations may include:

- study design
- study methodology
- sample size
- risk of bias
- measurement quality
- statistical methods
- control methods
- study limitations
- reporting transparency

The appropriate assessment method may differ according to source type.

For example, the criteria appropriate for evaluating a randomized controlled trial may differ from those appropriate for evaluating a clinical guideline.

---

# 22. Relevance

Relevance evaluates whether the evidence directly addresses the Knowledge Claim being considered.

High relevance means:

> The evidence directly addresses the question or claim.

Lower relevance may occur when:

- the evidence addresses a related but different condition
- the population differs substantially
- the outcome differs
- the intervention differs
- the evidence addresses a different clinical question

Evidence should not be treated as directly supporting a claim merely because the subjects are broadly related.

---

# 23. Applicability

Applicability evaluates whether the evidence can reasonably be applied to the intended context.

Factors may include:

- population
- geography
- healthcare setting
- disease severity
- intervention availability
- demographic characteristics
- clinical context

A study can be methodologically strong but have limited applicability to a specific population.

Therefore:

> **Methodological strength and practical applicability are separate considerations.**

---

# 24. Currency

Currency evaluates how current the evidence is relative to the Knowledge Claim.

Currency should consider:

- publication date
- guideline update date
- known changes in medical understanding
- newer evidence
- current clinical practice
- regulatory changes

Currency must not be interpreted as:

> Newer = automatically better.

Older evidence may remain highly important.

The purpose of currency assessment is to determine whether newer information materially changes the interpretation of the evidence.

---

# 25. Consistency

Consistency evaluates whether different credible sources generally support similar conclusions.

For example:

    Evidence A → supports Claim
    Evidence B → supports Claim
    Evidence C → supports Claim

may indicate greater consistency.

Conversely:

    Evidence A → supports Claim
    Evidence B → contradicts Claim
    Evidence C → uncertain

indicates evidence conflict and requires additional assessment.

Consistency is one dimension of evidence assessment and should not be treated as proof by itself.

---

# 26. Transparency

Evidence assessment should consider whether the source provides sufficient information to understand:

- how the evidence was produced
- how conclusions were reached
- limitations
- methodology
- conflicts of interest where disclosed

Greater transparency generally improves the ability to evaluate evidence.

---

# 27. Independence

Where relevant, evidence assessment should consider potential conflicts of interest, sponsorship, funding, or other factors that may affect interpretation.

This does not mean:

> Industry-funded = invalid.

Nor does it mean:

> Independently funded = automatically correct.

The purpose is to preserve relevant context for evidence evaluation.

---

# 28. Evidence Limitations

Evidence records should preserve important limitations.

Examples include:

- small sample size
- short follow-up
- high risk of bias
- limited population
- observational design
- indirect evidence
- incomplete data
- inconsistent findings

Limitations should not be hidden merely because they make a Knowledge Asset more difficult to write.

A trustworthy knowledge system preserves uncertainty.

---

# 29. Evidence Body

An Evidence Body is a structured collection of relevant Evidence Claims considered together when assessing support for a Knowledge Claim.

A Knowledge Claim will often require more than one Evidence Claim.

For example:

    Knowledge Claim
          ↓
      Evidence Body
          │
          ├── Evidence Claim A
          ├── Evidence Claim B
          ├── Evidence Claim C
          └── Evidence Claim D

The Evidence Body provides the working evidence set for a particular Knowledge Claim.

An Evidence Body may contain:

- supporting evidence
- contradictory evidence
- neutral or uncertain evidence
- evidence of different study types
- evidence from different populations
- evidence from different time periods

The Evidence Body should preserve these differences rather than treating all evidence as identical.

---

# 30. Evidence Body Scope

An Evidence Body should be constructed around a defined Knowledge Claim or evidence question.

The scope should be sufficiently clear to determine:

- which Evidence Claims belong in the body
- which Evidence Claims are outside the body
- why the selected evidence is relevant
- whether important contradictory evidence has been considered

The Evidence Body should not become an uncontrolled collection of references.

The principle is:

> **Evidence is assembled for a defined knowledge question, not merely accumulated.**

---

# 31. Evidence Body Composition

An Evidence Body may contain Evidence Claims from multiple Evidence Sources.

For example:

    Evidence Body
        │
        ├── Guideline Claim
        ├── Systematic Review Claim
        ├── RCT Claim
        ├── Cohort Claim
        └── Safety Evidence Claim

Different evidence types may answer different aspects of the same Knowledge Claim.

The system should preserve the identity and characteristics of each Evidence Claim within the Evidence Body.

---

# 32. Evidence Body Completeness

An Evidence Body should be evaluated for reasonable completeness.

This does not mean every available publication must be included.

Instead, the reviewer should consider whether important evidence has been omitted.

Potential omissions include:

- major contradictory studies
- important recent guidelines
- major safety evidence
- relevant systematic reviews
- important population-specific evidence

Completeness requirements should be proportionate to the importance and risk of the Knowledge Claim.

---

# 33. Evidence Synthesis

Evidence Synthesis is the governed interpretation of an Evidence Body used to determine how strongly the available evidence supports a Knowledge Claim.

Evidence Synthesis is not simply a summary of the Evidence Claims.

It should consider:

- supporting findings
- contradictory findings
- evidence quality
- relevance
- applicability
- currency
- consistency
- limitations
- evidence gaps
- population differences
- methodological differences
- overall interpretation

Conceptually:

    Evidence Body
          ↓
    Evidence Synthesis
          ↓
    Evidence Strength
          ↓
    Knowledge Claim

---

# 34. Evidence Synthesis vs Evidence Claim

An Evidence Claim describes what a particular source reports or supports.

Evidence Synthesis evaluates the body of evidence collectively.

For example:

    Evidence Claim A:
    Study A reports benefit.

    Evidence Claim B:
    Study B reports no significant difference.

    Evidence Claim C:
    Study C reports benefit in a specific population.

These claims are not themselves the synthesis.

The synthesis may conclude:

    "Available evidence suggests a possible benefit,
    but findings are inconsistent and applicability
    to the broader population is uncertain."

Therefore:

> **Evidence Claim and Evidence Synthesis must remain separate concepts.**

---

# 35. Evidence Synthesis and Conflicting Evidence

Evidence Synthesis must explicitly account for meaningful conflicting evidence.

For example:

    Evidence Body
        │
        ├── Study A → Supports
        ├── Study B → Supports
        ├── Study C → Contradicts
        └── Study D → Uncertain
                ↓
        Evidence Synthesis
                ↓
        Current Interpretation

The synthesis should explain, where appropriate:

- why findings differ
- whether differences are clinically important
- whether populations differ
- whether methodologies differ
- whether newer evidence changes interpretation
- whether uncertainty remains

---

# 36. Evidence Synthesis and Evidence Strength

Evidence Strength represents the strength of support provided by the Evidence Body after appropriate assessment and synthesis.

Conceptually:

    Evidence Claims
          ↓
    Evidence Assessments
          ↓
      Evidence Body
          ↓
    Evidence Synthesis
          ↓
    Evidence Strength

Evidence Strength should therefore reflect the total evidence picture rather than simply the strongest individual source.

---

# 37. Evidence Strength

Evidence Strength represents the overall strength of support provided by available evidence for a particular Knowledge Claim.

Evidence Strength should not be reduced to a universal hierarchy based solely on study type.

For example:

    RCT
    ↓
    automatically strongest

is an oversimplification.

The strength of evidence depends on:

- research question
- study design
- methodological quality
- relevance
- applicability
- consistency
- limitations
- total evidence body
- evidence synthesis

Evidence Strength should therefore be determined through structured assessment.

---

# 38. Evidence Strength and Knowledge Confidence

Evidence Strength and Knowledge Confidence are separate concepts.

### Evidence Strength

Describes:

> How strongly does the available evidence support the claim?

### Knowledge Confidence

Describes:

> How confident is Amar Smart Doctor that the governed Knowledge Claim is sufficiently supported for its intended use?

They may be related but are not identical.

For example:

    Strong Evidence
    +
    Poor applicability
    =
    Potentially lower Knowledge Confidence

Likewise:

    Moderate Evidence
    +
    High relevance
    +
    High consistency
    +
    Appropriate applicability
    =
    Potentially useful Knowledge Confidence

The final confidence model will be defined through governance and validated against real Knowledge Assets.

---

# 39. Conflicting Evidence

Medical evidence may conflict.

The Evidence Standard must preserve such conflicts rather than silently eliminating them.

For example:

    Evidence A ── supports ── Claim

    Evidence B ── contradicts ── Claim

    Evidence C ── provides uncertainty

The system should preserve these relationships.

Conflict assessment should consider:

- study quality
- relevance
- population differences
- methodology
- publication date
- outcome differences
- statistical uncertainty
- subsequent evidence
- clinical context

---

# 40. Current Interpretation of Conflicting Evidence

When evidence conflicts, the system may establish a current interpretation after appropriate assessment and synthesis.

The interpretation should preserve:

- supporting evidence
- contradictory evidence
- uncertainty
- limitations
- reasoning
- review status

The system must not conceal meaningful disagreement simply to produce a cleaner answer.

---

# 41. Evidence Provenance

Evidence Provenance records the origin and chain of support for knowledge.

The preferred conceptual chain is:

    Knowledge Asset
          ↓
    Knowledge Claim
          ↓
    Evidence Synthesis
          ↓
    Evidence Body
          ↓
    Evidence Claim
          ↓
    Evidence Source
          ↓
    Original Publication / Source

Where appropriate, provenance should also record:

- who extracted the claim
- when it was extracted
- how it was assessed
- who reviewed it
- when it was reviewed
- what version of the source was used
- how the Evidence Body was constructed
- who performed or approved the Evidence Synthesis

---

# 42. Provenance Principle

The core provenance principle is:

> **A significant medical claim should be traceable to the evidence supporting it and to the reasoning used to synthesize that evidence.**

The level of traceability should be proportionate to the importance and risk of the claim.

High-risk or clinically significant claims should receive stronger provenance requirements.

---

# 43. Citation Policy

Citations should support specific medical claims wherever practical.

A citation should allow a reviewer to identify:

- the source
- the relevant evidence
- the publication
- the version or date where applicable

Citation quality should be evaluated based on:

- accuracy
- relevance
- completeness
- traceability
- source reliability

A bibliography without claim-level traceability should not automatically be considered sufficient evidence governance.

---

# 44. Citation Completeness

Important medical claims should not remain unsupported when credible evidence is reasonably available.

Citation completeness should consider:

- claim importance
- medical risk
- evidence availability
- source quality
- uncertainty

Not every sentence requires a citation.

However, significant medical assertions should have appropriate supporting evidence.

---

# 45. Citation Verification

Citations should be verified before a Knowledge Asset reaches an approved state.

Verification should establish, where practical:

1. The cited source exists.
2. The source is correctly identified.
3. The source actually supports the Evidence Claim.
4. The Evidence Claim has not been materially distorted.
5. Important limitations have not been omitted.
6. The citation remains accessible or otherwise identifiable.

AI may assist with citation verification.

AI verification alone does not constitute final medical approval.

---

# 46. Evidence Verification

Evidence verification evaluates whether an Evidence Claim has been accurately extracted and interpreted.

Verification should consider:

- source identity
- claim accuracy
- context
- interpretation
- population
- intervention or exposure
- comparator
- outcome
- timeframe
- setting
- limitations
- citation accuracy

The objective is to prevent:

    source says X

from becoming:

    source proves Y

when the source does not actually support Y.

---

# 47. Evidence Claim vs Recommendation Claim

Evidence Claims and Recommendation Claims are distinct concepts.

An Evidence Claim describes what the evidence reports, observes, estimates, or supports.

A Recommendation Claim expresses what should be considered, done, avoided, or preferred under a defined context.

For example:

    Evidence Claim:
    Treatment X reduces outcome Y in population Z.

    Recommendation Claim:
    Treatment X should be considered for population Z under condition Q.

The recommendation may require additional considerations beyond the evidence itself.

These may include:

- benefits
- harms
- certainty of evidence
- patient preferences
- resource considerations
- feasibility
- clinical context
- professional judgment
- guideline methodology

Therefore:

> **Evidence Claim does not automatically become Recommendation Claim.**

---

# 48. Recommendation Provenance

Where a Recommendation Claim is based on evidence, the recommendation should preserve its relationship to the supporting evidence.

Conceptually:

    Recommendation Claim
          ↓
    Supporting Knowledge Claim
          ↓
    Evidence Synthesis
          ↓
    Evidence Body
          ↓
    Evidence Claims
          ↓
    Evidence Sources

The recommendation must not be represented as if the underlying Evidence Source directly stated the recommendation unless the source actually contains that recommendation.

This distinction prevents:

> "The study recommends X"

when the study merely provides evidence relevant to X.

---

# 49. Recommendation Authority

A Recommendation Claim may have additional authority requirements.

For example, a recommendation may originate from:

- clinical practice guideline
- professional organization
- regulatory authority
- institutional protocol
- evidence-informed governance process

The authority of the recommendation should be distinguishable from the strength of the underlying evidence.

A guideline recommendation may be authoritative while still explicitly acknowledging low or moderate certainty of evidence.

---

# 50. Human Medical Review

Human medical review is required where appropriate for medically significant Knowledge Claims and Recommendation Claims.

Medical review may assess:

- clinical interpretation
- evidence sufficiency
- evidence synthesis
- evidence conflicts
- applicability
- safety
- uncertainty
- claim wording
- recommendation wording
- appropriate limitations

The exact review requirements will depend on the Knowledge Lifecycle and risk classification.

---

# 51. AI-Assisted Evidence Work

AI may assist with evidence-related tasks.

Permitted assistance may include:

- literature discovery
- source identification
- evidence extraction
- claim extraction
- terminology normalization
- source comparison
- conflict detection
- citation suggestions
- evidence summarization
- evidence synthesis assistance
- evidence gap identification
- recommendation-source comparison

AI must not be treated as the authoritative evidence source.

The governing principle is:

> **AI may accelerate evidence work; it does not establish medical truth.**

---

# 52. AI-Assisted Evidence Synthesis

AI may assist in constructing or analyzing an Evidence Body.

It may:

- group related Evidence Claims
- identify supporting findings
- identify contradictory findings
- compare study populations
- identify methodological differences
- detect evidence gaps
- propose a draft synthesis
- identify claims requiring human review

However:

> **AI-generated Evidence Synthesis is a draft analytical artifact until appropriately reviewed.**

AI must not silently resolve conflicting evidence or manufacture consensus.

---

# 53. AI-Generated Claims

An AI-generated statement is not automatically an Evidence Claim.

AI output may become part of the evidence workflow only when its underlying source can be independently identified and verified.

For example:

    AI says:
    "Study X found Y."

is not sufficient.

The system should identify:

    Study X
       ↓
    Original Source
       ↓
    Evidence Claim
       ↓
    Verification

Only then may the claim enter the governed evidence workflow.

---

# 54. AI-Generated Recommendations

AI-generated recommendations require an additional boundary.

An AI system may propose:

    "Treatment X may be considered."

That output is not automatically an approved Recommendation Claim.

The recommendation must be evaluated against:

- supporting evidence
- applicable guidelines
- clinical context
- safety considerations
- recommendation authority
- human governance requirements

AI may assist in constructing or comparing recommendations.

AI does not independently authorize medical recommendations.

---

# 55. Evidence Hierarchy

The Evidence Standard does not establish a single universal hierarchy in which one study type is always superior to every other source.

Different evidence types answer different questions.

For example:

- randomized trials may be highly informative for intervention effectiveness
- diagnostic studies may be appropriate for diagnostic accuracy
- cohort studies may be useful for prognosis or risk
- systematic reviews may synthesize multiple studies
- clinical guidelines may provide evidence-informed recommendations
- regulatory sources may be authoritative for approved indications or safety information

Evidence Strength must therefore be determined in context.

---

# 56. Source Authority

Source authority should be considered separately from evidence quality.

Examples of authoritative source categories may include:

- government health agencies
- recognized medical organizations
- peer-reviewed journals
- established academic institutions
- regulatory authorities

Authority alone does not eliminate the need for evidence assessment.

A highly authoritative source may still contain:

- outdated information
- limited applicability
- uncertainty
- evolving recommendations

---

# 57. Source Selection Principles

When multiple sources are available, evidence selection should prioritize:

1. Relevance
2. Appropriate authority
3. Methodological quality
4. Applicability
5. Currency
6. Consistency
7. Transparency

The precise priority may depend on the clinical question.

Source selection should avoid relying unnecessarily on:

- unsourced websites
- anonymous content
- low-quality summaries
- AI-generated references
- secondary content when a reliable primary source is available

---

# 58. Evidence Freshness and Monitoring

Evidence should be monitored for meaningful changes.

Potential triggers include:

- new clinical guidelines
- major systematic reviews
- important randomized trials
- regulatory changes
- safety warnings
- major changes in clinical consensus

Evidence monitoring should support the Knowledge Lifecycle.

The Evidence Standard defines the evidence requirements.

The Knowledge Lifecycle determines what happens to affected Knowledge Assets.

---

# 59. Evidence Versioning

Evidence records should preserve source versions where relevant.

For example:

    Guideline v1
         ↓
    Guideline v2
         ↓
    Updated Recommendation

The system should avoid overwriting historical evidence in a way that destroys provenance.

Where a new source materially changes a Knowledge Claim, the Knowledge Asset should enter the appropriate review process.

---

# 60. Evidence Deprecation

Evidence may become unsuitable for current use because it is:

- withdrawn
- superseded
- materially contradicted
- obsolete
- retracted
- replaced by authoritative guidance

Deprecated evidence should not necessarily be deleted.

Historical provenance may remain important.

The system should distinguish:

    Historical Evidence
          ≠
    Current Preferred Evidence

---

# 61. Retracted Evidence

Retracted publications require special handling.

Where an Evidence Source has been retracted:

- the retraction should be recorded
- affected Evidence Claims should be identified
- affected Evidence Bodies should be identified
- affected Evidence Syntheses should be reviewed
- dependent Knowledge Claims should be reviewed
- affected Knowledge Assets should enter the appropriate lifecycle process

A retracted source should not continue to function as trusted supporting evidence.

---

# 62. Evidence Gaps

The Evidence System should be able to identify evidence gaps.

An evidence gap exists when:

- a claim lacks adequate support
- available evidence is weak
- evidence is contradictory
- evidence is outdated
- applicability is uncertain
- reliable sources cannot be found

Evidence gaps should not automatically be filled with AI-generated assumptions.

Instead:

    Evidence Gap
         ↓
    Uncertainty / Review
         ↓
    Research Requirement

---

# 63. Uncertainty

The Evidence Standard must preserve uncertainty.

Where evidence does not support a definitive conclusion, the Knowledge System should allow the resulting Knowledge Claim to express appropriate uncertainty.

Examples include:

- evidence is limited
- evidence is inconsistent
- evidence is indirect
- evidence is emerging
- evidence is insufficient

The system should not manufacture certainty merely because a definitive answer is easier to publish.

---

# 64. Evidence and Medical Safety

Evidence governance is particularly important for claims involving:

- diagnosis
- treatment
- medication
- dosage
- contraindications
- adverse effects
- emergency conditions
- pregnancy
- children
- vulnerable populations

Higher-risk claims should receive stronger evidence and review requirements.

Detailed risk classification belongs to the broader Knowledge Governance and Lifecycle architecture.

---

# 65. Evidence and Knowledge Assets

A Knowledge Asset may contain multiple Knowledge Claims.

Each significant Knowledge Claim may reference one or more Evidence Bodies.

Each Evidence Body contains relevant Evidence Claims.

Conceptually:

    Knowledge Asset
         │
         ├── Knowledge Claim A
         │       ↓
         │   Evidence Body A
         │       ├── Evidence Claim 1
         │       └── Evidence Claim 2
         │
         ├── Knowledge Claim B
         │       ↓
         │   Evidence Body B
         │       └── Evidence Claim 3
         │
         └── Knowledge Claim C
                 ↓
             Evidence Body C
                 ├── Evidence Claim 4
                 └── Evidence Claim 5

Recommendations remain distinct:

    Knowledge Asset
         │
         ├── Knowledge Claim
         │       ↓
         │   Evidence Body
         │       ↓
         │   Evidence Synthesis
         │
         └── Recommendation Claim
                 ↓
             Governance

This architecture prevents the evidence of one claim from being incorrectly assumed to support every claim in the Knowledge Asset.

---

# 66. Evidence and Medical Taxonomy

Evidence Claims may reference Taxonomy Concepts.

For example:

    Evidence Claim
         ↓
    Polycystic Ovary Syndrome
         ↓
    Medical Taxonomy

This allows evidence to be associated with controlled medical concepts.

However, taxonomy classification does not itself validate the evidence.

MTS organizes concepts.

ES evaluates evidence.

---

# 67. Evidence and Knowledge Engineering Framework

The Evidence Standard provides the evidence rules used by the Knowledge Engineering Framework.

Conceptually:

    Evidence Source
         ↓
    Evidence Claim
         ↓
    Evidence Assessment
         ↓
    Evidence Body
         ↓
    Evidence Synthesis
         ↓
    Knowledge Claim
         ↓
    Knowledge Asset

KEF defines the workflow.

ES defines the evidence requirements within that workflow.

---

# 68. Evidence Lifecycle

Evidence may move through a conceptual lifecycle:

    Discovered
        ↓
    Identified
        ↓
    Extracted
        ↓
    Assessed
        ↓
    Organized into Evidence Body
        ↓
    Synthesized
        ↓
    Verified
        ↓
    Used
        ↓
    Monitored
        ↓
    Updated / Deprecated

This lifecycle is an architectural model.

The detailed operational lifecycle will be coordinated with the Knowledge Lifecycle.

---

# 69. Evidence Governance

Evidence governance should control:

- source acceptance
- evidence classification
- evidence claim scope
- assessment rules
- evidence body construction
- synthesis requirements
- verification requirements
- citation requirements
- conflict handling
- reviewer responsibilities
- evidence updates
- deprecation
- provenance preservation
- recommendation evidence requirements

Governance should be proportionate to medical risk.

---

# 70. Human and AI Responsibility

The Evidence System follows the principle:

    AI
    ↓
    Assistance

    Human Governance
    ↓
    Authority

AI may:

- discover
- extract
- compare
- group evidence
- assist synthesis
- summarize
- identify conflicts
- identify evidence gaps

Humans may:

- review
- validate
- approve
- reject
- resolve significant conflicts
- approve medically significant interpretations
- approve recommendations

The exact division of responsibility will be governed by the broader AI Governance and Knowledge Lifecycle systems.

---

# 71. Technology Independence

Evidence Standard v0.3 is technology-independent.

It does not prescribe:

- database technology
- graph database
- search engine
- API framework
- AI model
- cloud provider
- storage platform

Implementation decisions should occur after the conceptual model has been validated against real Knowledge Assets and evidence examples.

---

# 72. Future Interoperability

The Evidence System should be capable of supporting recognized identifiers and metadata standards where useful.

Potential interoperability mechanisms may include:

- DOI
- PMID
- guideline identifiers
- regulatory identifiers
- structured citation metadata

These are examples rather than mandatory dependencies.

The exact interoperability strategy should be determined during platform engineering.

---

# 73. Evidence Quality Principles

The Evidence System should prioritize:

### Traceability

Claims should be traceable to supporting evidence.

### Accuracy

Evidence should represent the original source faithfully.

### Relevance

Evidence should address the claim being made.

### Applicability

Evidence should be suitable for the intended context.

### Context Preservation

Evidence claims should not be generalized beyond their supported scope.

### Transparency

Important limitations should remain visible.

### Currency

Evidence should be monitored for meaningful changes.

### Consistency

Conflicting evidence should be identified rather than hidden.

### Synthesis

Multiple pieces of evidence should be interpreted collectively where appropriate.

### Proportionality

Higher-risk claims should receive stronger evidence controls.

### Independence

Potential conflicts and sponsorship should be considered where relevant.

### Recommendation Separation

Evidence claims should not be presented as recommendations unless an appropriate recommendation process exists.

### Human Oversight

AI assistance must not replace appropriate medical governance.

---

# 74. Architectural Boundaries

The following boundaries are explicitly maintained.

### Evidence Standard owns:

- evidence concepts
- evidence source definition
- evidence claim definition
- evidence claim scope
- evidence assessment
- evidence body definition
- evidence synthesis definition
- evidence provenance
- evidence verification
- citation principles
- evidence governance
- evidence / recommendation distinction

### KAS owns:

- Knowledge Asset structure

### KEF owns:

- knowledge engineering workflow

### MTS owns:

- medical concept classification

### Knowledge Lifecycle owns:

- Knowledge Asset state transitions

### AI Governance owns:

- AI responsibility and authorization

### Platform Engineering owns:

- technical implementation

This separation prevents architectural duplication.

---

# 75. Acceptance Criteria for v0.3

Evidence Standard v0.3 is considered architecturally complete when:

- [x] Evidence Source and Evidence Claim are separate concepts
- [x] Evidence assessment is multidimensional
- [x] Evidence Strength and Knowledge Confidence are separated
- [x] Conflicting evidence is explicitly represented
- [x] Claim-level provenance is defined
- [x] Evidence Source is defined
- [x] Evidence Claim is defined
- [x] Evidence Claim Scope is explicitly defined
- [x] Population scope is addressed
- [x] Condition / Context scope is addressed
- [x] Intervention / Exposure scope is addressed
- [x] Comparator scope is addressed
- [x] Outcome scope is addressed
- [x] Timeframe scope is addressed
- [x] Setting scope is addressed
- [x] Evidence assessment dimensions are defined
- [x] Evidence limitations are preserved
- [x] Evidence Body is defined
- [x] Evidence Body scope is defined
- [x] Evidence Body composition is addressed
- [x] Evidence Body completeness is addressed
- [x] Evidence Synthesis is defined
- [x] Evidence Synthesis is distinguished from Evidence Claims
- [x] Evidence Synthesis accounts for conflicting evidence
- [x] Evidence Synthesis is connected to Evidence Strength
- [x] Citation principles are defined
- [x] Verification principles are defined
- [x] Evidence Claim and Recommendation Claim are explicitly separated
- [x] Recommendation provenance is defined
- [x] Human medical review boundary is defined
- [x] AI evidence-assistance boundary is defined
- [x] AI-assisted Evidence Synthesis boundary is defined
- [x] AI recommendation boundary is defined
- [x] Evidence freshness is addressed
- [x] Evidence versioning is addressed
- [x] Evidence deprecation is addressed
- [x] Retracted evidence is addressed
- [x] Evidence gaps are addressed
- [x] Uncertainty is preserved
- [x] Relationship to KAS is defined
- [x] Relationship to KEF is defined
- [x] Relationship to MTS is defined
- [x] Technology independence is preserved

---

# 76. Open Decisions for v1.0+

The following decisions should deliberately remain open until the v0.3 architecture is reviewed:

- exact evidence scoring model
- exact evidence strength scale
- exact Knowledge Confidence scale
- formal risk-based evidence requirements
- formal source credibility scoring
- formal conflict-resolution algorithm
- exact citation metadata schema
- evidence database model
- evidence graph model
- external evidence API integrations
- automated evidence monitoring
- automated evidence update detection
- formal Recommendation Claim model
- recommendation strength representation
- recommendation authority model
- detailed medical reviewer workflow
- detailed Evidence Synthesis methodology
- automated evidence synthesis controls
- formal Evidence Body completeness criteria

These should be decided only when sufficient real Knowledge Assets and evidence examples exist to test the architecture.

---

# 77. Document Control

| Field              | Value                        |
| ------------------ | ---------------------------- |
| Document           | Evidence Standard            |
| Short Name         | ES                           |
| Version            | 1.0                          |
| Status             | Released                     |
| Owner              | Amar Smart Doctor            |
| System             | ASM Brain                    |
| Domain             | Knowledge System             |
| Document Type      | Standard                     |
| Milestone          | S1-04.4                      |
| Previous Version   | ES v0.3                      |
| Previous Standards | KAS v1.0, KEF v1.0, MTS v1.0 |

---

# End of Document