# Glossary

**Status:** v0.2.1 Working Draft. Terms should align with established community definitions where practical.

## AI-readiness

A relationship between a defined data product and an intended use, concerned with whether software and users can find, obtain, interpret, combine and rely on it with its material provenance, quality, uncertainty, rights and limitations visible.

## Assessment target

The explicitly bounded object being assessed, including version, representation and scope. It may be narrower than a complete published dataset.

## Core conformance

Satisfaction of applicable common requirements independent of a specific use instance.

## Use-class conformance

Satisfaction of requirements associated with a broad task class or operating mode.

## Specific-use fitness

The outcome of comparing an assessment target with explicit requirements for one intended use. It is not a general property of the dataset.

## Dimension

An organising category that provides a home for criteria. In v0.2.1 dimensions are for navigation and ownership, not independent scores.

## Criterion

A single testable or reviewable project requirement with one home dimension. A project-specific criterion requires a documented residual gap.

## Prior-art mechanism

An existing checklist, standard, specification, convention, validator or maintained practice considered before creating a project-specific criterion.

## Delegated validation

Using an established standard and, where practical, its maintained validator to establish a finding instead of reimplementing the external standard in this project.

## Native finding

A result produced by an external standard, validator or assessment mechanism retained with its original identity, source/tool and version rather than collapsed into a generic project score.

## Residual gap

A question necessary for conformance or use-fitness evaluation that remains after relevant existing mechanisms have been considered. A residual gap must state what prior art covers and why that coverage is insufficient for the remaining question.

## Applicability

Whether a criterion applies to the assessment target and context: applicable, not applicable or undetermined.

## Evidence item

A traceable item used to support a criterion result or use-specific verdict, including source, scope, date/version and acquisition or test method.

## Evidence basis

The way evidence was obtained, such as a maintained-validator finding, deterministic inspection, authoritative structured metadata, documentation, declaration or third-party evidence.

## Finding / criterion result

The result of evaluating a criterion: met, partially met, not met, indeterminate, blocked by prerequisite, or not assessed.

## Assurance

How strongly a result is supported by its evidence. v0.2.1 exposes the evidence basis and provenance rather than assigning an overall assurance score.

## Gating prerequisite

A dependency that must be established before a criterion can be evaluated.

## Informing dependency

A dependency that supplies context but does not by itself block evaluation.

## Use requirement

A structured requirement for a specific intended use, for example a required temporal support, spatial scale, geographical domain, acceptable gaps, or uncertainty information.

## Use-specific verdict

Comparison of one use requirement with the assessment target: supported, supported with caveats, not supported, cannot be determined, or requires domain judgement.

## Domain judgement

A conclusion requiring relevant scientific or operational expertise and not safely derivable solely from machine inspection.

## Blocked

A criterion result indicating that assessment cannot proceed because a gating prerequisite has not been established.

## Nominal resolution

The encoded or published spacing or size of observations, grid points or cells.

## Effective resolution

The scale of information that the observation, sampling or production process can meaningfully support. It may differ materially from nominal resolution.

## Scientific support

The spatial, temporal, thematic or population support to which a data value or product meaningfully pertains, taking account of sampling and production methods rather than only its encoded coordinates.

## Provenance

Information about sources, production, processing and responsible agents sufficient to understand how an assessment target came to exist.

## Quality and uncertainty information

Information supplied with or about data describing measurement quality, validation, limitations, uncertainty, bias, QC or similar characteristics. Absence of reported uncertainty does not imply absence of uncertainty.

## Open / controlled / protected access

Provisional access categories. Access identifies who can obtain data; rights identify what authorised users may do with it. A protected dataset is not automatically less AI-ready.

## Improvement action

A documented action that can provide new or improved evidence, remove a blocker, mitigate a limitation or make a limitation clearer.

## Closing evidence

Evidence expected to demonstrate completion of an improvement action or permit reassessment.

## Evidence bundle

A versioned or snapshotted collection of evidence used as input to reproducible evaluation.

## Assessment manifest

A machine-readable record of the target, evidence, specification/check versions, results, exclusions, overrides and other information needed to understand or replay an assessment.

## Reassessment

A new evaluation after evidence, the target, the specification, a validator or a use statement has changed. Prior results should remain traceable rather than being overwritten without history.
