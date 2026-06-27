# Awesome Knowledge Drift

Software teams are now building with humans, codebases, documents, and AI coding tools all carrying different versions of the project in their heads. Sometimes the README says one thing, the code does another, the architecture decision record says a third, and the AI agent confidently implements against a fourth. This repository collects evidence of that mismatch.

**Knowledge Drift** occurs when **Human Intent**, **Machine Knowledge**, and **Observable Reality** no longer describe the same project state.

This is a public research repository for documenting the problem clearly, neutrally, and with evidence.

## What is Knowledge Drift?

Modern software projects now have three realities:

1. **Human Intent**: what people meant, requested, decided, expected, or agreed to.
2. **Machine Knowledge**: what an AI assistant, coding agent, retrieval system, memory, index, or generated summary appears to know.
3. **Observable Reality**: what the code, tests, runtime behavior, logs, configuration, and repository history actually show.

Knowledge Drift happens when those realities diverge.

Concrete examples:

- An AI agent implements against stale assumptions from an earlier version of the project.
- A README says one thing, but the code does another.
- An architecture decision record says a decision was made, but the implementation changed later.
- Cursor or Claude Code loses architectural context and edits against the wrong boundary.
- A team believes authentication uses one provider, but the code uses another.
- A generated implementation satisfies the literal prompt while violating unstated human intent.
- Documentation describes an API contract that tests no longer enforce.
- A task specification changes, but an agent continues executing the older version.

These are not rare edge cases for teams using AI coding tools. They are familiar failure modes: the tool is not necessarily broken, the humans are not necessarily careless, and the code may even compile. The problem is that the project has stopped agreeing with itself.

## Why this repository exists

The mission of this repository is to collect real-world cases, discussions, papers, and examples showing that documentation, AI context, architecture decisions, and agent execution frequently diverge from reality.

The goal is not to prove that one tool is bad or that one workflow is correct. The goal is to make Knowledge Drift easier to see, classify, discuss, and study.

This repository exists to:

- Gather public examples in one place.
- Classify recurring drift patterns.
- Encourage reproducible case reports.
- Support neutral discussion across tools, vendors, and workflows.
- Help researchers and practitioners reason from evidence instead of anecdotes.

## Why this matters now

AI coding tools increase the amount of software written from compressed, retrieved, inferred, or remembered project context.

That context is often useful. It is also often incomplete.

A human reviewer may remember the product constraint but miss the generated implementation detail. An agent may see the function signature but miss the architecture rule. A model may follow an old README because the code moved faster than the docs. A team may trust a passing test suite even though the original intent was never encoded in tests.

As AI-assisted development becomes normal, the cost of stale project knowledge moves from occasional confusion to repeated execution risk. More work is being delegated to systems that can act quickly on partial truth.

Knowledge Drift is the name for that gap.

## What counts as evidence

Good evidence is specific, attributable, and inspectable.

Preferred evidence includes:

- Public bug reports, issue threads, pull requests, postmortems, or design discussions.
- Reproducible examples showing a mismatch between stated intent, machine context, and observed behavior.
- Academic papers, technical reports, or empirical studies.
- Engineering blog posts with concrete examples and enough detail to evaluate the claim.
- Tool behavior reports that include inputs, outputs, environment details, and reproduction steps.

Evidence should avoid:

- Unsupported claims.
- Vendor blame.
- Hype or solution-first framing.
- Private information, secrets, or non-public customer details.
- Broad complaints that cannot be inspected or reproduced.

Public sources are preferred. Reproducible cases are preferred. Neutral summaries are preferred.

## Current Evidence Count

As of 2026-06-27, this repository contains 56 drafted Knowledge Drift evidence case files under `cases/**`:

- AI Context Drift: 11
- Documentation Drift: 27
- Architecture Drift: 8
- Specification Drift: 5
- Agent Execution Drift: 5
- Memory Drift: 0

## Categories of drift

Initial categories are intentionally broad and may evolve as the evidence base grows.

- **AI context drift**: The context available to an AI system no longer reflects the current project state.
- **Documentation drift**: Documentation, comments, README files, or generated docs no longer match implementation or behavior.
- **Architecture drift**: Architecture decisions, diagrams, boundaries, or intended designs diverge from the implemented system.
- **Agent execution drift**: Automated or semi-automated agents execute against stale goals, incomplete instructions, or outdated assumptions.
- **Specification drift**: Requirements, tickets, acceptance criteria, or product specifications diverge from what is built or tested.
- **Memory drift**: Persistent memories, summaries, cached state, or project notes become stale, incomplete, or misleading.

See [taxonomy/knowledge-drift-taxonomy.md](taxonomy/knowledge-drift-taxonomy.md) for a fuller working taxonomy.

## How to contribute

Submit a case if you have seen this happen.

Useful contributions include:

- Adding a new case using [templates/case-template.md](templates/case-template.md).
- Adding a source using [templates/source-template.md](templates/source-template.md).
- Improving the taxonomy with clearer distinctions.
- Adding definitions to the glossary.
- Linking relevant papers, engineering blogs, discussions, or tools.
- Strengthening existing entries with better citations or reproduction details.

A good contribution does not need to be dramatic. A small, well-documented mismatch is more useful than a broad claim.

Before contributing, read [CONTRIBUTING.md](CONTRIBUTING.md).

## What this repository is not

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
