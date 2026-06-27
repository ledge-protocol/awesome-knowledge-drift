# AI-Assisted Coding Produced Locally Plausible Code

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [x] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- AI Context Drift

## Summary

Addy Osmani's post "The 70% problem: Hard truths about AI-assisted coding" describes a recurring pattern where AI-assisted development can make engineers feel more productive while leaving the harder work of integration, quality, and maintainability unresolved.

As a Knowledge Drift case, this is a draft lead rather than a verified incident. The architectural-drift interpretation is that an assistant may generate code that is locally plausible but insufficiently aligned with the larger system's intended architecture, requiring human review to reconcile the output with long-term maintainability.

## Source Type

- Source type: engineering blog post
- Date observed: 2024-12-04
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://addyo.substack.com/p/the-70-problem-hard-truths-about

## Affected System or Context

AI-assisted software development workflows using coding assistants to generate or modify application code.

## Human Intent

Developers intend to use AI assistance to accelerate useful software delivery without sacrificing system quality, maintainability, or architectural coherence.

## Machine Knowledge

The assistant's useful knowledge is bounded by prompt context, retrieved code context, and model training. The draft interpretation is that this knowledge may be enough for local implementation but not enough for system-level architecture decisions.

## Observable Reality

The post describes a field pattern: AI assistance may help reach an initial implementation quickly, while the remaining work involves judgment, integration, testing, review, and maintainability checks.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Human expectations include architectural fit and durable maintainability; the AI system may optimize for the immediate coding request.
- Machine Knowledge vs Observable Reality: Generated code can appear correct locally while still needing validation against the actual codebase and system constraints.
- Human Intent vs Observable Reality: Productivity gains do not necessarily imply that the resulting software architecture improved.

## Impact

Potential review burden, rework, and accumulation of locally reasonable code that does not fully match the system's intended architecture. The source does not provide a reproducible production incident, so impact should not be overstated.

## Detection Method

Author field observation and engineering reflection.

## Evidence

Evidence quality level:

- [x] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The public Substack archive metadata identifies the post title, author, publication date, and summary describing the gap between reported AI-assisted productivity and observed software improvement.
- The source is a broad engineering reflection, not a specific inspectable repository incident.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [x] Unknown

Steps or inspection path:

1. Read the public post.
2. Treat architectural drift as a hypothesis about the described development pattern.
3. Look for linked or follow-up examples with concrete code review or repository evidence before promoting this beyond a draft lead.

Missing context or limitations:

- No specific repository, pull request, or failing architecture check is cited in this draft.
- This case should remain Level 1 unless stronger implementation evidence is added.

## Notes

Conservative reading: this is not proof that AI assistance caused architecture drift in a named system. It is a public engineering-blog lead about a plausible mechanism for architecture drift.

