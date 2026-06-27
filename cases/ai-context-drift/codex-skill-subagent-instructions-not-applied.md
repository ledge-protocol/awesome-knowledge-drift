# Skill Instructions to Use Subagents Were Not Applied

## Drift Category

Primary category:

- [x] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Agent Execution Drift

## Summary

A Codex CLI issue reports that a selected skill's instruction to use subagents was not acted on unless the user repeated the same instruction in the prompt. The public report frames the mismatch as a difference between loaded skill context and the execution strategy actually chosen by the agent.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-19
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/openai/codex/issues/23496

## Affected System or Context

Codex CLI skill execution and subagent workflow selection.

## Human Intent

The skill author intended the workflow to use subagents when the task matched the skill. The issue states that repeating "use subagents" in the user prompt should not be necessary when the selected skill already says so.

## Machine Knowledge

The agent had access to loaded skill instructions, but the reported behavior suggests that instruction was not treated as sufficient execution context.

## Observable Reality

The reporter observed two different outcomes: without prompt-level repetition, the work ran locally in the main agent; with repeated prompt text, subagents were spawned.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Skill-authored workflow intent was present but apparently not promoted into operative execution context.
- Machine Knowledge vs Observable Reality: The expected subagent execution path did not occur in the reported first run.
- Human Intent vs Observable Reality: The requested skill workflow and observed execution strategy differed.

## Impact

The same task can silently run with different execution strategy depending on whether a user duplicates instructions. Impact is workflow brittleness and possible missed review or decomposition steps.

## Detection Method

User report comparing two prompts against the same skill.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes version, platform, YOLO mode command, expected behavior, and reproduction steps.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the GitHub issue.
2. Create a skill that requires subagents.
3. Compare execution with and without repeating the subagent instruction in the prompt.

Missing context or limitations:

- The public report does not include the full skill files or transcript.

## Notes

This is treated as a reported context-propagation mismatch, not a general claim about all skill workflows.

