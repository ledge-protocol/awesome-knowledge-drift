# README Setup Instructions Did Not Run the Application

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

A DevMatch issue reports that the README did not accurately reflect the project structure and that following the documented setup process did not result in a running application.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-12
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/jayantaryan/DevMatch/issues/2

## Affected System or Context

DevMatch README setup and onboarding instructions.

## Human Intent

The README intended to let a new contributor clone, configure, and run the application.

## Machine Knowledge

The README contained setup steps, dependency information, and structure assumptions that the issue says were incomplete or stale.

## Observable Reality

The reporter states that following the setup instructions from a clean clone failed or required undocumented steps.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The README no longer encoded all steps needed for successful setup.
- Machine Knowledge vs Observable Reality: Commands and configuration did not match the current project.
- Human Intent vs Observable Reality: A new contributor could not run the app using README instructions alone.

## Impact

Contributor onboarding friction and repeated support burden.

## Detection Method

Clean-environment setup attempt.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes reproduction steps, expected behavior, and suggested improvements.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Clone the repository.
2. Follow the README setup steps.
3. Attempt to start the application and compare with the issue.

Missing context or limitations:

- The issue does not include exact command output.

## Notes

Evidence is public but would be stronger with terminal logs from a clean setup.

