# LLMs Struggled to Localize Conflicting Prompt Knowledge

## Drift Category

Primary category:

- [x] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Memory Drift

## Summary

Wang et al. study knowledge conflicts in large language models, where a model's parametric knowledge differs from non-parametric information supplied in prompt context. Their evaluation asks whether models can identify a conflict, locate the conflicting information, and present distinct answers or viewpoints.

This is an AI context drift case because the mismatch is between model-held knowledge and context supplied at inference time. The paper reports benchmark behavior, not a single deployed incident.

## Source Type

- Source type: academic paper
- Date observed: 2023-10-02
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://arxiv.org/abs/2310.00935

## Affected System or Context

Large language model question answering and reasoning workflows where prompt context may contradict the model's internal knowledge.

## Human Intent

When a prompt supplies conflicting evidence, a user or evaluator may expect the model to notice the conflict, identify what disagrees, and avoid silently collapsing the conflict into a single unsupported answer.

## Machine Knowledge

The model has parametric knowledge from training and non-parametric knowledge in the current prompt. The paper treats conflicts between those sources as a test condition.

## Observable Reality

The paper reports that evaluated models performed better at identifying the existence of conflicts than at pinpointing specific conflicting segments or producing distinct answers in conflict scenarios.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The desired behavior is explicit conflict handling, but the model's internal and contextual knowledge may not be reconciled transparently.
- Machine Knowledge vs Observable Reality: The model may have both internal and prompt-provided information available while failing to localize or preserve the conflict in its answer.
- Human Intent vs Observable Reality: The final response may be less explicit about competing information than the task calls for.

## Impact

Possible answer ambiguity, misplaced confidence, or loss of relevant context in RAG-like workflows. The paper supports this as a benchmarked model behavior, but it does not establish that every LLM system will fail in the same way.

## Detection Method

Benchmark evaluation with simulated contextual knowledge conflicts.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [x] Level 5: Academic or formal study

Evidence details:

- Paper: "Resolving Knowledge Conflicts in Large Language Models" by Yike Wang, Shangbin Feng, Heng Wang, Weijia Shi, Vidhisha Balachandran, Tianxing He, and Yulia Tsvetkov.
- The paper introduces an evaluation framework for contextual knowledge conflicts.
- The reported results distinguish conflict detection from harder tasks such as locating the conflict and presenting separate answers.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Read the arXiv paper and inspect any linked code or benchmark artifacts.
2. Run conflict prompts where retrieved or supplied context contradicts known model facts.
3. Compare whether the model identifies the conflict, localizes the conflicting spans, and answers with appropriate caveats.

Missing context or limitations:

- The paper's conflicts are benchmark scenarios; production RAG systems may add retrieval ranking, citation, or validation layers.
- Results vary by model, domain, prompt format, and conflict construction method.

## Notes

This case is about conflict handling under inconsistent context, not ordinary hallucination without supplied contradictory evidence.

