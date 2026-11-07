# AI-Ready Water and Environmental Data

**Working draft: v0.2.1**  
**Checkpoint date: 2026-11-07**

This repository develops an open, evidence-backed method for assessing and improving the AI-readiness of water and related environmental data. The intended future product is a workbench, but the present repository is deliberately focused on the assessment model, standards reuse, evidence, and bounded real-data pilots.

## Core idea

AI-readiness is treated as a relationship between a defined data product and an intended use. The method separates:

1. **core conformance**, for common use-independent requirements;
2. **use-class conformance**, for broad task or operating-mode requirements; and
3. **fitness for a specific use**, evaluated requirement by requirement against an explicit use statement.

The assessment exposes evidence, caveats, unresolved domain judgement and improvement actions. It does not assign a universal AI-ready badge or opaque composite score.

## Development principle

**Reuse standards first; add only residual assessment logic.**

ESIP AI-Ready Data Checklist v1.1 is the primary environmental baseline. Where an established standard already answers an assessment question, its native finding should be reused as evidence rather than recreated as an AIR criterion. CF is a major machine-testable foundation for scientific representation where applicable. STAC, RO-Crate and Croissant are candidate complementary layers for discovery, package/context/provenance and ML consumption.

A project-specific criterion requires a documented residual gap: the crosswalk must identify relevant prior art, explain what it already establishes, and state the unresolved question that remains necessary for conformance or use-fitness evaluation.

## Organising dimensions

The six dimensions remain a navigation and ownership structure for criteria, not the primary logic of assessment:

- D1 Extent, resolution and completeness
- D2 Digital representation and metadata
- D3 Semantic interoperability
- D4 Access and operational reliability
- D5 Provenance, quality and uncertainty
- D6 Governance and rights

## Assessment logic

```text
assessment target
  -> applicable external standards / evidence
  -> delegated or reused findings
  -> residual project criterion where necessary
  -> criterion result
  -> explicit use requirement
  -> use-specific verdict
  -> improvement action
  -> reassessment
```

## Repository map

- `PROJECT_STATE.md` - authoritative checkpoint and immediate next work.
- `CONCEPTUAL_MODEL.md` - working conceptual specification.
- `GLOSSARY.md` - controlled working terminology.
- `SOURCES.md` - maintained evidence/source register.
- `crosswalk/CROSSWALK.md` - standards reuse and residual-gap analysis.
- `adr/` - accepted material design decisions.
- `examples/` - bounded pilots used to test and refine the model.
- `CHANGELOG.md` - version history.
- `LICENSE-NOTE.md` - unresolved licensing decision.

## Current pilot

The first bounded pilot is HadUK-Grid daily precipitation at nominal 1 km resolution. The pilot is intentionally designed to test a scientifically important distinction: encoded grid spacing is not necessarily the effective observational resolution that the underlying station network and interpolation process can support.

See `examples/HADUK_GRID_ASSESSMENT_PLAN.md`.

## What this project is not

- not a universal AI-ready declaration or certification;
- not a composite readiness score;
- not a replacement for ESIP, CF, STAC, RO-Crate, Croissant or domain standards;
- not a bespoke CF/STAC/etc. validator where maintained standards validators exist;
- not a requirement to publish RDF, OWL or a knowledge graph;
- not yet a software application or agent architecture;
- not an automated legal or scientific judgement system.

## Next checkpoint

v0.2.1 consolidates the model after the first standards crosswalk. The next evidence-generating step is one bounded manual HadUK-Grid assessment, followed by independent review. A formal criteria register and machine-readable assessment contract are deferred until the pilot has tested the conceptual model.
