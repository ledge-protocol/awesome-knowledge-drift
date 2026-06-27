# Codex Instructions Were Nested Under the Wrong TOML Table

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

- Tooling Drift

## Summary

A nono-packs issue reports that a `toml_block` directive appended `developer_instructions` after the last TOML table, causing the key to be parsed inside that table rather than at root. The intended instruction context therefore did not reach Codex as intended.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-22
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/always-further/nono-packs/issues/52

## Affected System or Context

nono-packs Codex configuration generation and `developer_instructions` placement.

## Human Intent

The user intended root-level Codex `developer_instructions` to be inserted at the top or otherwise outside nested MCP server tables.

## Machine Knowledge

Codex would read configuration according to TOML structure. If the key lands under `mcp_servers.filesystem`, it is not root-level developer instruction context.

## Observable Reality

The issue provides a minimal TOML example where appending a bare key after `[mcp_servers.filesystem]` makes it part of that table.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Instructions were intended as global Codex context but became nested configuration data.
- Machine Knowledge vs Observable Reality: The parsed TOML structure differed from the apparent visual intention of the appended block.
- Human Intent vs Observable Reality: The generated config did not place the instruction where intended.

## Impact

Codex may not receive intended instructions, causing later behavior to proceed from incomplete context.

## Detection Method

Manual inspection of generated TOML structure and a minimal reproduction.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes exact TOML before and after insertion and explains the parse result.

## Reproducibility

Reproducibility status:

- [x] Fully reproducible
- [ ] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the minimal TOML example in the issue.
2. Parse it with a TOML parser.
3. Confirm `developer_instructions` belongs to the last table, not the root.

Missing context or limitations:

- The issue does not show a complete Codex session affected by the misplaced key.

## Notes

This is a strong early example of machine-readable configuration drifting from human intent.

