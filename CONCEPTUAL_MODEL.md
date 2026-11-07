# Conceptual model

**Version:** 0.2.1-working-draft

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
  nominal_spatial_resolution: 1km
  resources: []
```

The assessment MUST state the granularity of its conclusions and MUST NOT imply uniform findings across variables, stations, periods, representations or access routes not assessed.

## 4. Three assessment levels

### 4.1 Core conformance

Use-independent requirements, wherever applicable.

### 4.2 Use-class conformance

Requirements associated with a broad task or operating mode.

### 4.3 Fitness for a specific use instance

A comparison between explicitly stated use requirements and characteristics or limitations established for the assessment target.

Automation is expected to be stronger at identifying hard mismatches than at proving scientific fitness.

## 5. Organising dimensions

The six dimensions provide a stable home and navigation structure for criteria. They are **not** six independent scores and do not define the assessment workflow.

### D1 Extent, resolution and completeness

Spatial, temporal, thematic and population scope; resolution/support; expected versus observed completeness; sampling or site-selection design; known gaps and biases; and changes through time. Representativeness is evaluated against a target population or use.

### D2 Digital representation and metadata

Machine parseability and binding of values to variables, units, time, space, missing-value conventions, identifiers, quality/status encodings, immutable/citable versions and other structural metadata.

### D3 Semantic interoperability

Concept identification and semantic comparability. Vocabulary or standard-name alignment can be machine-checkable; scientific combinability may still require domain judgement.

### D4 Access and operational reliability

Mechanisms for authorised discovery and access, APIs/services, bulk access, subsetting, authentication, documentation, change notification and operational reliability. Archival preservation is related but distinct.

### D5 Provenance, quality and uncertainty

Lineage, production method, processing, quality control, revisions, observed/modelled/estimated status, uncertainty information, validation, performance evidence and declared limitations. Fitness is not part of this dimension.

### D6 Governance and rights

Stewardship, authority, licence and permissions, access restrictions, AI-use conditions, privacy/security considerations, attribution, correction mechanisms and responsibilities.

## 6. Standards-first and residual-gap rule

The project MUST assess applicable prior art before creating a project-specific criterion.

A project-specific criterion MUST have a documented residual need. The crosswalk MUST identify relevant guidance, standards, specifications or maintained validators and explain why they do not fully answer the assessment question.

Where an external mechanism adequately establishes the required fact or conformance finding, the assessment SHOULD reuse that native evidence rather than introduce a duplicate AIR criterion.

A residual question may legitimately remain where, for example:

- an external standard establishes encoding but not scientific meaning or sufficiency;
- a declaration must be evaluated against a stated use;
- multiple standards provide complementary evidence but no integrated conclusion;
- domain judgement is inherently required;
- the project needs reproducible assessment/evidence mechanics not supplied by the data standard itself.

## 7. Criterion model

Each project-specific criterion MUST have exactly one home dimension. It MAY reference other criteria or external mechanisms.

Candidate fields:

```yaml
id: AIR-D1-RES-001
title: Effective resolution is characterised where materially different from nominal resolution
home_dimension: D1
purpose: Prevent encoded spacing being mistaken for supported observational information scale.
applies_when: []
prior_art:
  - mechanism: ESIP
    coverage: partial
  - mechanism: CF
    coverage: encoding evidence
residual_gap: Scientific support/effective resolution is not established by encoded spacing alone.
preferred_evidence: []
requires: []
assessment_method: deterministic | declaration | domain_judgement
closing_actions: []
```

Dependencies are criterion-level, static and versioned. **Gating dependencies** block assessment; **informing dependencies** add context without blocking it.

## 8. Evidence model

Evidence collection and criterion evaluation are separate.

### 8.1 Applicability

- applicable
- not applicable
- undetermined

### 8.2 Evidence basis

Examples:

- maintained-validator finding;
- deterministic inspection;
- authoritative structured metadata;
- provider/repository documentation;
- responsible-person declaration;
- third-party evidence;
- deterministic derivation;
- AI-suggested candidate, not accepted as evidence.

Every evidence item SHOULD record:

- source identifier or location;
- source/version where applicable;
- observation/retrieval date;
- scope within the assessment target;
- acquisition or test method;
- content hash where a snapshot is retained;
- validator/tool and version where applicable.

External findings SHOULD preserve their native identity and severity/status rather than being silently rewritten into project terminology.

### 8.3 Criterion result

- met
- partially met
- not met
- indeterminate
- blocked by prerequisite
- not assessed

### 8.4 Specific-use verdict

Per use requirement:

- supported
- supported with caveats
- not supported
- cannot be determined
- requires domain judgement

No overall fitness label is defined in v0.2.1.

## 9. Delegated validation

The method SHOULD delegate checks to established standards and maintained validators where these already answer the question.

For CF-applicable data, CF can establish many machine-readable facts about variables, units, coordinates, calendars, cell bounds/methods, grids, ancillary variables, flags and discrete sampling geometries. A maintained CF checker should be preferred to recreating these rules.

A standards warning or failure is evidence about that standard's conformance requirement. It is not automatically an AI-readiness failure. The project criterion or use requirement must state why the finding is material.

## 10. Nominal versus effective resolution

**Nominal resolution** is the encoded or published grid spacing, cell size or observation spacing.

**Effective resolution** is the scale of information the observation, sampling, interpolation or production process can meaningfully support.

The two MUST NOT be treated as interchangeable. An encoded 1 km grid can be perfectly machine-readable while the underlying observing network and production method do not support independent 1 km-scale information.

This distinction is a model residual: standards can describe coordinates, bounds and processing metadata, but the scientific support appropriate to a use may require provider evidence or domain judgement.

## 11. Use model

Task and operating mode are separate.

Candidate task classes:

- discovery and exploration;
- integration and comparison;
- prediction, classification or estimation;
- monitoring, anomaly or event detection.

Candidate mode modifiers:

- exploratory/research;
- reproducible training snapshot;
- recurring pipeline;
- near-real-time operation;
- limited human review;
- autonomous/agent-mediated;
- high-consequence decision support.

A specific-use statement SHOULD include, where material:

- target phenomenon or population;
- spatial support/resolution required;
- temporal support/resolution required;
- geographical and temporal domain;
- acceptable missingness and latency;
- required uncertainty/QC information;
- transformations or combinations envisaged;
- evaluation/validation expectations;
- decision consequence;
- human oversight and escalation.

## 12. Dataset facets

Avoid a single mutually exclusive dataset-type hierarchy. Candidate facets include:

- representation structure;
- sampling/feature geometry;
- origin;
- transformations;
- temporal status;
- access modality.

Criteria should use simple, reviewable applicability conditions over facets.

## 13. Determinism, records and overrides

A live resource may change. The evidence bundle therefore records retrieval time and, where practical, content hashes or immutable identities.

Formal evaluation should be a deterministic function of:

- evidence bundle;
- specification version/content;
- validator/check versions;
- configuration;
- selected use statement.

The assessment record MUST state what was not assessed and why.

Human overrides MUST preserve the original finding and record actor, reason, date and scope.

AI assistance may locate evidence, suggest mappings or draft explanations, but AI-generated claims are not accepted as evidence without verification against an authoritative source.

## 14. Improvement actions

An improvement action is a catalogue entry linked to criteria or use requirements and the evidence expected to close or clarify them.

Suggested fields:

- ID and title;
- criteria/use requirements addressed;
- operation tag;
- actor;
- preconditions;
- effort;
- external dependency;
- recoverability;
- closing evidence;
- expected use-specific effect.

The future workbench should guide improvement without prescribing scientifically inappropriate transformations.

## 15. Open dependencies

All material needed to implement or assess against normative project requirements must be openly readable.

Restricted or paid standards may be informative and crosswalked, but cannot be required to apply the specification. Project documentation must not reproduce copyright-protected normative text without permission.

## 16. Non-goals for this working draft

- universal binary AI-ready declaration;
- aggregated ranking/readiness score;
- replacement for ESIP, CF, STAC, RO-Crate, Croissant or domain standards;
- compulsory RDF/knowledge-graph publication;
- bespoke validation where maintained standards validators suffice;
- automated legal judgement;
- automated scientific representativeness judgement;
- software architecture, UI or agent specification;
- a complete criteria library before pilot validation.
