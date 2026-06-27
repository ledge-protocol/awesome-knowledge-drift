# Report Documentation Was Outdated Because a Reference Entry Was Missing

## Drift Category

Primary category:

- [ ] AI Context Drift
- [x] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Tooling Drift

## Summary

An OpenVox docs issue reports that report documentation was outdated because a `report` entry was missing from the documentation reference-generation code.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-12
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/OpenVoxProject/openvox-docs/issues/187

## Affected System or Context

OpenVox generated report documentation.

## Human Intent

The documentation site intended to include current reference documentation for reports.

## Machine Knowledge

The docs generation configuration omitted the `report` reference entry.

## Observable Reality

The issue links the affected docs page and the source file where the missing entry caused the generated documentation to be stale.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The intended docs coverage was not represented in the generation configuration.
- Machine Knowledge vs Observable Reality: The generated docs did not include the current report reference.
- Human Intent vs Observable Reality: Readers saw outdated report documentation.

## Impact

Generated documentation can silently fall behind when generation inputs omit current references.

## Detection Method

Manual inspection of generated docs and documentation-generation source.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links both the outdated docs page and the source file missing the relevant entry.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the affected report documentation page.
2. Inspect the linked `puppet_doc.rb` reference-generation file.
3. Confirm whether the `report` entry is present in the docs-generation source for the relevant revision.

Missing context or limitations:

- The public issue does not include a full regeneration log.

## Notes

This case is useful because it points to a docs-generation source of drift, not only a stale prose page.

