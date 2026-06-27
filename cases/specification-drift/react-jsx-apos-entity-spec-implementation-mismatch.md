# JSX Specification and Implementation Differed on `&apos;`

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [x] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Documentation Drift

## Summary

A React JSX issue asks whether `&apos;` is allowed because the JSX specification points to an HTML4 entity list that does not include it, while the implementation accepted and rendered it.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-18
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/react/jsx/issues/169

## Affected System or Context

JSX named character reference specification and implementation behavior.

## Human Intent

The specification intended to define which named character references are allowed.

## Machine Knowledge

The implementation used by the JSX demo accepted `&apos;`.

## Observable Reality

The reporter observed that the HTML4 list linked by the spec does not include `&apos;`, while the demo renders it as an apostrophe.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The implementation allowed a case the spec appeared to disallow.
- Machine Knowledge vs Observable Reality: Demo behavior accepted the entity.
- Human Intent vs Observable Reality: Readers could not know whether the spec or implementation was authoritative.

## Impact

Parser authors and users may implement or rely on different behavior.

## Detection Method

Manual comparison of specification link and implementation behavior.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the specification production, the HTML4 entity list, and the JSX demo.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the JSX spec production.
2. Check the linked HTML4 entity list for `&apos;`.
3. Test `&apos;` in the JSX demo.

Missing context or limitations:

- The issue asks for clarification and does not include maintainer resolution.

## Notes

This is a compact, public example of spec text and implementation behavior diverging.

