# Source register

**Status:** initial register for v0.2.0 Working Draft.

The register prevents the project from relying on conversational memory. Source details and interpretations should be updated when they materially influence the specification.

## Tier 1: foundational/open sources

### ESIP AI-Ready Data Checklist v1.1
- File: `ai-ready-data-checklist-v.1.1.md`
- Version: 1.1
- Published: 2026-09-30; typo update: 2026-10-06
- Role: primary environmental AI-readiness baseline and checklist prior art.
- Notable project implications: minimum measurable bundle; file-level assessment as pragmatic current approach; separate raw/derived assessment; quality, documentation, access and preparation questions; restricted-data questions.
- Treatment: detailed crosswalk; reuse or specialise before inventing project-specific criteria.

### ESIP Data Readiness Cluster 2026 update
- File: `2026-09-01_Rao.pdf`
- Role: direction of travel and WDS pilot feedback.
- Notable implications: intentionality, definitions/examples, interoperability with existing conventions, scalability; CF/ACDD crosswalk; movement toward automated assessment and recommendations.
- Treatment: informative project-positioning source.

### CF Metadata Conventions
- File: `NetCDF Climate and Forecast (CF) Metadata Conventions.pdf`
- Captured page was the 1.14 draft; latest released version listed in that document is 1.13 (2025-12-17).
- Licence: document states CC0.
- Role: authoritative environmental/scientific representation semantics where CF applies.
- Notable implications: standard names, units, coordinates, calendars, bounds, cell methods, quality/ancillary variables, CRS, DSG, geometries and encoding-independent CF data model.
- Treatment: delegate validation where possible; preserve native findings; target released CF versions for normative use.

### Croissant / GeoCroissant / Responsible AI extension
- Primary links supplied separately.
- Role: ML-oriented machine-readable metadata, geographic extensions, provenance/responsible-AI information.
- Treatment: detailed crosswalk pending exact field review.

### STAC
- Primary links supplied separately.
- Role: asset inventory and spatial-temporal discovery; useful model for small core, extensions and validation.
- Treatment: reuse for discovery where appropriate; do not copy its governance model without verification.

### RO-Crate
- Role: candidate dataset/package identity, citation, agents, relationships and provenance layer.
- Treatment: earlier FDRI reference implementation hypothesis; detailed crosswalk pending.

## Tier 2: strongly informative

### PNNL AI-Ready Data Pilot Project Report
- File: `3020608.pdf`
- Date: 2025-12
- Role: practitioner pilot demonstrating workflow friction, interpretability, stewardship signals and domain-expert dependence.
- Caution: pilot used three CSV datasets and its starter checklist includes tabular-specific recommendations that should not be universalised.

### ODI A framework for AI-ready data v2
- File: `A_framework_for_AI-ready_data_V2.pdf`
- Date: 2025
- Role: generic framework covering dataset properties, metadata, infrastructure and governance.
- Treatment: crosswalk concepts, particularly Croissant, provenance, access and governance.

### ODI A framework for AI-ready enterprise data
- File: `A_framework_for_AI-ready_enterprise_data.pdf`
- Date: 2026-06
- Licence: CC BY 4.0.
- Role: 21-criterion enterprise framework built from comparative review and interviews.
- Treatment: informative; avoid importing enterprise-only assumptions such as compulsory MDM/knowledge graphs into environmental dataset conformance.

### HadUK-Grid data paper
- File: `Geoscience Data Journal - 2019 - Hollis - HadUK-Grid A new UK dataset of gridded climate observations.pdf`
- Role: first candidate real gridded worked case.
- Notable implications: interpolated observations, changing station network, explicit observation-day semantics, QC limitations, versioning, CF-compliant NetCDF and important distinction between 1 km grid spacing and effective observational resolution.

## Tier 3: architecture and implementation references

### Data Director reference implementation
- File: `Joe-Heffer-Towards-a-Data-Director-reference-implementation-2026-10-16.pdf`
- Role: implementation principles for provenance, stable records, deterministic metadata, grounding, policy gates, conformance/evaluation separation, tests and human referral.
- Treatment: architectural inspiration for later workbench design, not an AI-readiness standard.

### Agentic AI for Research Data Management workshop plan
- File: `DSN-AI-Agents-for-RDM-Workshop-Plan.pdf`
- Role: community/role context and explicit human-control principle for RDM agents.

### Earlier FDRI exploration
- File: `05 wcs_2026-02-23_km.pptx`
- Role: project history/reference implementation hypothesis using CF + STAC + RO-Crate + Croissant.

## Restricted/informative sources

### ISO/IEC 5259-5:2025
- File: `ISO-IEC-5259-5-2025.pdf`
- Role: informative alignment for data-quality governance, responsibilities and lifecycle controls.
- Restriction: copyright-protected; not suitable as a required open normative dependency.
- Treatment: describe conceptual alignment without reproducing protected requirements or requiring implementers to purchase the standard.

## Source policy
1. Normative project requirements must be understandable from openly readable project text or openly readable normative dependencies.
2. Existing domain standards should be delegated to rather than rewritten where practical.
3. External source claims in project documentation should include source/version.
4. A source's existence does not make its recommendation appropriate for this project; each adoption decision belongs in the crosswalk or an ADR.
