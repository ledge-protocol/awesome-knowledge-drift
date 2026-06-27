# Documentation Listed CLI Commands That Returned Invalid Choice

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

A claude-mpm issue reports that several documented CLI commands were outdated, including an OAuth command that returned `invalid choice` and a setup command whose documented argument had changed.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-03-21
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/bobmatnyc/claude-mpm/issues/354

## Affected System or Context

claude-mpm documentation for Slack-related CLI setup commands.

## Human Intent

The documentation intended to provide executable CLI setup commands.

## Machine Knowledge

The documentation encoded older command names and arguments.

## Observable Reality

The reporter states that one documented command returned `invalid choice` and that another command should use a different setup target.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to guide setup but carried stale commands.
- Machine Knowledge vs Observable Reality: The CLI rejected at least one documented command.
- Human Intent vs Observable Reality: Users could not complete setup by copying the documented commands.

## Impact

Outdated setup commands can block users before they reach the intended workflow.

## Detection Method

Command-line execution of documented commands.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names specific documented commands and the observed CLI error or corrected command.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and find the relevant documented CLI commands.
2. Run the documented OAuth command with the relevant claude-mpm version.
3. Compare the CLI response with the documented setup flow.

Missing context or limitations:

- The issue does not list the installed claude-mpm version.

## Notes

This case is about documentation drift in a CLI setup workflow, not about the behavior of an AI model.

