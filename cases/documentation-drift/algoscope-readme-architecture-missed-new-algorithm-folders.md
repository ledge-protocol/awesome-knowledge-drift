# README Architecture Section Missed New Algorithm Folders

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

An AlgoScope issue reports that the README architecture section showed an outdated folder structure and omitted several algorithm and component categories added to the project.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-28
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/algoscope-hq/AlgoScope/issues/429

## Affected System or Context

AlgoScope README architecture and folder-structure documentation.

## Human Intent

The README intended to describe the current code organization.

## Machine Knowledge

The README encoded an older architecture view that omitted newer folders.

## Observable Reality

The issue lists missing `src/algorithms/` categories such as backtracking, dynamic programming, math theory, and string algorithms, along with newer components.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The architecture docs no longer represented the current project structure.
- Machine Knowledge vs Observable Reality: The documented folder tree omitted existing directories.
- Human Intent vs Observable Reality: Contributors could form an incomplete picture of available modules.

## Impact

Outdated architecture sections can slow contribution and discovery of existing code areas.

## Detection Method

Manual audit of README architecture docs against repository folders.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue identifies the README section and lists specific missing folders and components.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the README architecture section referenced by the issue.
2. Inspect the repository `src/algorithms/` and `src/components/` directories.
3. Compare the documented structure with existing folders.

Missing context or limitations:

- The issue does not include command output from listing the directories.

## Notes

This is a closed public issue with path-level mismatch details.

