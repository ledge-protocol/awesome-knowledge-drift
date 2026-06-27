# ByteTrack Documentation Listed Parameters Not Accepted by the Class

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

A Roboflow Supervision issue reports that the tracker documentation listed `ByteTrack` constructor parameters that were not accepted by the implementation in the current package version.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-20
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/roboflow/supervision/issues/2261

## Affected System or Context

Roboflow Supervision tracker documentation and the `ByteTrack` Python API.

## Human Intent

The documentation intended to describe the supported constructor arguments for `ByteTrack`.

## Machine Knowledge

The published documentation encoded an older or incorrect parameter contract for `ByteTrack`, including arguments such as `track_thresh`.

## Observable Reality

The reporter linked the implementation and provided a minimal Python example showing that a documented argument was not accepted in Supervision `0.27.0.post2`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The documentation intended to guide users but encoded a stale API shape.
- Machine Knowledge vs Observable Reality: The documented constructor parameters did not match the source implementation.
- Human Intent vs Observable Reality: Users could not rely on the docs to instantiate the tracker.

## Impact

Users following the tracker documentation could get runtime failures or configure tracking with incorrect assumptions.

## Detection Method

User reproduction with a minimal Python example and source inspection.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the tracker docs and implementation, names the package version, and includes a minimal example using a documented argument.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and linked tracker documentation.
2. Compare the documented `ByteTrack` parameters with the linked implementation.
3. Run the issue's minimal example against the reported package version.

Missing context or limitations:

- Exact behavior may differ in later Supervision releases.

## Notes

This is a closed public issue with direct documentation and code links.

