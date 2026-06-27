# Claude.md Memory Management Reported as Confusing

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

- Memory Drift

## Summary

A Hacker News discussion about managing Claude Code project context describes memory management as challenging: too little or too much context can waste tokens and confuse Claude. The discussion centers on `CLAUDE.md` as a mechanism for communicating repository rules and team knowledge while avoiding overload from irrelevant codebase details.

This is a draft case because it is a public discussion about a workflow and tool behavior, not a deterministic reproduction. It still captures an AI Context Drift pattern where project rules and tribal knowledge must be selectively loaded, but context window constraints and irrelevant details can make the agent's effective project knowledge unreliable.

## Source Type

- Source type: Hacker News comment
- Date observed: 2026-03-12
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://news.ycombinator.com/item?id=47350194

## Affected System or Context

Claude Code workflows using `CLAUDE.md` or similar project instruction files to carry repository rules and team knowledge.

## Human Intent

Developers intended project-level files to communicate repository rules, practices such as test-driven development, and team knowledge that should guide coding-agent behavior.

## Machine Knowledge

The agent's usable context depended on what was placed in `CLAUDE.md` and loaded into the model context. The discussion reports that too little context or too much context can both produce poor behavior.

## Observable Reality

The HN comment states that memory management is difficult and that overloading or underloading context can confuse Claude. It also says issues with `CLAUDE.md` appear to be common in that workflow.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Humans wanted stable repository rules and team knowledge to shape agent behavior.
- Machine Knowledge vs Observable Reality: The loaded context could be insufficient, excessive, or irrelevant, producing confusion rather than reliable project understanding.
- Human Intent vs Observable Reality: The project instruction mechanism required active management and did not automatically preserve a clear project model.

## Impact

Token waste, agent confusion, and additional workflow overhead for maintaining context files. The source does not document a specific incorrect patch.

## Detection Method

Public discussion and workflow report.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The comment discusses `CLAUDE.md`, context-window constraints, wasted tokens, and Claude becoming confused when context is poorly managed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the Hacker News comment.
2. Review the quoted workflow around `CLAUDE.md`.
3. Treat the report as workflow evidence, not a standalone reproduction.

Missing context or limitations:

- The linked product discussion and comment do not provide a minimal repository, full session transcript, or exact `CLAUDE.md` file.

## Notes

This case overlaps with existing project-instruction drift cases, but its emphasis is the operational tradeoff between too little context and context overload.
