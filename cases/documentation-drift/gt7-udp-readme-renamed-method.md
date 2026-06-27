# README Example Used a Renamed Parser Method

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

A `gt7-udp` issue reports that the README example failed to compile because it called a parser method that had been renamed. The reporter also noted that returned data had moved under a different object path.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-10
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/MacManley/gt7-udp/issues/3

## Affected System or Context

`gt7-udp` README example and parser API.

## Human Intent

The README intended to give users a working code example for reading UDP data.

## Machine Knowledge

The README encoded the old method name `read` and older data access assumptions.

## Observable Reality

Compilation failed with a message that `GT7_UDP_Parser` had no member named `read`; the reporter said it had been renamed to `readData`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The documented example no longer represented the intended current API.
- Machine Knowledge vs Observable Reality: The compiler rejected the documented method.
- Human Intent vs Observable Reality: Users following the README could not run the example.

## Impact

New users may fail at the first integration step and need to infer renamed API behavior.

## Detection Method

Compilation failure after running the README example.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes the compiler error and names the replacement method and data path.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the README example and issue.
2. Compile the example against the current parser class.
3. Confirm whether `read` exists or has been replaced by `readData`.

Missing context or limitations:

- No exact dependency version is provided.

## Notes

The evidence is specific and directly ties documentation to a compiler-observed mismatch.

