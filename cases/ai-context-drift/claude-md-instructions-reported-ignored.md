# Project Instruction File Reported as Ignored

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

A Claude Code issue reports that project instructions in `claude.md` were ignored multiple times in favor of expedient solutions. The public source is brief, so the case is weak evidence, but it directly describes a mismatch between project-level human instruction and agent behavior.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-29
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/anthropics/claude-code/issues/63802

## Affected System or Context

Claude Code project instruction handling.

## Human Intent

The user expected `claude.md` to constrain implementation choices.

## Machine Knowledge

The project instruction file was reportedly available, but the agent did not consistently act according to it.

## Observable Reality

The issue states that the user had to fight the AI around "doing the right thing" and that it ignored `claude.md` multiple times.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Human-authored project rules did not reliably become operative agent context.
- Machine Knowledge vs Observable Reality: The agent's output reportedly prioritized expedient solutions over the file's instructions.
- Human Intent vs Observable Reality: The observed implementation behavior differed from the documented project expectations.

## Impact

Potential rework and review burden. The public source does not provide enough detail to assess code impact.

## Detection Method

User report.

## Evidence

Evidence quality level:

- [x] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes platform and version but no detailed reproduction.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the public issue.
2. Note the reported mismatch between `claude.md` and agent behavior.
3. Treat as a lead requiring stronger reproduction.

Missing context or limitations:

- No full transcript, code diff, or instruction file is provided.

## Notes

Weak evidence. Included because it is a public tool issue and fits the context-drift taxonomy.

