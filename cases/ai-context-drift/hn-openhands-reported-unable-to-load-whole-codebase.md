# OpenHands Reported Unable to Load Whole Codebase Context

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

A Hacker News commenter reported trying OpenHands with GPT-4o on a TypeScript/React project. They found it useful for writing new code, but said it struggled to make changes when the project contained a lot of repetitive code because it could not load the whole codebase into the context window.

The report describes the agent compensating with search loops and localized snippets, which may fail to preserve enough project-wide context for reliable maintenance changes. This is a public discussion case, not a reproducible bug report.

## Source Type

- Source type: Hacker News comment
- Date observed: 2025-01-26
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://news.ycombinator.com/item?id=42830215

## Affected System or Context

OpenHands using GPT-4o on a TypeScript/React project created with Vite.

## Human Intent

The developer expected the agent to help modify an existing generated project, including making changes across repetitive code.

## Machine Knowledge

The agent reportedly could not hold the whole codebase in the context window and instead relied on searching files, showing nearby lines, and performing search-and-replace style edits.

## Observable Reality

The commenter observed that OpenHands was decent at new-code generation but had difficulty making later changes in a project with repetitive code.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The maintenance task required broader codebase understanding than the model could keep active.
- Machine Knowledge vs Observable Reality: Local grep results and nearby snippets did not fully substitute for the whole project context.
- Human Intent vs Observable Reality: The agent's edit workflow was less effective after the project moved from creation to modification.

## Impact

Potentially unreliable maintenance edits and reduced productivity when the relevant change spans repeated or similar code. The source does not state that a faulty patch was merged.

## Detection Method

Developer report after trying the tool for several days.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The HN comment names OpenHands, GPT-4o, the project stack, and the observed search-based compensation for context-window limits.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the Hacker News comment.
2. Note the named tool, model, and project type.
3. Treat as a lead for reproducing maintenance edits on a repetitive TypeScript/React codebase.

Missing context or limitations:

- No repository, prompts, terminal log, or final diffs are included.

## Notes

This case is about effective context availability, not necessarily literal forgetting. The reported workaround was search-driven local context gathering.
