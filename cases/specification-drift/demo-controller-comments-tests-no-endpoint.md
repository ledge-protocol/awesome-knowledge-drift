# Endpoint Specification Comments and Tests Existed Without Implementation

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

A WebApplication5 issue reports that a `/hello` endpoint had specification comments and tests, but the controller method was missing implementation and requests returned 404.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-24
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/akkki98/WebApplication5/issues/14

## Affected System or Context

Spring Boot controller endpoint, tests, and specification comments.

## Human Intent

The endpoint was expected to return `hello world` with a key parameter and `key not passed` without it.

## Machine Knowledge

Unit tests and comments encoded the expected endpoint behavior.

## Observable Reality

The issue states that the endpoint was not implemented and requests returned 404.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Tests and comments represented the intended behavior.
- Machine Knowledge vs Observable Reality: The implementation did not satisfy the tests or comments.
- Human Intent vs Observable Reality: The endpoint behavior was absent at runtime.

## Impact

Failing unit tests and unusable documented endpoint behavior.

## Detection Method

Runtime request and failing tests.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes expected behavior, actual 404 behavior, reproduction steps, and test names.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Start the application with `mvn spring-boot:run`.
2. Request `/hello?key=test`.
3. Run the named unit tests.

Missing context or limitations:

- Requires repository checkout and matching Java/Maven environment.

## Notes

This is specification drift because the behavioral contract existed in tests/comments before code.

