# CLI Business Logic Drifted Outside Shared SDK Services

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [x] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Specification Drift

## Summary

An `auths` issue reports that business rules lived in the CLI and agent front door rather than shared SDK services, violating the project's own architecture rule. The issue connects duplicated storage-path logic to shipped bugs.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-23
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/auths-dev/auths/issues/350

## Affected System or Context

`auths` CLI, agent front doors, SDK/Core service boundary, and storage-path resolution.

## Human Intent

Project instructions stated that business logic should live in SDK/Core, not the CLI presentation layer.

## Machine Knowledge

CLI command files reportedly performed config parsing, validation, lifecycle logic, and storage-path resolution directly.

## Observable Reality

The issue states that duplicated storage-path resolution caused commands to ignore a global `--repo` flag and act on the wrong store.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The implementation placed logic where the architecture rule said it should not live.
- Machine Knowledge vs Observable Reality: Existing guards caught imports but not inline domain logic.
- Human Intent vs Observable Reality: The boundary violation produced real command behavior drift.

## Impact

Shipped bugs, possible destructive action against the wrong store, duplicated logic, and incomplete CI enforcement.

## Detection Method

Capability-mapping audit and source inspection.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue lists affected commands, the architecture rule, current guard limitation, and acceptance criteria.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the issue.
2. Inspect the named CLI command files.
3. Compare against the `CLAUDE.md` architecture rule and SDK capability surface.

Missing context or limitations:

- Some audit details are summarized in the issue rather than attached as raw output.

## Notes

The case is framed as architecture drift, not individual fault.

