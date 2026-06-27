# Agent-Created Issue Captured PvP Feature Gap Against Reference Behavior

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [x] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Specification Drift

## Summary

An Acorn issue created through the Claude GitHub app reports that PvP combat was not implemented: the attack handler only resolved NPC attacks while the expected behavior from `eoserv Attack.cpp` included player-vs-player damage and related rules.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-26
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/do4k/Acorn/issues/13

## Affected System or Context

Acorn combat packet handler and PvP roadmap behavior.

## Human Intent

The referenced roadmap and source behavior expected PK maps and arena melee between players to work.

## Machine Knowledge

The issue reports that the handler only scanned `CurrentMap.Npcs`.

## Observable Reality

PvP attacks reportedly did nothing because there was no branch for a player on the target tile.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Expected PvP behavior was not encoded in the implementation.
- Machine Knowledge vs Observable Reality: The handler's target lookup covered NPCs only.
- Human Intent vs Observable Reality: The game did not support the referenced PvP behavior.

## Impact

Unimplemented PvP combat on PK maps and arena scoring paths.

## Detection Method

Codebase review issue created by an agent integration.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the handler file, expected behavior, acceptance criteria, and roadmap reference.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the issue.
2. Inspect `AttackUseClientPacketHandler.cs`.
3. Test attacking another player on a PK-enabled map.

Missing context or limitations:

- The issue does not include a runtime test transcript.

## Notes

This is included in Agent Execution Drift because the public issue metadata shows it was created through an agent app and records an execution/review gap for a delegated implementation stream.

