# ViewModels Bypassed the Repository Layer

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [x] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- 

## Summary

A `blokp` issue reports that three ViewModels made direct API calls instead of using the repository layer, while other ViewModels followed the repository pattern.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-02-27
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/sulhimbn/blokp/issues/537

## Affected System or Context

Android/Kotlin ViewModels and repository pattern usage.

## Human Intent

The intended architecture used repositories between ViewModels and API services.

## Machine Knowledge

Several ViewModels called `ApiConfig.getApiService()` directly.

## Observable Reality

The issue lists which ViewModels used repositories and which bypassed them.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Some presentation-layer classes did not follow the intended clean architecture.
- Machine Knowledge vs Observable Reality: The code contained both compliant and non-compliant patterns.
- Human Intent vs Observable Reality: Architecture was inconsistent across equivalent components.

## Impact

Inconsistent retry logic, caching, error handling, and testability.

## Detection Method

Repository inspection.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names affected ViewModels, root cause hypothesis, impact, and acceptance criteria.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the named ViewModels.
2. Search for direct API service calls.
3. Compare with ViewModels using repositories.

Missing context or limitations:

- No automated architecture test output is attached.

## Notes

The issue says the ViewModels were likely created before the repository pattern was fully established.

