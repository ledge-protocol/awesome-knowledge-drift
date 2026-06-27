# Tuple Documentation Described Mutable Values as Immutable

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

- Specification Drift

## Summary

A Modular issue reports that Mojo documentation described `Tuple` as immutable, while current Mojo allowed in-place mutation of tuple elements.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-19
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/modular/modular/issues/6695

## Affected System or Context

Mojo language documentation for the `Tuple` type.

## Human Intent

The language documentation intended to describe the semantics of Mojo tuples.

## Machine Knowledge

The documentation encoded the claim that `Tuple` represented an immutable tuple.

## Observable Reality

The reporter provided Mojo code in which assigning to a tuple element succeeded and appeared to mutate the value in place.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The documentation stated semantics that no longer matched the intended or implemented behavior.
- Machine Knowledge vs Observable Reality: The documented immutability claim conflicted with executable behavior.
- Human Intent vs Observable Reality: Users could misunderstand tuple semantics when writing Mojo code.

## Impact

Incorrect type-semantics documentation can lead to wrong mental models, especially for users comparing Mojo tuples with Python tuples.

## Detection Method

Runtime experiment with a small Mojo program.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the official docs, gives a Mojo version, and includes sample code demonstrating mutation.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked tuple documentation.
2. Run the sample code from the issue with the reported Mojo version.
3. Compare the mutation behavior with the documentation claim.

Missing context or limitations:

- Later documentation or language releases may have changed the wording or behavior.

## Notes

This case sits near specification drift because the stale documentation described language semantics.

