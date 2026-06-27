# README Referenced a Removed `--alpm` Option

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

An arch-hs issue reports that the README usage section documented a `--alpm` option that was no longer available in the installed command.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-02-11
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/berberman/arch-hs/issues/91

## Affected System or Context

arch-hs README usage documentation and CLI options.

## Human Intent

The README intended to document valid command-line usage.

## Machine Knowledge

The README encoded `--alpm` as an available option.

## Observable Reality

The reporter showed `arch-hs` rejecting `--alpm` as an invalid option in version `0.12.1-57`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The README's intended usage guidance was stale.
- Machine Knowledge vs Observable Reality: The documented option did not exist in the CLI.
- Human Intent vs Observable Reality: Users could not run the README command successfully.

## Impact

Stale CLI examples can break onboarding and scripted usage copied from the README.

## Detection Method

Command-line execution and comparison with README usage.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the README section and includes terminal output with the invalid-option error.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked README usage section.
2. Install the reported `arch-hs` package version.
3. Run the README command that includes `--alpm`.

Missing context or limitations:

- Package availability and behavior may vary by Arch package revision.

## Notes

The issue stayed open for several months but is now closed.

