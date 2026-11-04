# ADR-0002: Separate conformance from fitness for a specific use

**Status:** Accepted for v0.2.0 Working Draft  
**Date:** 2026-11-04

## Context
A well-documented, standards-conformant dataset can be unsuitable for a particular spatial scale, temporal scale or scientific question. Conversely, a knowledgeable expert may be able to use a weakly documented dataset for a narrow task. Collapsing these cases into one score creates false authority.

## Decision
Represent three related outputs:
1. core conformance;
2. use-class conformance;
3. fitness evaluation against a structured specific-use statement.

Fitness is not a dimension. Specific-use conclusions are reported per requirement and may explicitly require domain judgement.

## Consequences
- No universal binary `AI-ready` property.
- No overall fitness confidence label in the working draft.
- Use requirements become first-class assessment inputs.
