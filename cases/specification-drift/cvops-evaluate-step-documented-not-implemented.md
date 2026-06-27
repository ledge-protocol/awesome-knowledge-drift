# Evaluate Step Was Documented but Not Implemented

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [x] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Documentation Drift

## Summary

A CVOps issue reports that an `evaluate` step was documented as first-class but had no implementation in `packages/steps`.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-16
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/YehudaBriskman/CVOps/issues/79

## Affected System or Context

Worker training service documentation and step implementation registry.

## Human Intent

The system design expected an evaluate step that runs evaluation on a held-out commit and stores metrics.

## Machine Knowledge

Documentation referenced `step.evaluate`, but no corresponding step implementation existed.

## Observable Reality

The issue states "documented, not implemented" and references the docs and missing code location.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Documentation expressed an intended capability.
- Machine Knowledge vs Observable Reality: The implementation package lacked the capability.
- Human Intent vs Observable Reality: The training workflow could not execute the documented step.

## Impact

Model evaluation cannot be treated as first-class until the implementation and registry exist.

## Detection Method

Gap review between docs and source tree.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names `docs/services/worker-training.md`, `packages/steps`, and acceptance criteria.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the referenced documentation.
2. Search `packages/steps` for an evaluate step.
3. Check whether it is registered.

Missing context or limitations:

- The issue does not include a command transcript.

## Notes

This is a direct documented-feature-versus-code absence case.

