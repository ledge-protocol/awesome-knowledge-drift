# README Claimed Angular 21 Compatibility That Did Not Work

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

An ngx-quill issue reports that the README compatibility table claimed Angular v21 compatibility for ngx-quill 29 and later, but the reporter found that Angular v21 did not work with ngx-quill 31.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-22
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/KillerCodeMonkey/ngx-quill/issues/2066

## Affected System or Context

ngx-quill README compatibility documentation for Angular versions.

## Human Intent

The README intended to communicate supported Angular and ngx-quill version combinations.

## Machine Knowledge

The compatibility table encoded Angular v21 as compatible with ngx-quill versions at or above 29.

## Observable Reality

The reporter states that Angular v21 did not actually work with ngx-quill 31.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The support matrix presented a compatibility claim that did not match observed use.
- Machine Knowledge vs Observable Reality: The documented version combination failed.
- Human Intent vs Observable Reality: Users could select incompatible dependency versions based on the README.

## Impact

Incorrect compatibility documentation can waste upgrade time and cause dependency-resolution or runtime failures.

## Detection Method

User upgrade or installation attempt.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the README compatibility section and states the failing version combination.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked compatibility table.
2. Create or inspect an Angular v21 project using ngx-quill 31.
3. Compare observed compatibility with the README matrix.

Missing context or limitations:

- The issue excerpt does not include exact installation logs.

## Notes

This is closed public evidence of stale dependency compatibility documentation.

