# README Described a Static HTML Site After a Next.js Migration

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

A theshieldit.com issue reports that the README still described a pure HTML/CSS site that could be opened directly in a browser, while the project had become a Next.js 15 static export using pnpm, TypeScript, Tailwind, and build scripts.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-18
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/TheShield2594/theshieldit.com/issues/53

## Affected System or Context

theshieldit.com README setup, stack, and deployment documentation.

## Human Intent

The README intended to tell users how the site is structured and how to run or deploy it.

## Machine Knowledge

The README encoded an older no-build static-site model.

## Observable Reality

The issue states that the repository had moved to a Next.js 15, pnpm, TypeScript, Tailwind v4 workflow with build scripts.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The README no longer represented the current project model.
- Machine Knowledge vs Observable Reality: The documented no-build workflow conflicted with the current framework and toolchain.
- Human Intent vs Observable Reality: New contributors could follow the README and fail to work with the current app.

## Impact

Incorrect setup and deployment documentation can block contributors and lead to incorrect deployment assumptions.

## Detection Method

Manual comparison of README claims with current repository structure and scripts.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the stale README claims and the current stack they conflicted with.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and README around the reported setup section.
2. Inspect package files and scripts in the repository.
3. Compare the current stack with the README's no-build instructions.

Missing context or limitations:

- The README may have been updated after the issue was closed.

## Notes

This is a clear documentation drift case caused by a framework/tooling migration.

