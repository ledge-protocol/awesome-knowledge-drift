# CLI Documentation Referenced an Encrypt Command That Was Not Available

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

A dotenvx issue reports that CLI documentation referenced an `encrypt` command, but running the command produced a CLI error saying that no such command existed.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-04-17
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/dotenvx/dotenvx/issues/790

## Affected System or Context

dotenvx CLI documentation and installed command behavior.

## Human Intent

The CLI documentation intended to describe commands available to users.

## Machine Knowledge

The documentation encoded `dotenv encrypt` as an available command.

## Observable Reality

The reporter included terminal output showing the CLI did not recognize `encrypt` and printed help for the available command set.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to guide CLI usage but listed an unavailable command.
- Machine Knowledge vs Observable Reality: The documented command did not exist in the installed CLI.
- Human Intent vs Observable Reality: Users could not perform the documented workflow.

## Impact

Users following the docs could hit immediate command failures and lose trust in the CLI reference.

## Detection Method

Command-line execution.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes terminal output for `dotenv encrypt` and `dotenv --help`.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Install the dotenvx CLI version relevant to the issue.
2. Run the documented `dotenv encrypt` command.
3. Compare the result with the documented CLI reference.

Missing context or limitations:

- The issue excerpt does not state the exact installed CLI version.

## Notes

The issue is a strong documentation-drift example because it includes direct command output.

