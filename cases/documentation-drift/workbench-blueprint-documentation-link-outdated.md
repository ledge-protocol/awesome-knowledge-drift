# Blueprint Documentation Link Was Outdated

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

- Tooling Drift

## Summary

A Workbench issue reports that the in-app link to Blueprint documentation pointed to an outdated documentation location.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-03-07
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/workbenchdev/Workbench/issues/1018

## Affected System or Context

Workbench UI link to Blueprint compiler documentation.

## Human Intent

The UI intended to take users to current Blueprint documentation.

## Machine Knowledge

The application or documentation link encoded an old Blueprint documentation URL.

## Observable Reality

The issue identifies the outdated URL and includes screenshots showing where the link appeared in the UI.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The intended documentation destination was represented by an old link.
- Machine Knowledge vs Observable Reality: The link no longer pointed to the current documentation location.
- Human Intent vs Observable Reality: Users clicking the UI help link reached stale or wrong documentation.

## Impact

Outdated documentation links can send users to obsolete reference material and break help workflows.

## Detection Method

Manual UI inspection and link checking.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue provides the outdated URL and screenshots of the UI path to the link.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and inspect the screenshots.
2. Locate the Blueprint documentation button in the affected Workbench version.
3. Compare the linked URL with the current Blueprint documentation location.

Missing context or limitations:

- Direct reproduction requires the affected Workbench version.

## Notes

This is a link-level documentation drift case rather than stale prose.

