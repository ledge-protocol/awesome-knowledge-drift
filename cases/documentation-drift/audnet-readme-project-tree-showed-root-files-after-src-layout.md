# README Project Tree Showed Root Files After a `src` Layout

## Drift Category

Primary category:

- [ ] AI Context Drift
- [x] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Architecture Drift

## Summary

An Audnet issue reports that the README project-structure tree showed template folders at the repository root, while the actual code and templates lived under `src/net_audit/`.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-11
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/Elshayib/Audnet/issues/39

## Affected System or Context

Audnet README project-structure documentation.

## Human Intent

The README intended to help contributors understand the repository layout.

## Machine Knowledge

The README encoded an older flat project tree with template directories at the root.

## Observable Reality

The issue states that the actual layout placed everything under `src/net_audit/`, including templates.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The README's structure diagram no longer reflected the intended package layout.
- Machine Knowledge vs Observable Reality: The documented tree disagreed with the actual repository tree.
- Human Intent vs Observable Reality: Contributors could look for files in the wrong locations.

## Impact

Stale structure diagrams increase onboarding friction and can mislead contributors during edits.

## Detection Method

Manual comparison of README tree with repository layout.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue identifies the stale README section and the actual `src/net_audit/` layout.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and README project-structure section.
2. Inspect the repository tree for `src/net_audit/`.
3. Compare the README tree with the actual layout.

Missing context or limitations:

- The README may have been corrected after the issue closed.

## Notes

This case has specific path-level evidence of documentation drift.

