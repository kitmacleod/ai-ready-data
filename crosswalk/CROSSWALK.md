# Prior-art and standards crosswalk

**Status:** scaffold for v0.2.0 Working Draft. Do not treat blank cells as gaps in external standards.

## Purpose
Determine what the project genuinely needs to add by mapping AI-readiness questions to existing community guidance and technical standards. The preferred outcome is often **reuse**, not a new AIR criterion.

## Decision values
- `ADOPT`: existing approach is sufficient.
- `PROFILE`: reuse with water/environmental applicability guidance.
- `EXTEND`: existing approach covers part of the need; project-specific residual remains.
- `DIFFER`: deliberate project difference with recorded rationale.
- `VERIFY`: primary-source review still needed.

## Initial crosswalk

| Need / ESIP area | Existing mechanism | Initial decision | Residual question for this project |
|---|---|---|---|
| Assessment granularity | ESIP v1.1 minimum measurable bundle; pragmatic file-level manual assessment | ADOPT + EXTEND | Define explicit assessment target and scope of conclusions |
| Dataset version/raw-derived status | ESIP General Information | ADOPT | Record exact target/version in assessment manifest |
| Spatial/temporal extent | ESIP Quality/Documentation; CF coordinates and bounds where applicable | ADOPT/PROFILE | Is the encoded extent the relevant scientific support for the intended use? |
| Spatial/temporal resolution | ESIP Quality; CF coordinates/bounds/cell methods | EXTEND | Distinguish nominal encoding resolution from effective informational/observational resolution |
| Missing values | ESIP Preparation; CF `_FillValue`, missing/valid ranges | ADOPT/PROFILE | Distinguish encoding from scientific meaning of missingness and use impact |
| Variable meaning | ESIP Documentation; CF `standard_name`, units, long_name | ADOPT/PROFILE | Shared identifiers do not prove scientific comparability |
| Time semantics | CF time units, calendar, bounds, cell methods | ADOPT/PROFILE | Domain/use-specific timing conventions may still require interpretation |
| CRS/geolocation | CF coordinates and grid mappings | ADOPT | Confirm domain-specific vertical/reference requirements where relevant |
| QC/status flags | CF ancillary variables and flags; ESIP quality procedures | ADOPT/PROFILE | Determine whether available QA/QC evidence is sufficient for the intended use |
| Uncertainty | ESIP Quality; CF ancillary variables can encode uncertainty-related variables | EXTEND | Capture model/sampling/structural uncertainty and limitations outside file-level encoding |
| Bias/representativeness | ESIP Quality | PROFILE/EXTEND | Fitness layer evaluates against a stated target population/use; domain judgement may be required |
| Provenance | ESIP; CF `source`, `history`, `references`; RO-Crate/PROV candidates | EXTEND | Define sufficient end-to-end lineage and evidence provenance without duplicating metadata |
| Integrity/fixity | ESIP checksums; RO-Crate candidates | ADOPT | Assessment evidence bundle also needs hashes and retrieval time |
| Dataset discovery | ESIP Documentation; STAC for spatiotemporal assets | PROFILE | Identify appropriate discovery standard by target type |
| Access/API | ESIP Access; STAC API/OGC/open APIs where relevant | PROFILE | Operational reliability, controlled access and use-specific latency requirements |
| Restricted data | ESIP restricted-data questions | ADOPT + EXTEND | Separate satisfaction of readiness criteria from strength of available assurance |
| ML-oriented metadata | ESIP Preparation; Croissant | VERIFY/PROFILE | Use-pattern-specific consumption metadata and links to authoritative scientific metadata/assets |
| Recommended/non-recommended uses | ESIP Documentation | ADOPT + EXTEND | Compare declared limitations with structured specific-use requirements |
| Example code/notebooks | ESIP Documentation | ADOPT | Treat as usability evidence, not scientific fitness proof |
| Labels/targets | ESIP Preparation; Croissant/STAC label approaches | PROFILE | Apply only to relevant supervised-learning use classes |
| Governance roles | ESIP contacts; ODI; ISO 5259 informative | EXTEND | Explicit authority for declarations/overrides and feedback/correction routes |
| Rights/licence | ESIP Documentation/Access; Croissant RAI/ODRL candidates | VERIFY/PROFILE | Keep access class separate from permitted uses; no automated legal judgement |
| Assessment reproducibility | Data Director-style stable records/hashes; project-specific | EXTEND | Evidence collection snapshot + deterministic evaluation + manifest |
| Improvement guidance | ESIP direction of travel; project-specific structure | EXTEND | Link findings to actor, action, closing evidence and reassessment |

## CF integration principle
Where CF applies, a maintained CF conformance checker should be used rather than recreating CF rules. Native findings should be preserved with checker/version information and mapped transparently to assessment criteria. A CF warning is not automatically an AI-readiness failure.

## Questions the crosswalk must answer next
1. Which ESIP v1.1 questions can be satisfied directly by CF 1.13 metadata and a CF checker?
2. Which require ACDD, STAC, RO-Crate, Croissant or another existing standard?
3. Which ESIP questions are inherently declarations or domain judgements?
4. Which residual questions remain genuinely specific to use-relative water/environmental readiness?
5. Do the proposed six project dimensions remain useful after the crosswalk, or should the project adopt a different organising structure?
