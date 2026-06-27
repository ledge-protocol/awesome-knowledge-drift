# MapControl Documentation Failed With Current Single-Project Structure

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

An Uno Platform issue reports that `MapControl` setup documentation did not work with Uno.Sdk 5.3 and the current single-project structure.

## Source Type

- Source type: GitHub issue
- Date observed: 2024-08-11
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/unoplatform/uno/issues/17904

## Affected System or Context

Uno Platform `MapControl` documentation and project setup.

## Human Intent

The documentation intended to guide users through setting up `MapControl`.

## Machine Knowledge

The docs encoded setup steps that did not account for the current Uno.Sdk and single-project structure.

## Observable Reality

The reporter states that following the docs with Uno.Sdk 5.3 and the current project structure did not allow them to set up `MapControl`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to guide current setup but described an older arrangement.
- Machine Knowledge vs Observable Reality: The documented steps failed in the current project structure.
- Human Intent vs Observable Reality: Users could not complete setup by following the docs.

## Impact

Broken setup documentation can block adoption of a platform control.

## Detection Method

User setup attempt with the current SDK and project structure.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the affected documentation page and names the SDK version and project structure involved.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked `MapControl` documentation.
2. Create or inspect a current Uno.Sdk 5.3 single-project app.
3. Attempt the documented setup steps.

Missing context or limitations:

- The issue excerpt does not include the exact setup error.

## Notes

This is a closed public issue, though stronger evidence would include command output or a minimal repository.

