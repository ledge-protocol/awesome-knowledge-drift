# Markdown Reference Graph Was Not Resolved as Context

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

- Documentation Drift

## Summary

A Claude Code feature request reports that markdown references in instruction files are treated as text rather than followed as context links. The result is an instruction graph where human-authored modular context exists, but only the first file is visible to the agent.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-16
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/anthropics/claude-code/issues/68729

## Affected System or Context

Claude Code instruction files, markdown links, and project context assembly.

## Human Intent

The user intended a network of instruction files to be followed through markdown or wiki-style references.

## Machine Knowledge

The agent reportedly read the first file but did not resolve referenced files, leaving downstream instructions out of the active context.

## Observable Reality

The issue describes a 30-file instruction graph and a 110-line manual bridge file maintained to compensate for missing reference traversal.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Human-authored references were intended to load related instructions, but the agent treated them as non-operative text.
- Machine Knowledge vs Observable Reality: The project contained linked files that were not included in the context path described by the issue.
- Human Intent vs Observable Reality: The modular instruction design did not produce the intended active context.

## Impact

Important constraints may be omitted when instructions are split across files, increasing the chance that the agent acts from partial project knowledge.

## Detection Method

User report from attempted use of modular instruction files.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue describes the observed behavior, alternatives tried, and a concrete use case with roughly 30 linked files.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the issue.
2. Create markdown instruction files that reference each other.
3. Observe whether the agent follows those references without an explicit bridge.

Missing context or limitations:

- The specific vault is not included.

## Notes

This is classified as AI Context Drift because the source of truth exists in project documents but is not part of the agent's effective context.

