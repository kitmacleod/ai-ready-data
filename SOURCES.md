# Source register

**Status:** v0.2.1 Working Draft.  
This register records sources that materially influence the conceptual specification. Inclusion is not endorsement. Adoption decisions belong in the crosswalk or an ADR.

## Tier 1: foundational/open sources

### ESIP AI-Ready Data Checklist v1.1

- File: `ai-ready-data-checklist-v.1.1.md`
- Version: 1.1
- Published: 2026-09-30; typo update: 2026-10-06
- Role: primary environmental AI-readiness baseline and checklist prior art.
- Project implications: explicit assessment granularity; raw/derived status; quality, documentation, access and preparation questions; restricted-data handling; use guidance.
- Treatment: crosswalk first; reuse/profile before project-specific criteria.

### ESIP Data Readiness Cluster 2026 update

- File: `2026-09-01_Rao.pdf`
- Role: community direction of travel and WDS pilot feedback.
- Project implications: intentionality, interpretability, interoperability and scalability; explicit CF/ACDD crosswalk work; movement toward machine-actionable assessment and improvement recommendations.
- Treatment: informative positioning and crosswalk evidence.

### CF Metadata Conventions

- File: `NetCDF Climate and Forecast (CF) Metadata Conventions.pdf`
- Captured document: 1.14 draft snapshot.
- Normative target for this project checkpoint: latest released version represented in the captured document, CF 1.13, released 2025-12-17.
- Licence: captured document states CC0.
- Role: authoritative scientific representation semantics where CF applies.
- Project implications: standard names, units, coordinates, calendars, bounds, cell methods, CRS, ancillary variables, quality flags, uncertainty-related variables, geometries, DSG and an encoding-independent conceptual data model.
- Treatment: delegate validation to maintained CF tooling where practical; retain native findings. CF conformance does not establish representativeness, effective observational resolution or specific-use fitness.

### STAC

- Role: candidate spatiotemporal asset inventory and discovery layer.
- Treatment: profile for appropriate targets; preserve a small-core/extension philosophy; do not make STAC universal where another discovery mechanism is more appropriate.
- Evidence status at v0.2.1: detailed primary-source field mapping remains to be completed before any STAC-specific normative criteria are created.

### RO-Crate

- Role: candidate package/context layer for identity, citation, agents, relationships and provenance.
- Treatment: complementary to scientific in-file metadata and asset catalogues; avoid duplicate authoritative metadata stores.
- Evidence status at v0.2.1: detailed primary-source field mapping remains to be completed before normative project dependencies are declared.

### Croissant / GeoCroissant / Responsible AI extension

- Role: candidate ML-consumption and machine-readable dataset metadata layer.
- Treatment: profile for representative ML consumption patterns and link to authoritative scientific metadata/assets rather than copying them.
- Evidence status at v0.2.1: exact field-level mapping remains VERIFY work.

## Tier 2: strongly informative

### PNNL AI-Ready Data Pilot Project Report

- File: `3020608.pdf`
- Date: 2025-12
- Role: practitioner pilot showing workflow friction, human interpretability, stewardship signals and dependence on domain expertise.
- Caution: only three practitioners and three CSV datasets; tabular-specific recommendations must not be universalised.

### ODI A framework for AI-ready data v2

- File: `A_framework_for_AI-ready_data_V2.pdf`
- Date: 2025
- Role: generic framework covering dataset properties, metadata, surrounding infrastructure and governance.
- Treatment: concept source for machine-readable metadata, provenance, access, versioning and governance; do not import recommendations uncritically into environmental conformance.

### ODI A framework for AI-ready enterprise data

- File: `A_framework_for_AI-ready_enterprise_data.pdf`
- Date: 2026-06
- Licence: CC BY 4.0.
- Role: 21-criterion enterprise framework built from comparative review and interviews.
- Treatment: informative. Enterprise MDM, shared business ontology, knowledge graph, policy-as-code and active-cataloguing recommendations are context-specific, not universal environmental dataset requirements.

### Toward FAIR and AI-Ready Data: GlueX case study

- File: `TowardFairAndAIReadyDataSep2026.pdf`
- Status: preprint.
- Role: example of separating FAIR from a deterministic AI-readiness layer, evaluating existing validation software, retaining per-criterion profiles and identifying domain-native gaps.
- Treatment: strongly informative for assessment mechanics, with caution that the case is experimental nuclear physics and the framework has not yet been tested end to end on a second domain.

### HadUK-Grid data paper

- File: `Geoscience Data Journal - 2019 - Hollis - HadUK-Grid A new UK dataset of gridded climate observations.pdf`
- Role: first bounded worked case.
- Project implications: derived/interpolated observations; time semantics; changing station network; QC limitations; versioning; CF-compliant netCDF; explicit distinction between 1 km grid spacing and effective observational resolution.
- Treatment: primary evidence for the first pilot. The paper describes v1.0.0.0; the actual pilot must bind to an explicitly selected product version before conclusions are recorded.

## Tier 3: architecture and implementation references

### Data Director reference implementation

- File: `Joe-Heffer-Towards-a-Data-Director-reference-implementation-2026-10-16.pdf`
- Role: implementation inspiration for stable records, evidence hashes, grounding/source checks, deterministic record construction, policy gates, conformance/evaluation separation and human referral.
- Treatment: later workbench architecture inspiration, not an AI-readiness standard.

### Agentic AI for Research Data Management workshop plan

- File: `DSN-AI-Agents-for-RDM-Workshop-Plan.pdf`
- Role: community context and explicit human-control principle for consequential RDM decisions.
- Treatment: informative for future workbench/agent governance only.

### Earlier FDRI exploration

- File: `05 wcs_2026-02-23_km.pptx`
- Role: project history and reference implementation hypothesis using CF + STAC + RO-Crate + Croissant.
- Treatment: historical design input, not evidence that those four mechanisms are required for every target.

## Restricted/informative sources

### ISO/IEC 5259-5:2025

- File: `ISO-IEC-5259-5-2025.pdf`
- Role: informative alignment on data-quality governance, responsibilities, risk and lifecycle controls for analytics/ML.
- Restriction: copyright-protected.
- Treatment: informative only. Normative project requirements must not require access to this paid/restricted standard or reproduce its protected text.

## Historical synthesis

### AI-Ready Data Assessment: Operationalising FAIR for Water and Environmental Data

- File: `AI-Ready Data Assessment Operationalising FAIR for Water and Environmental Data.docx`
- Date: 2026-11-07
- Role: exploratory synthesis that helped motivate layered assessment, FAIR operationalisation, use-relative fitness and the need to avoid composite scores.
- Treatment: historical/supporting analysis rather than authoritative project state. Where it conflicts with the accepted ADRs or current conceptual model, the maintained repository artefacts prevail.

## Source policy

- Normative project requirements must be understandable from openly readable project text or openly readable normative dependencies.
- Existing domain standards should be delegated to rather than rewritten where practical.
- External findings should preserve source/version and validator/tool identity.
- Search snippets, AI summaries and undocumented claims are not acceptable primary evidence for a criterion result.
- A source's existence does not make its recommendation appropriate for this project.
- Detailed STAC, RO-Crate and Croissant mappings remain verification work rather than assumed conformance requirements in v0.2.1.
