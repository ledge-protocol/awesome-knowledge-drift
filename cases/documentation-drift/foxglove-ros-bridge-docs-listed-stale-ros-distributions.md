# ROS Bridge Docs Listed Stale Supported Distributions

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

A Foxglove SDK issue reports that the docs listed Humble and Iron as supported ROS distributions, while the repository README indicated Jazzy and Kilted should be listed.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-02-03
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/foxglove/foxglove-sdk/issues/856

## Affected System or Context

Foxglove ROS bridge documentation and supported ROS distribution list.

## Human Intent

The docs intended to tell users which ROS distributions were supported.

## Machine Knowledge

The published docs retained an older supported-distribution list.

## Observable Reality

The issue states that the current README listed newer distributions that should replace the docs list.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to describe support status but contained stale release names.
- Machine Knowledge vs Observable Reality: The docs and README disagreed about supported ROS distributions.
- Human Intent vs Observable Reality: Users could target obsolete or wrong support combinations.

## Impact

Stale support matrices can mislead installation and compatibility decisions.

## Detection Method

Manual comparison between docs and repository README.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the outdated and expected ROS distribution names and links the affected docs.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked docs page.
2. Open the repository README for the same component.
3. Compare the supported ROS distribution lists.

Missing context or limitations:

- The issue does not include a build or installation failure.

## Notes

This is documentation drift between two public documentation surfaces in the same project context.

