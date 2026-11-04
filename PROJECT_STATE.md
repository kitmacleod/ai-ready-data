# Project state

**Status:** v0.2.0 Working Draft  
**Date:** 2026-11-04

## Purpose
Develop an open, evidence-backed method and eventual workbench for assessing and improving the AI-readiness of water and related environmental data.

## Current proposition
AI-readiness is a relationship between a defined data product and an intended use: the degree to which, and the conditions under which, software and its users can find, obtain, interpret, combine and rely on the data for that use without undue manual intervention, with provenance, quality, uncertainty, rights and material limitations visible.

The project distinguishes:
1. **Core conformance**: common requirements applicable to an assessment target.
2. **Use-class conformance**: requirements associated with a broad class of use.
3. **Fitness for a specific use instance**: comparison of data characteristics with explicit user requirements.

The project does **not** intend to label a dataset as universally AI-ready or calculate an opaque overall readiness score.

## Current hypothesis
Existing standards and community work may establish much of general conformance. The project's distinctive value may lie primarily in:
- explicit assessment targets;
- traceable evidence and reproducible assessment;
- structured use requirements;
- specific-use fitness evaluation;
- first-class domain judgement;
- practical improvement actions and reassessment;
- water and environmental worked examples.

## Relationship to prior art
ESIP AI-Ready Data Checklist v1.1 is the primary environmental AI-readiness baseline. CF Conventions are a major reusable foundation for machine-interpretable scientific data. STAC, RO-Crate and Croissant are candidate complementary layers for discovery, provenance/context and ML consumption respectively. The project aims to reuse and profile these approaches rather than replace them.

## Candidate dimensions
These remain working hypotheses and may change after crosswalking and pilots:
1. Extent, resolution and completeness
2. Digital representation and metadata
3. Semantic interoperability
4. Access and operational reliability
5. Provenance, quality and uncertainty
6. Governance and rights

Every criterion should have one home dimension and may cross-reference other criteria.

## Primary pilot cases
1. A bounded gridded environmental product, initially HadUK-Grid daily precipitation or a similarly well-documented target.
2. An NRFA-style hydrometric time series.
3. A bounded Riverfly RMI citizen-science biological observation case.

## Challenge cases
- Annual abstraction/use data against a finer-scale hydrological requirement.
- Shared or protected water-utility data.

## Reference implementation hypothesis from earlier FDRI work
1. Improve and validate scientific internals, including CF where applicable.
2. Generate STAC from authoritative scientific metadata for asset discovery.
3. Use RO-Crate for dataset identity, provenance, licensing, citation and relationships.
4. Define representative ML use patterns and use Croissant to describe ML consumption, referencing published assets.

## Immediate work
1. Complete ESIP -> existing standards -> residual gap crosswalk.
2. Refine the conceptual model and glossary from the crosswalk.
3. Perform one bounded manual assessment.
4. Obtain independent expert review.
5. Only then develop machine-readable assessment contracts.

## Do not build yet
- hosted workbench UI;
- overall AI-readiness score or badge;
- certification;
- bespoke CF/STAC/etc. validators where maintained validators exist;
- ontology or compulsory RDF infrastructure;
- agent architecture;
- large criterion library;
- automated legal decisions.
