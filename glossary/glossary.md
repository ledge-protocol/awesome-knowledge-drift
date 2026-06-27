# Glossary

This glossary defines terms used in this repository. Definitions should remain practical, neutral, and tied to observable software development work.

## Knowledge Drift

Knowledge Drift occurs when **Human Intent**, **Machine Knowledge**, and **Observable Reality** no longer describe the same project state.

## Human Intent

Human Intent is what people meant, requested, decided, expected, or agreed to.

It may appear in requirements, issues, pull request comments, architecture decisions, design documents, chat discussions, review feedback, or team conventions.

## Machine Knowledge

Machine Knowledge is the project knowledge available to a machine system such as an AI assistant, coding agent, search index, retrieval system, cache, generated summary, or persistent memory.

It may be incomplete, stale, compressed, inferred, or inconsistent with the current repository.

## Observable Reality

Observable Reality is the project state that can be inspected directly.

Examples include source code, tests, build output, runtime behavior, logs, deployed configuration, repository history, and public issue or pull request state.

## Drift Case

A drift case is a concrete example where two or more project knowledge sources diverge.

A strong case includes a public source, a neutral summary, and enough detail for others to inspect or reproduce the mismatch.

## Evidence

Evidence is inspectable support for a claim about Knowledge Drift.

Evidence may include public issue threads, pull requests, reproduction repositories, test output, papers, blog posts, technical reports, or documented tool behavior.

## Reproducible Case

A reproducible case is a drift case that can be recreated or inspected through documented steps.

Reproducibility may be full or partial. Some public cases are inspectable but not fully reproducible because the original environment, model version, or private context is unavailable.

## Public Source

A public source is a link or artifact that readers can inspect without private access.

Public sources are preferred because they allow contributors to verify claims and discuss the evidence without relying on private accounts.

## AI Context Drift

AI context drift occurs when the context available to an AI system no longer reflects the current project state.

## Documentation Drift

Documentation drift occurs when documentation, comments, examples, or runbooks no longer match implementation, configuration, tests, or runtime behavior.

## Architecture Drift

Architecture drift occurs when the implemented system diverges from intended architecture, boundaries, diagrams, or architecture decisions.

## Agent Execution Drift

Agent execution drift occurs when an automated or semi-automated agent acts on stale, incomplete, or changed instructions.

## Specification Drift

Specification drift occurs when requirements, tickets, acceptance criteria, or product specifications diverge from implementation, tests, or observable behavior.

## Memory Drift

Memory drift occurs when persistent memories, generated summaries, cached state, or project notes become stale, incomplete, or misleading.

## Source of Truth

A source of truth is the knowledge source treated as authoritative for a decision or behavior.

Knowledge Drift often appears when multiple sources are treated as authoritative but disagree.

## Stale Context

Stale context is information that was accurate at some earlier time but no longer reflects the current project state.

## Partial Retrieval

Partial retrieval occurs when a tool or system retrieves some relevant context but misses other information needed to understand the project state.

## Observable Mismatch

An observable mismatch is a specific, inspectable disagreement between knowledge sources.

Examples include a README command that fails, a test expectation that contradicts a specification, or generated code that calls a removed API.

## Vendor Blame

Vendor blame is framing a case primarily as a failure of a specific vendor rather than as evidence of a broader drift pattern.

This repository avoids vendor blame. Vendor names may appear when necessary for accurate source attribution, but the focus should remain on the technical mismatch.
