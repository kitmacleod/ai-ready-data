# Changelog

All notable changes to the conceptual specification are recorded here.

The project uses semantic versioning as a working convention. Before 1.0, minor releases may contain conceptual or outcome-affecting changes; these must be described explicitly.

## [0.2.1-working-draft] - 2026-11-07

### Added

- Completed first-pass prior-art crosswalk as a maintained project artefact.
- Explicit residual-gap rule for project-specific criteria.
- Criterion provenance expectation linking project requirements to relevant prior art and delegated evidence.
- Explicit distinction between organising dimensions and assessment workflow.
- Native-finding concept for evidence returned by external standards and maintained validators.
- HadUK-Grid bounded manual-assessment plan in `examples/`.
- Effective resolution/scientific support as an exemplar residual environmental question.

### Changed

- Clarified that the six dimensions are a navigation/home structure, not independent readiness scores.
- Strengthened the existing-standards-first principle from guidance into a criterion-design constraint.
- Clarified that external standard findings should retain source/tool/version and native status instead of being blindly translated into AI-readiness failures.
- Refined evidence-basis terminology to include maintained-validator findings explicitly.
- Clarified the separation between access class and permitted use.
- Updated CF treatment so normative references target released CF 1.13, while the captured 1.14 material is treated as draft evidence only.
- Refined project state so the next development gate is empirical testing through HadUK-Grid rather than expansion of the criteria library.
- Expanded the glossary with residual gap, delegated validation, native finding, scientific support and reassessment.
- Updated the source register to distinguish verified primary material from detailed standard mappings still requiring verification.

### Confirmed

- No universal binary AI-ready declaration.
- No composite readiness/usability score or badge.
- No bespoke CF/STAC/etc. validator where maintained validation exists.
- No compulsory RDF/OWL/knowledge-graph architecture.
- No large project-specific criteria library before pilot validation.
- ISO/IEC 5259 remains informative rather than normative.
- Licensing remains unresolved pending an explicit project decision.

### Deferred

- First completed HadUK-Grid assessment.
- Formal criteria register.
- Machine-readable assessment schema/contract.
- Automated assessment implementation.
- Detailed normative mappings for STAC, RO-Crate and Croissant.
- Additional hydrometric and citizen-science pilots.

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
