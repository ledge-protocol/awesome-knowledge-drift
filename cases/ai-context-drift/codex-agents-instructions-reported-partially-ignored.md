# Project AGENTS Instructions Reported as Partially Ignored

## Drift Category

Primary category:

- [x] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Agent Execution Drift

## Summary

A Codex issue reports that the Codex app stopped following a specific Git workflow instruction from a project-level `AGENTS.md` file while still following surrounding instructions. The reported mismatch is between durable project instructions and the agent's actual execution behavior.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-24
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/openai/codex/issues/29879

## Affected System or Context

Codex app project-level instruction handling.

## Human Intent

The user intended `AGENTS.md` to govern testing, validation, git workflow, and documentation behavior across projects.

## Machine Knowledge

The project instruction file reportedly included a Git workflow section requiring atomic commits and specific commit-related constraints.

## Observable Reality

The issue reports that the agent used git for inspection but no longer attempted the requested commit workflow until challenged, while other instructions around the same section were followed.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The project-level instruction file was meant to be durable context.
- Machine Knowledge vs Observable Reality: The reported execution followed some nearby instructions but not the Git workflow instruction.
- Human Intent vs Observable Reality: The requested commit workflow did not occur until the user challenged the agent.

## Impact

Project workflows that depend on durable agent instructions can silently lose specific constraints while appearing to follow others.

## Detection Method

User report from repeated project use.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes Codex app version, platform, the relevant `AGENTS.md` excerpt, and observed behavior.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the issue.
2. Review the quoted `AGENTS.md` instructions.
3. Compare the reported execution behavior with the Git workflow instruction.

Missing context or limitations:

- The issue does not include a full transcript or deterministic reproduction steps.

## Notes

Evidence is public but should be treated as weak until a minimal public reproduction or transcript is attached.
