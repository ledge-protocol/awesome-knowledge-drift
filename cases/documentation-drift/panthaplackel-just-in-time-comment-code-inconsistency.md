# Code Changes Can Leave Method Comments Inconsistent

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

Panthaplackel, Li, Gligoric, and Mooney studied just-in-time detection of inconsistencies between natural language comments and source code changes. The paper frames the mismatch as occurring when code is modified without the corresponding comment being updated.

This is a narrow documentation drift case: the documentation unit is a source-code comment, and the observable reality is the changed method body. The paper evaluates detection over comment/code pairs, not all forms of project documentation.

## Source Type

- Source type: academic paper
- Date observed: 2020-10-04
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://arxiv.org/abs/2010.01625

## Affected System or Context

Source-code comments that describe implementation behavior, usage, preconditions, postconditions, or other method-level details.

## Human Intent

Comments are intended to help developers understand the code they accompany. When a method body changes, the intended synchronized state is that any affected comment changes with it.

## Machine Knowledge

The comment text encodes a natural-language description of the old or expected code behavior. A just-in-time detector attempts to infer whether that text still aligns with the code change.

## Observable Reality

The paper evaluates a model that correlates comments with code changes and predicts whether a comment becomes inconsistent after a method body changes. It also discusses combining inconsistency detection with comment update models.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The comment is meant to explain the current code, but may preserve a description from before the code change.
- Machine Knowledge vs Observable Reality: The comment text and changed method body can describe different behavior or constraints.
- Human Intent vs Observable Reality: Developers may rely on a comment that no longer reflects the implementation.

## Impact

Potential developer confusion, maintenance friction, and missed updates during review. The paper cites prior work connecting outdated comments with confusion and bugs, but this case should be treated as evidence of the inconsistency pattern and detection task rather than proof of a specific production failure.

## Detection Method

Just-in-time machine learning analysis of comment/code pairs before code changes are committed.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [x] Level 5: Academic or formal study

Evidence details:

- Paper: "Deep Just-In-Time Inconsistency Detection Between Comments and Source Code" by Sheena Panthaplackel, Junyi Jessy Li, Milos Gligoric, and Raymond J. Mooney.
- The paper studies whether a comment becomes inconsistent as a result of changes to the associated code body.
- The evaluation uses a corpus of comment/code pairs across comment types and compares against baseline approaches.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Read the paper and inspect any linked datasets or implementation artifacts.
2. Review the paper's task definition for comment/code inconsistency.
3. Compare method-level comments against corresponding code changes in a repository history.

Missing context or limitations:

- The case concerns comments associated with code changes, not standalone docs, runbooks, or external API documentation.
- Detection quality depends on the training corpus, comment type, and model assumptions.

## Notes

This case supports the knowledge drift pattern where a natural-language artifact remains stable while implementation changes.

