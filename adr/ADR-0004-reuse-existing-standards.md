# ADR-0004: Delegate to existing standards and maintained validators

**Status:** Accepted for v0.2.0 Working Draft  
**Date:** 2026-11-04

## Context
Environmental data already use mature standards such as CF. Reimplementing their validation would duplicate maintenance effort and risk incompatible interpretations. Earlier FDRI exploration also proposed complementary roles for CF, STAC, RO-Crate and Croissant.

## Decision
Use existing standards as authoritative for the concerns they already cover, and delegate deterministic checks to maintained validators when practical. Preserve native findings, tool versions and source evidence. Add project-specific criteria only for residual questions or explicit use-fitness evaluation.

## Consequences
- CF checker results may supply evidence but are not converted blindly into AI-readiness failures.
- STAC, RO-Crate and Croissant should retain distinct responsibilities rather than becoming duplicate metadata stores.
- The project should test whether combining existing standards leaves only a relatively small residual assessment layer.
