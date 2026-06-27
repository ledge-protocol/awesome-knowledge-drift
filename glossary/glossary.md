# Glossary

This glossary defines terms used in this repository. Definitions should remain practical, neutral, and stable across tools, vendors, and implementation approaches.

## Core Terms

### Knowledge Drift

Knowledge Drift occurs when two or more descriptions of the same project state no longer agree.

In this repository, the descriptions usually involve **Human Intent**, **Machine Knowledge**, and **Observable Reality**.

### Project State

Project state is the condition of a software project at a particular time.

It may include intended behavior, implemented behavior, tests, documentation, configuration, architecture, operational behavior, repository history, or recorded decisions.

### Knowledge Source

A knowledge source is any artifact, system, person, or process that describes or implies something about project state.

Examples include requirements, tickets, documentation, code, tests, logs, architecture decisions, model context, generated summaries, and project memories.

### Human Intent

Human Intent is what people meant, requested, decided, expected, or agreed to.

It may be explicit, such as an acceptance criterion, or implicit, such as a team convention that is consistently applied.

### Machine Knowledge

Machine Knowledge is the project state available to an automated or AI-assisted system.

It may come from prompts, retrieved files, indexes, summaries, memories, cached information, tool output, or prior generated work.

### Observable Reality

Observable Reality is the project state that can be inspected directly.

Examples include source code, tests, build output, runtime behavior, logs, deployed configuration, repository history, and public issue or pull request state.

### Mismatch

A mismatch is a specific disagreement between knowledge sources about the same project state.

A mismatch should be narrow enough that a reader can identify what disagrees with what.

### Observable Mismatch

An observable mismatch is a mismatch supported by inspectable evidence.

Examples include a README command that fails, a test expectation that contradicts a specification, or generated code that calls an API not present in the project.

## Cases and Evidence

### Drift Case

A drift case is a concrete example of Knowledge Drift.

A strong drift case identifies the knowledge sources, the mismatch, the relevant project state, and the evidence supporting the claim.

### Evidence

Evidence is inspectable support for a claim.

Evidence may include public issue threads, pull requests, reproduction repositories, test output, papers, blog posts, technical reports, documentation, source code, logs, or documented tool behavior.

### Public Source

A public source is evidence that readers can inspect without private access.

Public sources are preferred because they allow claims to be checked without relying on private accounts.

### Source Type

Source type is the kind of public source or artifact used as evidence.

Examples include issue, pull request, discussion, documentation, paper, blog post, report, source code, test output, or reproduction.

### Evidence Quality

Evidence quality is the strength and inspectability of the evidence supporting a case.

Evidence quality should describe what readers can verify, not how serious the case is.

### Reproducibility

Reproducibility is the extent to which a case can be recreated or independently inspected from the available evidence.

Reproducibility may be full, partial, inspectable but not reproducible, or insufficiently evidenced.

### Detection Method

Detection method is how a mismatch was found.

Examples include tests, build failure, code review, runtime behavior, manual inspection, user report, or comparison between knowledge sources.

### Impact

Impact is the practical consequence of a mismatch.

Impact may include confusion, rework, failed automation, incorrect implementation, review burden, user-facing failure, security risk, data loss, or unknown consequence.

## Taxonomy Terms

### Drift Category

A drift category is a named classification for a recurring Knowledge Drift pattern.

Categories help organize cases but do not replace the evidence in the case.

### Primary Category

The primary category is the most specific category that best describes the main mismatch in a drift case.

Each case should have one primary category.

### Secondary Category

A secondary category is another category that materially helps classify a drift case.

Secondary categories should be used when a case spans more than one pattern.

### AI Context Drift

AI Context Drift occurs when the context supplied to an AI system does not reflect the current project state.

### Documentation Drift

Documentation Drift occurs when written documentation diverges from implementation, tests, configuration, or runtime behavior.

### Architecture Drift

Architecture Drift occurs when the implemented system diverges from intended architecture, boundaries, decisions, or diagrams.

### Agent Execution Drift

Agent Execution Drift occurs when an automated or semi-automated agent continues acting on stale, incomplete, or changed instructions.

### Specification Drift

Specification Drift occurs when requirements, acceptance criteria, tickets, or product specifications diverge from implementation or tests.

### Memory Drift

Memory Drift occurs when persistent project memory, summaries, notes, or cached state become stale, incomplete, or misleading.

## Supporting Terms

### Source of Truth

A source of truth is the knowledge source treated as authoritative for a decision, behavior, or claim.

Knowledge Drift often appears when more than one source is treated as authoritative for the same project state and those sources disagree.

### Stale Context

Stale context is information that was accurate at an earlier time but no longer reflects the relevant project state.

### Partial Retrieval

Partial retrieval occurs when a tool or system retrieves some relevant context but omits other information needed to understand the relevant project state.

### Persistent Memory

Persistent memory is stored project knowledge intended to influence future work beyond the immediate task or session.

Examples include saved summaries, project notes, conventions, decisions, or cached state.

### Conflicting Sources

Conflicting sources are knowledge sources that make incompatible claims about the same project state.

### Vendor Blame

Vendor blame is framing a case primarily as a failure of a specific vendor rather than as evidence of a broader drift pattern.

This repository avoids vendor blame. Vendor names may appear when necessary for accurate source attribution, but the focus should remain on the technical mismatch.
