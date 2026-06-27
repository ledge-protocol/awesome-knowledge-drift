# PHPUnit Group Documentation Described Removed Comma-Separated Syntax

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

A PHPUnit documentation issue reports that docs for `--group` still described separating multiple groups with commas, even though that feature had been removed in PHPUnit 12.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-04-16
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/sebastianbergmann/phpunit-documentation-english/issues/418

## Affected System or Context

PHPUnit 13 documentation for the `--group` CLI option.

## Human Intent

The CLI documentation intended to describe supported `--group` usage.

## Machine Knowledge

The documentation retained a comma-separated multi-group syntax from an earlier PHPUnit version.

## Observable Reality

The reporter states that the feature was removed in PHPUnit 12 and that the documentation for PHPUnit 13 still described it.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to document current PHPUnit behavior but retained removed syntax.
- Machine Knowledge vs Observable Reality: The documented syntax was no longer supported.
- Human Intent vs Observable Reality: Users could invoke `--group` using invalid syntax.

## Impact

Users may waste time debugging CLI filtering behavior based on outdated documentation.

## Detection Method

User attempt to use documented CLI syntax with current PHPUnit documentation.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the affected documentation and the version where the feature was removed.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the PHPUnit `--group` documentation for the affected version.
2. Check PHPUnit 12 or later CLI behavior for comma-separated group names.
3. Compare the actual behavior with the documented syntax.

Missing context or limitations:

- The issue body does not include terminal output.

## Notes

This is a closed issue in the public PHPUnit documentation repository.

