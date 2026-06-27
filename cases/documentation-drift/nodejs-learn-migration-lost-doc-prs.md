# Documentation Migration Lost Previously Accepted Updates

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

- 

## Summary

A Node.js Learn issue reports that after moving documentation to the current repository, previously submitted documentation PRs were not present. The drift is between the intended current documentation state and the repository content after migration.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-04-03
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/nodejs/learn/issues/24

## Affected System or Context

Node.js Learn documentation repository migration.

## Human Intent

The prior documentation changes were intended to be preserved or reapplied in the new documentation repository.

## Machine Knowledge

The repository content after transfer omitted at least two referenced PR changes.

## Observable Reality

The issue links two prior `nodejs.org` PRs and notes that one was recreated in the new repository.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Intended documentation updates were not represented in the new repository.
- Machine Knowledge vs Observable Reality: The repository state missed known prior changes.
- Human Intent vs Observable Reality: Migrated docs appeared outdated relative to accepted or proposed earlier work.

## Impact

Documentation migration can lose corrections, forcing rework and leaving users with stale content.

## Detection Method

Manual comparison between old PRs and the new repository.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the old PRs and the recreated PR.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the linked old PRs.
2. Inspect the new Node.js Learn repository.
3. Compare whether those changes are present.

Missing context or limitations:

- The issue does not state whether all linked changes were previously accepted.

## Notes

This is documentation drift caused by repository migration rather than API evolution.

