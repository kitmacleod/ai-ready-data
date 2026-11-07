# Project state

**Status:** v0.2.1 Working Draft  
**Date:** 2026-11-07

## Purpose

Develop an open, evidence-backed method and eventual workbench for assessing and improving the AI-readiness of water and related environmental data.

## Current proposition

**AI-readiness is the relationship between a defined data product and an intended use: the degree to which, and the conditions under which, software and its users can find, obtain, interpret, combine and rely on the data for that use without undue manual intervention, with provenance, quality, uncertainty, rights and material limitations visible.**

The project distinguishes:

- **Core conformance**: common requirements applicable to an assessment target.
- **Use-class conformance**: requirements associated with a broad class of task or operating mode.
- **Fitness for a specific use instance**: comparison of established characteristics and limitations with explicit use requirements.

The project does **not** intend to label a dataset as universally AI-ready or calculate an opaque overall readiness score.

## Current architectural position

The first standards crosswalk supports the hypothesis that much generic environmental AI-readiness can be established by existing standards and community guidance. The project's distinctive layer should therefore remain small and evidence-focused.

The principal project-specific contributions are:

- explicit and bounded assessment targets;
- traceable evidence and reproducible assessment records;
- preservation of native findings from external standards and validators;
- structured use requirements and requirement-level fitness verdicts;
- documented residual gaps before project-specific criteria are introduced;
- first-class domain judgement;
- evidence-linked improvement actions and reassessment;
- water and environmental worked examples.

## Standards-first rule

The project MUST crosswalk before inventing a criterion. A project-specific criterion requires a documented residual gap showing:

1. the assessment question or need;
2. relevant existing guidance, standards, specifications or validators considered;
3. what those mechanisms already establish;
4. why they are insufficient for the remaining question; and
5. whether the residual belongs to core conformance, use-class conformance or specific-use fitness.

Where an external mechanism adequately establishes a fact or conformance finding, the assessment SHOULD retain that native finding as evidence instead of reproducing the external rule.

## Relationship to prior art

- **ESIP AI-Ready Data Checklist v1.1** remains the primary environmental AI-readiness baseline.
- **CF Conventions** are a major reusable foundation for machine-interpretable scientific data, including variables, units, coordinates, time, bounds, cell methods, CRS, ancillary variables, quality flags and discrete sampling geometries.
- **STAC** is a candidate discovery and asset-inventory layer for suitable spatiotemporal products.
- **RO-Crate** is a candidate package/context, identity, citation, relationship and provenance layer.
- **Croissant/GeoCroissant** is a candidate ML-consumption metadata layer.
- **ISO/IEC 5259-5:2025** remains informative rather than normative because normative project dependencies must be openly readable.

## Candidate dimensions

The six dimensions are retained as a stable organising and navigation structure. They do not define an aggregate readiness model.

- D1 Extent, resolution and completeness
- D2 Digital representation and metadata
- D3 Semantic interoperability
- D4 Access and operational reliability
- D5 Provenance, quality and uncertainty
- D6 Governance and rights

Every project-specific criterion has one home dimension, but assessment logic may reference evidence or prerequisites across dimensions.

## Assessment logic

```text
assessment target
  -> applicability
  -> applicable external standards / mechanisms
  -> delegated or reused evidence
  -> residual criterion where required
  -> criterion result
  -> explicit use requirement
  -> use-specific verdict
  -> improvement action
  -> reassessment
```

## Primary pilot cases

1. HadUK-Grid daily precipitation, bounded to a published version/product representation and one declared hydrological/ML use.
2. NRFA-style hydrometric time series.
3. Riverfly RMI bounded citizen-science biological observation case.

## Challenge cases

- annual abstraction/use data assessed against a finer-scale hydrological use;
- shared or protected water-utility data.

## Immediate next work

1. Execute the bounded HadUK-Grid manual assessment defined in `examples/HADUK_GRID_ASSESSMENT_PLAN.md`.
2. Record where external evidence is sufficient and where residual AIR criteria are actually needed.
3. Revise the conceptual model only if the pilot exposes a material defect or missing concept.
4. Obtain independent domain/data-steward review and record disagreements.
5. Only after the pilot and review, draft the first formal criteria register and machine-readable assessment contract.

## Do not build yet

- hosted workbench UI;
- overall AI-readiness score or badge;
- certification;
- bespoke validators where maintained standards validators exist;
- compulsory ontology/RDF/knowledge-graph infrastructure;
- agent architecture;
- large project-specific criterion library;
- automated legal judgement;
- automated scientific representativeness judgement.

## Release interpretation

v0.2.1 is a consolidation checkpoint following the first standards crosswalk. It does not claim that the method has been empirically validated. The first completed pilot is the gate to the next material conceptual release.
