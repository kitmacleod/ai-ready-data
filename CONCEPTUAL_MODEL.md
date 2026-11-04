# Conceptual model

**Version:** 0.2.0-working-draft

## 1. Purpose
The model supports transparent assessment of what an environmental data product can safely and efficiently support for a stated AI-enabled use, what evidence supports that conclusion, what cannot yet be determined, and what practical improvements could close important gaps.

## 2. Working definition
**AI-readiness is the relationship between a defined data product and an intended use: the degree to which, and the conditions under which, software and its users can find, obtain, interpret, combine and rely on the data for that use without undue manual intervention, with the data's provenance, quality, uncertainty, rights and material limitations visible.**

AI-readiness particularly concerns situations where software may act at scale or with limited human review, so hidden assumptions and incompatibilities can propagate automatically.

## 3. Assessment target
An assessment MUST identify exactly what is being assessed. A target may be a product, version, resource, variable, station subset, spatial or temporal subset, or access endpoint.

Example:
```yaml
assessment_target:
  product_id: haduk-grid
  product_version: TBD
  variables: [rainfall]
  temporal_frequency: daily
  spatial_resolution: 1km
  resources: []
```

The assessment MUST state the granularity of its conclusions and MUST NOT imply uniform findings across variables, stations or periods not assessed.

## 4. Three assessment levels
### 4.1 Core conformance
Use-independent requirements, wherever applicable.

### 4.2 Use-class conformance
Requirements associated with a broad task or operating mode.

### 4.3 Fitness for a specific use instance
A comparison between explicitly stated use requirements and characteristics or limitations established for the assessment target.

Automation is expected to be stronger at identifying hard mismatches than at proving scientific fitness.

## 5. Candidate dimensions
### D1 Extent, resolution and completeness
Describes spatial, temporal, thematic and population scope; resolution/support; expected versus observed completeness; sampling or site-selection design; known gaps and biases; and changes through time. Representativeness itself is evaluated against a target population or use.

### D2 Digital representation and metadata
Covers machine parseability and binding of values to variables, units, time, space, missing-value conventions, identifiers, quality/status encodings, immutable/citable versions and other structural metadata.

### D3 Semantic interoperability
Covers concept identification and semantic comparability. Vocabulary or standard-name alignment can be machine-checkable; scientific combinability may require domain judgement.

### D4 Access and operational reliability
Covers mechanisms for authorised discovery and access, APIs/services, subsetting, authentication, documentation, change notification and operational reliability. Archival preservation is related but distinct.

### D5 Provenance, quality and uncertainty
Covers lineage, production method, processing, quality control, revisions, observed/modelled/estimated status, uncertainty information, validation, performance evidence and declared limitations. Fitness is not part of this dimension.

### D6 Governance and rights
Covers stewardship, authority, licence and permissions, access restrictions, AI-use conditions, privacy/security considerations, attribution, correction mechanisms and responsibilities.

## 6. Criterion model
Each criterion MUST have exactly one home dimension. It MAY reference other criteria.

Candidate fields:
```yaml
id: AIR-D2-TIME-001
title: Time semantics are explicit
home_dimension: D2
purpose: Prevent silent temporal misinterpretation.
applies_when: []
preferred_evidence: []
requires: []
assessment_method: deterministic | declaration | domain_judgement
closing_actions: []
```

Dependencies should be criterion-level, static and versioned. `gating` dependencies block assessment; `informing` dependencies add context.

## 7. Separate assessment concepts
### Applicability
- applicable
- not applicable
- undetermined

### Evidence basis
Examples:
- deterministic inspection
- authoritative structured metadata
- provider/repository documentation
- responsible-person declaration
- third-party evidence
- deterministic derivation
- AI-suggested candidate, not accepted as evidence

Evidence should record source, observation date, scope and test/method.

### Criterion result
- met
- partially met
- not met
- indeterminate
- blocked by prerequisite
- not assessed

### Specific-use verdict
Per requirement:
- supported
- supported with caveats
- not supported
- cannot be determined
- requires domain judgement

No overall fitness label is defined in v0.2.0.

## 8. Use model
Task and operating mode are separate.

Candidate task classes:
- discovery and exploration
- integration and comparison
- prediction, classification or estimation
- monitoring, anomaly or event detection

Candidate mode modifiers:
- exploratory/research
- reproducible training snapshot
- recurring pipeline
- near-real-time operation
- limited human review
- autonomous/agent-mediated
- high-consequence decision support

A specific-use statement should eventually include required spatial/temporal resolution, acceptable gaps, necessary uncertainty information, decision consequence and human oversight.

## 9. Dataset facets
Avoid a single mutually exclusive dataset-type hierarchy. Candidate facets include:
- representation structure;
- sampling/feature geometry;
- origin;
- transformations;
- temporal status;
- access modality.

Criteria should use simple, reviewable applicability conditions over facets.

## 10. Existing standards first
The assessment SHOULD delegate checks to established standards and maintained validators where these already answer the question. Native findings should be retained as evidence rather than collapsed into a new generic score.

For CF-applicable data, CF can establish many machine-readable facts about variables, units, coordinates, time, cell bounds/methods, grids, ancillary variables, flags and discrete sampling geometries. CF conformance does not by itself establish effective observational resolution, representativeness or scientific fitness.

## 11. Determinism and observability
Evidence collection and evaluation should be separate phases. A live resource may change; the evidence bundle records retrieval time and hashes. Formal evaluation should be a deterministic function of:
- evidence bundle;
- specification version/content;
- validator/check versions;
- configuration and selected use statement.

The assessment record should state what was not assessed and why. Human overrides should preserve the original finding and record actor, reason, date and scope.

## 12. Improvement actions
An action is a catalogue entry linked to criteria and the evidence that would close or clarify them. Suggested fields:
- ID and title;
- criterion/requirements addressed;
- operation tag;
- actor;
- preconditions;
- effort;
- external dependency;
- recoverability;
- closing evidence;
- use-specific effect.

The workbench should guide improvement but not prescribe scientifically inappropriate transformations.

## 13. Open dependencies
All material needed to implement or assess against normative project requirements should be openly readable. Restricted or paid standards may be informative and crosswalked, but should not be required to apply this specification.

## 14. Non-goals for this working draft
- universal binary AI-ready declaration;
- aggregated ranking score;
- replacement for ESIP, CF, STAC, RO-Crate, Croissant or domain standards;
- automated legal judgement;
- automated scientific representativeness judgement;
- software architecture or UI specification.
