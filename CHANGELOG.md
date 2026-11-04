# Changelog

All notable changes to the conceptual specification will be recorded here.

The project uses semantic versioning as a working convention. Before 1.0, minor releases may contain conceptual or outcome-affecting changes; these must be described explicitly.

## [0.2.0-working-draft] - 2026-11-04

### Added
- Independent working definition of AI-readiness.
- Explicit assessment-target concept.
- Three assessment levels: core conformance, use-class conformance and fitness for a specific use.
- Separation of applicability, evidence basis, criterion result and use-specific verdict.
- Criterion-level prerequisite model with gating and informing relationships.
- Task classes separated from operating-mode modifiers.
- Dataset facets proposed in place of a single mutually exclusive dataset taxonomy.
- Open normative-dependency policy.
- Existing-standards-first/delegated-validation principle.
- Initial source register and project-state artefact.

### Changed
- Dimension 1 simplified to **Extent, resolution and completeness**; representativeness is treated as use-relative.
- Dimension 5 renamed to **Provenance, quality and uncertainty**; fitness removed from the dimension.
- Dimension 6 renamed to **Governance and rights**; trust treated as an outcome.
- Dimension dependencies moved conceptually from dimension-level to criterion-level.
- Data steward and repository curator treated as closely related roles.
- Project positioning changed from a standalone generic checklist toward a water/environmental operationalisation that builds on ESIP and existing standards.
- CF treated as a delegated machine-testable foundation where applicable.
- ISO/IEC 5259 treated as informative rather than normative because the standard is copyright restricted.

### Deferred
- Overall readiness/usability score or badge.
- Full water-quality chemistry/biology profiles.
- Hosted user interface.
- Bespoke validators where maintained standards validators exist.
- Normative machine-readable schemas and rule language.
- RDF/OWL/SHACL implementation.
- Formal community governance body and RFC process.

## [0.1.0] - superseded conceptual draft

### Added
- Initial six-dimension assessment model.
- Four early reference cases: hydrometric observations, citizen science, hydrological model output and abstraction/use data.
- Evidence-backed improvement-action concept.
- Initial maturity framing.

### Superseded in 0.2.0 Working Draft
- Fitness included within Dimension 5.
- Evidence state/result concepts that mixed applicability, evidence basis and outcome.
- Dimension-level dependency framing.
- Single-list dataset profiles that mixed structure, origin, processing and provider/domain.
