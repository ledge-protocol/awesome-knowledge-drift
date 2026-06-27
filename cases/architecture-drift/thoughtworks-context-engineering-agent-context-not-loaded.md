# Coding Agent Context Was Not Guaranteed to Load

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
- Agent Execution Drift

## Summary

The Thoughtworks/Martin Fowler memo "Context Engineering for Coding Agents" describes coding-agent context configuration such as rules, skills, instructions, and project conventions. It notes uncertainty around whether an LLM will load optional context when humans expect it to.

As an architecture-drift draft case, the relevant mismatch is between intended architectural guidance and what the agent actually includes in its working context. If project conventions or architectural boundaries are stored in optional context that is not loaded, an AI-assisted change can follow a locally plausible path while missing the intended system structure.

## Source Type

- Source type: engineering blog post / memo
- Date observed: 2026-02-05
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html

## Affected System or Context

Coding-agent workflows that rely on rule files, skills, subagents, slash commands, hooks, MCP tools, or repository search to supply architecture and project conventions.

## Human Intent

Teams intend coding agents to follow project conventions and architectural guidance encoded as context configuration.

## Machine Knowledge

The agent may have access to context interfaces, but the memo distinguishes between context loaded by humans, agent software, and the LLM itself. When the LLM decides whether to load context, the source says uncertainty remains.

## Observable Reality

The memo states that context engineering can increase the probability of useful results but cannot guarantee that an LLM will execute instructions as intended. It also warns that copied context configurations can repeat or contradict existing instructions.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Architectural rules may exist, but the agent may not include them in the active context for a task.
- Machine Knowledge vs Observable Reality: The agent's active context can differ from the full set of project conventions stored in files or skills.
- Human Intent vs Observable Reality: Generated code can miss intended boundaries if the relevant architectural guidance was not loaded or was contradicted by other context.

## Impact

Potential architecture drift through inconsistent component boundaries, repeated conventions, contradictory instructions, or generated code that follows incomplete project context. The source describes the mechanism, not a named production failure.

## Detection Method

Manual inspection of coding-agent context behavior and engineering guidance from the memo.

## Evidence

Evidence quality level:

- [x] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The memo describes context configuration for coding agents, including rules, skills, subagents, hooks, and MCP.
- It explicitly discusses uncertainty over whether an LLM will load expected context and cautions that context engineering changes probabilities rather than ensuring behavior.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [ ] Partially reproducible
- [x] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Read the memo's sections on context interfaces and who decides to load context.
2. Inspect a coding-agent project that stores architecture guidance in optional rules, skills, or subagents.
3. Compare generated changes against the full intended architectural guidance and the active context reported by the tool, if available.

Missing context or limitations:

- No single repository-level architecture violation is cited.
- The case is a mechanism lead and should remain Level 1 until paired with a concrete generated-code example.

## Notes

Conservative reading: the source supports the risk that architecture guidance can be absent from an agent's active context. It does not itself prove that a specific AI-generated change introduced architecture drift.

