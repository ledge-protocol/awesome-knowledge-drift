# Knowledge Drift Taxonomy

This taxonomy is a working classification system. It is meant to help contributors describe evidence consistently, not to force every case into a rigid model.

## Core Model

Knowledge Drift involves at least two, and often three, diverging views of a project.

### Human Intent

Human Intent is what people meant, requested, decided, expected, or agreed to.

Examples:

- Requirements.
- Tickets.
- Design discussions.
- Architecture decisions.
- Review comments.
- Acceptance criteria.
- Team conventions.

### Machine Knowledge

Machine Knowledge is the project state available to an AI system, agent, automation, index, cache, summary, memory, or generated context window.

Examples:

- Prompt context.
- Retrieved files.
- Embeddings or indexes.
- Agent memory.
- Summaries of prior work.
- Cached dependency or API knowledge.
- Generated plans.

### Observable Reality

Observable Reality is what can be inspected in the actual project or system.

Examples:

- Source code.
- Tests.
- Build output.
- Runtime behavior.
- Logs.
- Deployed configuration.
- Repository history.
- Public issue or pull request state.

Drift appears when these three views no longer align.

## Hierarchy

### Knowledge Drift

Definition:

Knowledge Drift occurs when **Human Intent**, **Machine Knowledge**, and **Observable Reality** no longer describe the same project state.

Parent:

- None.

Children:

- AI Context Drift.
- Documentation Drift.
- Architecture Drift.
- Agent Execution Drift.
- Specification Drift.
- Memory Drift.

Examples:

- An AI agent implements against stale assumptions from an earlier version of the project.
- A README says one thing, but the code does another.
- An architecture decision record says a decision was made, but the implementation changed later.
- A task specification changes, but an agent continues executing the older version.

Non-examples:

- A bug where the intended behavior, documentation, tests, and implementation all describe the same incorrect behavior.
- A missing feature that was never requested, documented, specified, or assumed by a tool.
- A general complaint about tooling without inspectable evidence of a mismatch.

### AI Context Drift

Definition:

AI Context Drift occurs when the context supplied to an AI system does not reflect the current project state.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- The model sees outdated files.
- Retrieval omits a relevant module.
- A generated summary loses a key constraint.
- Dependency, API, or framework knowledge is stale.
- The prompt includes an obsolete design assumption.
- A generated patch targets an API that no longer exists.
- An assistant recommends a pattern removed from the codebase.

Non-examples:

- Documentation diverges from code, but no AI system, retrieval context, memory, or generated context is involved.
- An assistant gives a poor answer despite receiving complete and current project context.
- A human misunderstands current code without relying on machine-supplied context.

### Documentation Drift

Definition:

Documentation Drift occurs when written documentation diverges from implementation, tests, configuration, or runtime behavior.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- README instructions no longer work.
- API docs describe old parameters.
- Comments explain logic that has since changed.
- Generated docs are not regenerated after code changes.
- Runbooks describe an obsolete operational process.
- A command documented in the README fails on a clean checkout.
- Code review notes identify comments that contradict the implementation.

Non-examples:

- A specification, ticket, or acceptance criterion diverges from implementation, but no documentation, comments, examples, or runbooks are involved.
- Documentation is incomplete but does not conflict with implementation, tests, configuration, or runtime behavior.
- Documentation and implementation are both wrong in the same way.

### Architecture Drift

Definition:

Architecture Drift occurs when the implemented system diverges from intended architecture, boundaries, decisions, or diagrams.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- Code bypasses intended module boundaries.
- Architecture decision records are no longer followed.
- Diagrams describe components that have been removed or renamed.
- A migration is partially completed but treated as complete.
- Tests enforce behavior inconsistent with the stated design.
- A dependency graph contradicts a documented boundary.
- A pull request introduces coupling that violates an accepted decision.

Non-examples:

- Code is organized differently from someone's preference, but no intended architecture, boundary, decision, or diagram is identified.
- Documentation describes an obsolete command or parameter without an architectural boundary or design decision being involved.
- A local bug exists inside a component without changing or contradicting the intended system structure.

### Agent Execution Drift

Definition:

Agent Execution Drift occurs when an automated or semi-automated agent continues acting on stale, incomplete, or changed instructions.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- A task changes after an agent has already planned execution.
- An agent resumes from a stale summary.
- A long-running agent applies an outdated interpretation of user intent.
- The agent updates code but does not update tests or documentation that define the same behavior.
- The execution environment differs from the assumed environment.
- An agent completes work against an older issue description.
- Logs show that execution followed an obsolete plan.

Non-examples:

- An AI assistant has stale context but does not execute a task or continue acting over time.
- A scripted build fails because of a normal configuration error, with no stale or changed instruction involved.
- A human implements an outdated requirement manually without automated or semi-automated agent execution.

### Specification Drift

Definition:

Specification Drift occurs when requirements, acceptance criteria, tickets, or product specifications diverge from implementation or tests.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- Acceptance criteria are edited after implementation starts.
- Tests encode an earlier version of requirements.
- Product copy describes behavior not supported by code.
- Edge cases are clarified in comments but not reflected in the specification.
- Multiple sources define conflicting behavior.
- A pull request closes a ticket but does not satisfy updated criteria.
- Tests pass while the documented behavior remains unimplemented.

Non-examples:

- Documentation is stale, but there is no requirement, acceptance criterion, ticket, or product specification involved.
- A requirement changes and implementation is updated to match it.
- A feature request is rejected and never treated as expected behavior.

### Memory Drift

Definition:

Memory Drift occurs when persistent project memory, summaries, notes, or cached state become stale, incomplete, or misleading.

Parent:

- Knowledge Drift.

Children:

- None.

Examples:

- A project memory says a migration is complete when it is partial.
- A summary omits a rejected approach.
- A saved convention conflicts with current code.
- Long-term memory captures a temporary workaround as a durable rule.
- Cached tool state survives after the underlying files change.
- An assistant repeatedly applies an obsolete convention from memory.
- Removing or updating stale memory changes later generated output.

Non-examples:

- A one-time prompt omits relevant files, but no persistent memory, summary, note, or cached state is involved.
- A person forgets a decision without any stored project knowledge being stale or misleading.
- A generated summary is current and accurate, even if it is brief.

## Cross-Cutting Attributes

Cases may also be tagged by attributes that cut across categories.

### Source of Drift

- Stale context.
- Partial retrieval.
- Human process gap.
- Documentation lag.
- Incomplete migration.
- Tool state mismatch.
- Ambiguous ownership.
- Conflicting sources of truth.

### Detectability

- Detected by tests.
- Detected by build failure.
- Detected by code review.
- Detected by runtime behavior.
- Detected by manual inspection.
- Undetected until user impact.

### Reproducibility

- Fully reproducible.
- Partially reproducible.
- Inspectable but not reproducible.
- Anecdotal or insufficiently evidenced.

### Impact Level

- Low: minor confusion or cleanup.
- Medium: rework, failed automation, incorrect implementation, or review burden.
- High: production issue, security risk, data loss, or major reliability concern.
- Unknown: source does not provide enough information.

## Classification Guidance

When classifying a case, prefer the most specific category.

Use AI Context Drift when the mismatch centers on what an AI system knew or did not know.

Use Documentation Drift when the mismatch centers on docs, comments, examples, or runbooks.

Use Architecture Drift when the mismatch centers on system structure, boundaries, or design decisions.

Use Agent Execution Drift when the mismatch centers on autonomous or semi-autonomous execution over time.

Use Specification Drift when the mismatch centers on requirements or acceptance criteria.

Use Memory Drift when the mismatch centers on persistent summaries, memories, caches, or stored project knowledge.

If a case fits multiple categories, record secondary categories rather than forcing an artificial distinction.

## Evidence Standard

A strong taxonomy entry should identify:

- The drifting knowledge sources.
- The observable mismatch.
- The project state at the time of observation.
- The public source or reproduction.
- The limits of what can be concluded.

The taxonomy should remain open to revision as more cases are collected.
