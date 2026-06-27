# Knowledge Drift Evidence Repository

This repository collects public evidence of **Knowledge Drift** in software projects.

Knowledge Drift occurs when two or more descriptions of the same project state no longer agree. In this repository, the descriptions usually involve:

1. **Human Intent**: what people meant, requested, decided, expected, or agreed to.
2. **Machine Knowledge**: the project state available to an automated or AI-assisted system.
3. **Observable Reality**: what can be inspected in source code, tests, build output, runtime behavior, logs, configuration, repository history, or public project discussion.

The repository is evidence-driven. It is not a benchmark, vendor scorecard, product catalogue, or argument for a single workflow.

## The Problem

Software projects are described by many knowledge sources: requirements, tickets, documentation, code, tests, architecture decisions, generated summaries, model context, and human conventions. These sources can become inconsistent as the project changes.

Examples:

- A README command no longer works on a clean checkout.
- API documentation describes a parameter that has been removed.
- An architecture decision says code should use one boundary, but implementation bypasses it.
- A task specification changes, but an automated agent continues working from the older version.
- A model receives a retrieved file set that omits the module needed to understand the requested change.
- A saved project summary says a migration is complete when the repository shows it is partial.

The relevant failure is not simply that a tool made a mistake or that documentation is stale. The failure is that two or more knowledge sources make incompatible claims about the same project state.

## Why This Matters

AI-assisted development increases the amount of work performed from compressed, retrieved, inferred, or remembered project context. That context can be useful, but it can also be incomplete or stale.

A generated change may compile while violating a requirement that was never encoded in tests. A reviewer may trust documentation that no longer matches code. An agent may act on an earlier task description after the issue has changed. A project memory may preserve an obsolete convention and influence later work.

Knowledge Drift gives these cases a common vocabulary so they can be collected, compared, and studied from evidence.

## What Counts as Evidence

Good evidence is specific, attributable, and inspectable.

Preferred evidence includes:

- Public issues, pull requests, discussions, postmortems, or design records.
- Reproducible examples showing a mismatch between knowledge sources.
- Academic papers, technical reports, or empirical studies.
- Engineering posts with concrete examples and enough detail to evaluate the claim.
- Tool behavior reports that include inputs, outputs, environment details, and reproduction steps.

Evidence should avoid:

- Unsupported claims.
- Vendor blame.
- Promotional or solution-first framing.
- Private information, secrets, credentials, or non-public customer details.
- Broad complaints that cannot be inspected or reproduced.

Public sources are preferred. Reproducible cases are preferred. Neutral summaries are preferred.

## How Cases Are Described

Each case should identify:

- The knowledge sources that disagreed.
- The specific mismatch.
- The project state at the time of observation.
- The evidence that supports the claim.
- The limits of what can be concluded.

Case files use three comparison points:

- **Human Intent vs Machine Knowledge**
- **Machine Knowledge vs Observable Reality**
- **Human Intent vs Observable Reality**

Not every case must involve all three. A useful case can show a clear mismatch between any two knowledge sources.

## Current Evidence Count

As of 2026-06-27, this repository contains 56 drafted Knowledge Drift evidence case files matching `cases/**/*.md`:

- AI Context Drift: 11
- Documentation Drift: 27
- Architecture Drift: 8
- Specification Drift: 5
- Agent Execution Drift: 5
- Memory Drift: 0

## Categories

The current taxonomy has one root concept, **Knowledge Drift**, with these direct child categories:

- **AI Context Drift**: the context supplied to an AI system does not reflect the current project state.
- **Documentation Drift**: written documentation diverges from implementation, tests, configuration, or runtime behavior.
- **Architecture Drift**: the implemented system diverges from intended architecture, boundaries, decisions, or diagrams.
- **Agent Execution Drift**: an automated or semi-automated agent continues acting on stale, incomplete, or changed instructions.
- **Specification Drift**: requirements, acceptance criteria, tickets, or product specifications diverge from implementation or tests.
- **Memory Drift**: persistent project memory, summaries, notes, or cached state become stale, incomplete, or misleading.

See [taxonomy/knowledge-drift-taxonomy.md](taxonomy/knowledge-drift-taxonomy.md) for definitions, examples, non-examples, and classification guidance.

## Repository Structure

- [cases/](cases/) contains drafted evidence cases grouped by primary category.
- [taxonomy/](taxonomy/) defines the working taxonomy.
- [glossary/](glossary/) defines stable terms used across the repository.
- [research/](research/) lists papers, engineering posts, discussions, and tools relevant to the topic.
- [templates/](templates/) contains templates for new cases and sources.
- [ledge/](ledge/) explains the repository's relationship to Ledge.

## How to Contribute

Before contributing, read [CONTRIBUTING.md](CONTRIBUTING.md).

Useful contributions include:

- Adding a new case using [templates/case-template.md](templates/case-template.md).
- Adding a source using [templates/source-template.md](templates/source-template.md).
- Improving the taxonomy with clearer distinctions.
- Adding or refining glossary definitions.
- Linking relevant papers, engineering posts, discussions, or tools.
- Strengthening existing entries with better citations or reproduction details.

A small, well-documented mismatch is more useful than a broad claim. Contributions should stay neutral and should make the evidence easier for others to inspect.

## What This Repository Is Not

This repository is not:

- A product.
- An SDK.
- A CLI.
- A benchmark suite.
- A vendor scorecard.
- A place for unverified claims.
- A promotional repository for any single company or tool.
- A solution catalogue organized around one preferred approach.

The repository should remain problem-first, evidence-driven, and useful to contributors with different views about possible solutions.

## Relationship to Ledge

This repository was started by people interested in the same problem space as Ledge, but it is not a Ledge product repository.

Ledge may be mentioned only where relevant to provenance, motivation, or related work. Contributions should not assume that Ledge is the answer to Knowledge Drift, and the repository should not be organized around promoting Ledge.

See [ledge/relationship-to-ledge.md](ledge/relationship-to-ledge.md) for the full position.
