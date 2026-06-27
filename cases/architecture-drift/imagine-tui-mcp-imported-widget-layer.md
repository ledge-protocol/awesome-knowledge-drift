# MCP Layer Imported a Widget Layer Outside Its Declared Boundary

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

- Documentation Drift

## Summary

An `imagine-tui` issue reports that `internal/mcp/server.go` imported `internal/widget/`, violating dependency boundaries documented in `CLAUDE.md`.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-03-14
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/joncooper/imagine-tui/issues/18

## Affected System or Context

Go package layering between `internal/mcp`, `internal/widget`, and `internal/dom`.

## Human Intent

The architecture section said `internal/mcp/` depends on `dom/` only.

## Machine Knowledge

The actual code imported `internal/widget` and called widget catalog functions from the MCP server.

## Observable Reality

The issue names the import line and function use sites and explains the undeclared dependency chain.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Declared package dependencies did not match the code dependency.
- Machine Knowledge vs Observable Reality: The import graph showed an upward dependency not present in docs.
- Human Intent vs Observable Reality: Architecture documentation and implementation disagreed.

## Impact

Layering becomes harder to reason about; future changes may assume an MCP boundary that no longer exists.

## Detection Method

Manual source inspection against architecture docs.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue gives the exact file, import, documented rule, and three possible resolution paths.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect `CLAUDE.md` for allowed dependencies.
2. Inspect `internal/mcp/server.go`.
3. Confirm whether it imports `internal/widget`.

Missing context or limitations:

- Requires repository state from the time of the issue.

## Notes

One proposed fix is to update docs if the dependency is intentional, which would turn drift into an explicit architecture change.

