# Architecture Docs Still Described Removed Game Components

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

A Stillnight-Win3.1 PR states that documentation was updated after an audit found architecture docs and diagrams describing components whose current roles had changed or been removed.

## Source Type

- Source type: GitHub pull request
- Date observed: 2026-01-18
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/JosephSerUSP/Stillnight-Win3.1/pull/428

## Affected System or Context

Game architecture documentation and code comments.

## Human Intent

Architecture documentation was intended to describe the current roles of systems such as trait handling, map logic, and combat behavior.

## Machine Knowledge

The docs and diagrams represented older component relationships, including removed or deprecated pieces.

## Observable Reality

The PR states that `TraitManager` had been replaced by `TraitRules`, `Game_Map` was deprecated, and `BattleSystem` did not use `Game_Action` for combat resolution.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Documentation described an obsolete architecture.
- Machine Knowledge vs Observable Reality: Code roles and component names had changed.
- Human Intent vs Observable Reality: The docs no longer guided future development accurately.

## Impact

Misleading docs can cause new work to target deprecated classes or wrong subsystem boundaries.

## Detection Method

Architecture documentation audit.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The PR lists exact documentation corrections and affected files.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the PR summary and diff.
2. Compare old documentation statements with current code roles.
3. Verify deprecated JSDoc additions.

Missing context or limitations:

- The automated task source is external and not fully public.

## Notes

This case sits between documentation and architecture drift; the primary observable artifact is documentation correction.

