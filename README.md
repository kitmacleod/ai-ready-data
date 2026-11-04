# AI-Ready Water and Environmental Data

**Working draft: v0.2.0**

This repository develops an open method for assessing and improving the AI-readiness of water and related environmental data. The intended future product is an evidence-backed workbench, but this repository is currently focused on the assessment model, alignment with existing standards and real-data pilots.

## Core idea
The project treats AI-readiness as a relationship between a defined data product and an intended use. It separates common conformance from fitness for a specific use and records the evidence, limitations and unresolved domain judgements behind every conclusion.

## What this project is not
- not a universal `AI-ready` badge;
- not an opaque readiness score;
- not a replacement for ESIP, CF, STAC, RO-Crate, Croissant or established domain standards;
- not yet a software application.

## Current development principle
**Reuse standards first; add only the residual assessment logic.**

The primary environmental baseline is the ESIP AI-Ready Data Checklist v1.1. CF is treated as a major machine-testable foundation where it applies. STAC, RO-Crate and Croissant are being crosswalked for complementary roles in discovery, provenance/context and ML consumption.

## Start here
1. `PROJECT_STATE.md` for the current project checkpoint.
2. `CONCEPTUAL_MODEL.md` for the working model.
3. `GLOSSARY.md` for terminology.
4. `SOURCES.md` for the evidence base.
5. `crosswalk/CROSSWALK.md` for reuse/gap analysis.
6. `adr/` for material design decisions.
7. `CHANGELOG.md` for version history.

## Current next steps
- complete the ESIP/CF/STAC/RO-Crate/Croissant crosswalk;
- refine the conceptual model from that crosswalk;
- perform a bounded HadUK-Grid manual assessment;
- test with independent domain/data-steward review;
- only then define machine-readable contracts and validation behaviour.

