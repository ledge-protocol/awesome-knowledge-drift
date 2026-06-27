# Awesome Knowledge Drift

Awesome Knowledge Drift is a public research repository for collecting evidence that Knowledge Drift is a recurring problem in AI-assisted software development.

Knowledge Drift occurs when **Human Intent**, **Machine Knowledge**, and **Observable Reality** no longer describe the same project state.

This repository focuses on the problem, not a particular product, vendor, or solution.

## What is Knowledge Drift?

Software projects depend on many forms of knowledge: requirements, documentation, architecture decisions, implementation details, tests, tickets, design discussions, and the context supplied to AI systems.

Knowledge Drift happens when those sources diverge.

Examples include:

- Documentation says an API behaves one way, but the implementation behaves another way.
- An AI coding assistant acts on stale or incomplete context.
- An architecture decision record describes a design that the codebase no longer follows.
- A task specification is updated, but an execution agent continues using an older version.
- A team believes a behavior is covered by tests, but the observable system does not enforce it.

In AI-assisted development, drift can compound quickly because tools may rely on partial snapshots of project knowledge while producing changes that alter the project state again.

## Why this repository exists

The goal of this repository is to collect real-world cases, discussions, papers, and examples showing that documentation, AI context, architecture decisions, and agent execution frequently diverge from reality.

The repository exists to make the problem easier to study:

- Gather public examples in one place.
- Classify recurring drift patterns.
- Encourage reproducible case reports.
- Support neutral discussion across tools, vendors, and workflows.
- Help researchers and practitioners reason from evidence instead of anecdotes.

This is not a repository for promoting a specific fix. It is a shared evidence base for understanding the problem.

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

Contributions are welcome when they improve the quality of the evidence base.

Useful contributions include:

- Adding a new case using [templates/case-template.md](templates/case-template.md).
- Adding a source using [templates/source-template.md](templates/source-template.md).
- Improving the taxonomy with clearer distinctions.
- Adding definitions to the glossary.
- Linking relevant papers, engineering blogs, discussions, or tools.
- Strengthening existing entries with better citations or reproduction details.

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
