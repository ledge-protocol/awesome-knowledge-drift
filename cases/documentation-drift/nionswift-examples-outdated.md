# Nion Swift Instrumentation Examples No Longer Worked

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

A Nion Swift instrumentation issue reports that documentation examples no longer worked. The report identifies a specific example that raised a `TypeError` and says attribute-access changes still did not make it work.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-20
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/nion-software/nionswift-instrumentation-kit/issues/380

## Affected System or Context

Nion Swift instrumentation documentation examples.

## Human Intent

The documentation intended to show working scripting examples.

## Machine Knowledge

The machine-readable examples encoded old access patterns such as dict-style assignment.

## Observable Reality

The reporter observed `TypeError: 'ScanFrameParameters' object does not support item assignment` and said the adjusted example still did nothing.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Example code represented an intended usage pattern that no longer matched the API.
- Machine Knowledge vs Observable Reality: Running the example produced an error or no effect.
- Human Intent vs Observable Reality: The promised working example did not work for the reporter.

## Impact

Broken examples can block scripting users and increase onboarding friction.

## Detection Method

User reproduction from documentation.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes the failing error and a link to the affected documentation example.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and linked docs page.
2. Run the documented scan example in a matching environment.
3. Compare behavior with the issue's reported error.

Missing context or limitations:

- Requires the relevant Nion Swift environment.

## Notes

The issue is open and labeled as documentation-related by the project.

