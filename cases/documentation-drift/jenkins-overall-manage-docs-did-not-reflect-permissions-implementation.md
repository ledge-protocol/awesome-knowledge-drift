# Overall/Manage Documentation Did Not Reflect Permission Implementation

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

A jenkins.io issue reports that the documentation for `Overall/Manage` permissions did not reflect the behavior in Jenkins core.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-04-20
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/jenkins-infra/jenkins.io/issues/9066

## Affected System or Context

Jenkins security/access-control documentation for permissions.

## Human Intent

The documentation intended to describe the permission model users should configure.

## Machine Knowledge

The published documentation encoded permission behavior that the reporter said was not aligned with Jenkins core.

## Observable Reality

The issue links the affected documentation page and points to Jenkins core as the source of reality for the permission behavior.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to describe current permissions but carried stale wording.
- Machine Knowledge vs Observable Reality: The documentation did not reflect the implementation in Jenkins core.
- Human Intent vs Observable Reality: Administrators could misunderstand what access a permission grants.

## Impact

Permission documentation drift can create configuration mistakes or incorrect security expectations.

## Detection Method

Manual comparison of documentation with implementation behavior.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the affected permissions page and the expected source of truth in Jenkins core.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked Jenkins permissions documentation.
2. Inspect the linked Jenkins core behavior or related source.
3. Compare the permission description with the implemented behavior.

Missing context or limitations:

- The issue excerpt does not include a minimal Jenkins configuration reproducer.

## Notes

This is a documentation drift case with potential security relevance, but the case should not overstate impact beyond the public issue.

