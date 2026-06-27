# Knowledge Drift Taxonomy

Knowledge Drift occurs when **Human Intent**, **Machine Knowledge**, and **Observable Reality** no longer describe the same project state.

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

## Primary Categories

### AI Context Drift

AI context drift occurs when the context supplied to an AI system does not reflect the current project state.

Common patterns:

- The model sees outdated files.
- Retrieval omits a relevant module.
- A generated summary loses a key constraint.
- Dependency, API, or framework knowledge is stale.
- The prompt includes an obsolete design assumption.

Evidence examples:

- A generated patch targets an API that no longer exists.
- An assistant recommends a pattern removed from the codebase.
- A reproduction shows that adding the missing context changes the output.

### Documentation Drift

Documentation drift occurs when written documentation diverges from implementation, tests, configuration, or runtime behavior.

Common patterns:

- README instructions no longer work.
- API docs describe old parameters.
- Comments explain logic that has since changed.
- Generated docs are not regenerated after code changes.
- Runbooks describe an obsolete operational process.

Evidence examples:

- A command documented in the README fails on a clean checkout.
- Code review notes identify comments that contradict the implementation.
- A public issue reports a docs/example mismatch.

### Architecture Drift

Architecture drift occurs when the implemented system diverges from intended architecture, boundaries, decisions, or diagrams.

Common patterns:

- Code bypasses intended module boundaries.
- Architecture decision records are no longer followed.
- Diagrams describe components that have been removed or renamed.
- A migration is partially completed but treated as complete.
- Tests enforce behavior inconsistent with the stated design.

Evidence examples:

- A dependency graph contradicts a documented boundary.
- A pull request introduces coupling that violates an accepted decision.
- An architecture document references services no longer present.

### Agent Execution Drift

Agent execution drift occurs when an automated or semi-automated agent continues acting on stale, incomplete, or changed instructions.

Common patterns:

- A task changes after an agent has already planned execution.
- An agent resumes from a stale summary.
- A long-running agent applies an outdated interpretation of user intent.
- The agent updates code but does not update tests or documentation that define the same behavior.
- The execution environment differs from the assumed environment.

Evidence examples:

- An agent completes work against an older issue description.
- A generated change passes local checks but conflicts with updated requirements.
- Logs show that execution followed an obsolete plan.

### Specification Drift

Specification drift occurs when requirements, acceptance criteria, tickets, or product specifications diverge from implementation or tests.

Common patterns:

- Acceptance criteria are edited after implementation starts.
- Tests encode an earlier version of requirements.
- Product copy describes behavior not supported by code.
- Edge cases are clarified in comments but not reflected in the specification.
- Multiple sources define conflicting behavior.

Evidence examples:

- A pull request closes a ticket but does not satisfy updated criteria.
- Tests pass while the documented behavior remains unimplemented.
- A discussion thread records a requirement change not reflected in the task.

### Memory Drift

Memory drift occurs when persistent project memory, summaries, notes, or cached state become stale, incomplete, or misleading.

Common patterns:

- A project memory says a migration is complete when it is partial.
- A summary omits a rejected approach.
- A saved convention conflicts with current code.
- Long-term memory captures a temporary workaround as a durable rule.
- Cached tool state survives after the underlying files change.

Evidence examples:

- An assistant repeatedly applies an obsolete convention from memory.
- A project summary contradicts the current repository.
- Removing or updating stale memory changes later generated output.

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

When classifying a case, prefer the most specific primary category.

Use AI context drift when the mismatch centers on what an AI system knew or did not know.

Use documentation drift when the mismatch centers on docs, comments, examples, or runbooks.

Use architecture drift when the mismatch centers on system structure, boundaries, or design decisions.

Use agent execution drift when the mismatch centers on autonomous or semi-autonomous execution over time.

Use specification drift when the mismatch centers on requirements or acceptance criteria.

Use memory drift when the mismatch centers on persistent summaries, memories, caches, or stored project knowledge.

If a case fits multiple categories, record secondary categories rather than forcing an artificial distinction.

## Evidence Standard

A strong taxonomy entry should identify:

- The drifting knowledge sources.
- The observable mismatch.
- The project state at the time of observation.
- The public source or reproduction.
- The limits of what can be concluded.

The taxonomy should remain open to revision as more cases are collected.
