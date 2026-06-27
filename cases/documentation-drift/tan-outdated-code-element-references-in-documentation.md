# Code Element References Remained After Source Elements Were Removed

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

- Tooling Drift

## Summary

Tan, Wagner, and Treude studied outdated code element references in GitHub README and wiki documentation. Their approach flags a reference when the documentation still contains a code element that existed when the documentation was last updated, but the current source code no longer contains any matching instance.

This is a documentation synchronization case: the paper documents a measurable mismatch between repository documentation and the source code history. The case should not be read as covering every kind of documentation drift, because the method focuses on code element references that disappear from source code.

## Source Type

- Source type: academic paper
- Date observed: 2022-12-02
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://arxiv.org/abs/2212.01479

## Affected System or Context

GitHub project documentation, especially README files and wiki pages that mention code elements such as functions, variables, classes, or build identifiers.

## Human Intent

Project documentation is intended to describe usable project concepts and code-facing instructions. In the paper's motivating examples, documentation continued to mention code elements after source changes had removed or renamed them.

## Machine Knowledge

The documentation retained textual references to code elements. The paper's detector compared those references with source-code snapshots from the time the documentation was updated and the current source revision.

## Observable Reality

The study reports that, across more than 3,000 GitHub projects, many projects had at least one moment in their history where documentation referenced a code element that was no longer present in source code. The paper also reports submitted GitHub issues for detected examples, some of which led to documentation fixes.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: Documentation intended to guide users or contributors, but retained references that could no longer be matched to current source elements.
- Machine Knowledge vs Observable Reality: Documentation text and current source code disagreed about whether a code element still existed.
- Human Intent vs Observable Reality: Users reading the documentation could be pointed at code-facing names that had been removed or renamed.

## Impact

Potential confusion for users and maintainers, stale setup or API references, and additional review or maintenance work. The paper supports these as plausible effects of outdated references, but impact varies by project and reference.

## Detection Method

Historical repository analysis comparing documentation references against source-code revisions.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [x] Level 5: Academic or formal study

Evidence details:

- Paper: "Detecting Outdated Code Element References in Software Repository Documentation" by Wen Siang Tan, Markus Wagner, and Christoph Treude.
- The paper defines outdated references by checking whether a code element existed when documentation was updated and later disappeared from source code while remaining in the documentation.
- The paper reports a large-scale GitHub analysis and includes motivating examples such as `google/glog`.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Read the paper and its linked appendix or implementation artifacts.
2. Inspect the documented GitHub examples and issue links referenced by the paper.
3. Re-run or adapt the detection approach against a selected GitHub repository history.

Missing context or limitations:

- The detector is limited to code element references that can be extracted and matched by the method.
- Some references may be legitimate historical notes, changelog entries, or user-facing compatibility guidance rather than stale documentation.

## Notes

This case is strongest as evidence for a specific documentation/source-code synchronization failure mode. It should not be generalized to all documentation quality issues.

