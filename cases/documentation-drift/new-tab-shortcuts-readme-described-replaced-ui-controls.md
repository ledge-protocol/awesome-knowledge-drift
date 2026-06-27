# README Usage Section Described Replaced UI Controls

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

A new-tab-shortcuts issue reports that the README usage section described an old UI, including a hover delete control, while the application had moved to a three-dot menu and added edit-mode behaviors not documented there.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-11
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/xjayk/new-tab-shortcuts/issues/21

## Affected System or Context

new-tab-shortcuts README usage documentation and browser-extension UI.

## Human Intent

The README intended to describe how users operate shortcut tiles.

## Machine Knowledge

The README encoded an older UI with hover deletion and omitted newer edit-mode interactions.

## Observable Reality

The issue states that delete moved to a three-dot menu and that newer edit-mode controls and keyboard behavior were missing from the README.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The usage guide no longer matched intended current interactions.
- Machine Knowledge vs Observable Reality: The documented controls differed from the current UI.
- Human Intent vs Observable Reality: Users relying on the README would look for controls that had been replaced.

## Impact

Stale UI documentation can confuse users and increase support burden for basic operations.

## Detection Method

Manual review of README usage text against current UI behavior.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue identifies the README line range and lists specific stale and missing UI behaviors.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and referenced README usage section.
2. Run or inspect the current extension UI.
3. Compare the tile controls and edit-mode behavior with the README.

Missing context or limitations:

- UI behavior may have changed again after the issue was closed.

## Notes

The issue is specific enough to inspect the stale claims without relying on broad complaints.

