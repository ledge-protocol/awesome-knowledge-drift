# Orchestration Files Referenced a Missing Agent

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

- Agent Execution Drift

## Summary

A `grocery-agent` issue reports that multiple orchestration files referenced a `codebase_investigator` sub-agent that did not exist in the repository.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-03
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/davidstanke/grocery-agent/issues/7

## Affected System or Context

Agent-farm orchestration files and expected sub-agent inventory.

## Human Intent

The orchestration design expected a `codebase_investigator` agent to exist and be callable.

## Machine Knowledge

Several files encoded references to the missing agent.

## Observable Reality

The repository did not contain the referenced agent in `extensions/agent-farm/agents/`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Orchestration references assumed a component that was absent.
- Machine Knowledge vs Observable Reality: The file references did not match repository contents.
- Human Intent vs Observable Reality: The intended workflow could not be executed as described.

## Impact

Agent workflows can fail or require manual correction when an expected sub-agent is missing.

## Detection Method

Scheduled audit.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names affected files and the missing target directory.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the affected orchestration files.
2. Search for `codebase_investigator`.
3. Confirm whether the agent file exists.

Missing context or limitations:

- The issue does not include raw audit logs.

## Notes

This is architecture drift in the agent system's component graph.

