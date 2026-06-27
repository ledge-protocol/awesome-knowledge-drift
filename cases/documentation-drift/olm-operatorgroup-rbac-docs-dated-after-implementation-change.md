# OperatorGroup RBAC Documentation Was Dated After an Implementation Change

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

An OLM docs issue reports that OperatorGroup RBAC documentation was outdated after an implementation commit changed the relevant behavior.

## Source Type

- Source type: GitHub issue
- Date observed: 2021-11-05
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/operator-framework/olm-docs/issues/198

## Affected System or Context

Operator Lifecycle Manager documentation for OperatorGroup RBAC behavior.

## Human Intent

The documentation intended to explain how OperatorGroup RBAC works for users installing operators.

## Machine Knowledge

The documentation retained behavior from before a referenced implementation commit.

## Observable Reality

The issue links the dated documentation, references the implementation commit, and includes reproduction steps for installing OLM and an operator.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs intended to describe current RBAC behavior but reflected older behavior.
- Machine Knowledge vs Observable Reality: The documented RBAC behavior diverged from the implementation after the commit.
- Human Intent vs Observable Reality: Users could misunderstand permissions created during operator installation.

## Impact

Outdated RBAC documentation can create incorrect expectations about generated permissions and operator behavior.

## Detection Method

Reproduction steps involving OLM and an operator installation.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue links the affected documentation and implementation commit and starts a concrete reproduction path.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the linked OperatorGroup RBAC documentation.
2. Inspect the referenced operator-lifecycle-manager commit.
3. Follow the issue's installation path to observe current RBAC behavior.

Missing context or limitations:

- Full reproduction requires a Kubernetes or OpenShift environment suitable for OLM.

## Notes

Although the issue was opened in 2021, it is closed and remains a public example of documentation lagging an implementation change.

