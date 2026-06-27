# LLMs Reported Not Retaining Code Review Lessons

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

A Hacker News commenter who reviews and writes code at work compared LLM coding output to inexperienced junior developers, but said LLMs do not retain lessons from previous iterations in the way human juniors do. The comment argues that even with significant parts of a codebase in context, the model remains blind to the full reality and history of the code.

This draft case captures a memory/context drift pattern in professional software work: review feedback, local practices, and historical project constraints do not reliably become durable machine knowledge across iterations.

## Source Type

- Source type: Hacker News comment
- Date observed: 2024-12-16
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://news.ycombinator.com/item?id=42434886

## Affected System or Context

LLM-assisted coding in a professional development and code-review environment.

## Human Intent

The reviewer expected repeated guidance, code review feedback, and company-specific practices to improve future coding behavior.

## Machine Knowledge

The LLM could receive parts of the codebase as context during an interaction, but reportedly did not retain examples, lessons, or project history across iterations.

## Observable Reality

The commenter reported needing to handhold LLMs repeatedly and said they did not learn from prior examples in the way human developers do.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Human feedback was expected to become reusable development guidance.
- Machine Knowledge vs Observable Reality: Context loaded for one interaction did not become durable understanding of project history or local practice.
- Human Intent vs Observable Reality: The reviewer observed repeated handholding instead of cumulative improvement.

## Impact

Ongoing review burden and limited suitability for autonomous coding in contexts where project history, local conventions, and previous feedback matter.

## Detection Method

Professional developer report in public discussion.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The comment describes workplace code review, repeated handholding, lack of durable learning from previous iterations, and incomplete understanding even when codebase context is supplied.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the Hacker News comment.
2. Note the stated comparison between human learning from review and LLM non-retention.
3. Treat as qualitative evidence requiring a stronger transcript or longitudinal study for validation.

Missing context or limitations:

- The source does not provide a specific tool, project, prompts, review comments, or diffs.

## Notes

This case may fit Memory Drift if the taxonomy later distinguishes between single-session context loss and cross-session failure to retain feedback.
