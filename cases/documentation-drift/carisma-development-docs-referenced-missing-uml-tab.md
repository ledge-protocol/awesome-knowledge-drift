# Development Documentation Referenced a Missing UML Properties Tab

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

- 

## Summary

A CARiSMA Tool issue reports that the development documentation instructed users to select a `UML` entry in the Properties tab, but that entry was not present in the actual UI.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-02
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/CARiSMA-Tool/carisma-tool/issues/77

## Affected System or Context

CARiSMA Tool development documentation for adding tag values in a Papyrus profile project.

## Human Intent

The documentation intended to guide developers through adding tag values in the UI.

## Machine Knowledge

The documentation encoded a UI path that included selecting `UML` under the Properties tab.

## Observable Reality

The reporter states that the documented path did not work because there was no `UML` item in the Properties tab.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The intended workflow was represented by outdated UI instructions.
- Machine Knowledge vs Observable Reality: The documented UI element was absent.
- Human Intent vs Observable Reality: Users could not complete the documented workflow as written.

## Impact

Outdated UI instructions can block contributors trying to follow the development documentation.

## Detection Method

Manual attempt to follow the documentation.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the affected documentation section and quotes the relevant UI instruction.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked development documentation.
2. Follow the tag-value workflow in the relevant Papyrus environment.
3. Check whether the documented `UML` selection exists.

Missing context or limitations:

- Verification requires a matching CARiSMA/Papyrus UI environment.

## Notes

The public report is concise but identifies a specific stale UI instruction.

