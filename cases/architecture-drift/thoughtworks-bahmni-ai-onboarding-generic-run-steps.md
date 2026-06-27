# AI Onboarding Suggested Generic Run Steps for a Legacy System

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [x] Architecture Drift
- [ ] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- AI Context Drift

## Summary

The Thoughtworks/Martin Fowler post "Onboarding to a 'legacy' codebase with the help of AI" describes using AI tools to understand a Bahmni/OpenMRS issue. The author reports low confidence in AI-suggested application-run steps and suspected that tools with only codebase access made up generic suggestions.

This is not a case of AI generating architecture drift in a code change. It is a draft architecture-drift-adjacent case showing how incomplete AI context about a multi-repository legacy architecture can diverge from the real system structure and operational setup.

## Source Type

- Source type: engineering blog post
- Date observed: 2024-08-15
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://martinfowler.com/articles/exploring-gen-ai/09-ai-help-onboarding-codebase.html

## Affected System or Context

Bahmni/OpenMRS codebase onboarding and issue investigation using Bloop, GitHub Copilot Chat, ChatGPT, and a wiki-backed RAG bot.

## Human Intent

The developer wanted to understand the relevant repositories, domain terms, runtime setup, and testing path for a legacy healthcare application.

## Machine Knowledge

Different AI tools had different context: some had only the currently open codebase, one had wiki/documentation context, and ChatGPT relied mostly on general model knowledge.

## Observable Reality

The post describes a large multi-repository system with older technology and significant setup complexity. AI-suggested run steps were extensive and, for tools limited to codebase context, suspected to be generic or invented.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The developer needed system-level architecture and runtime knowledge; some AI tools only had partial repository context.
- Machine Knowledge vs Observable Reality: Generic run instructions did not provide high-confidence alignment with the actual legacy setup.
- Human Intent vs Observable Reality: AI assistance did not remove the need to understand repository boundaries, dependencies, and setup constraints manually.

## Impact

Potentially wasted onboarding time, incorrect setup attempts, and low-confidence test generation when AI tools do not understand the real architecture and operational topology. The post does not report that generated code was merged or caused production drift.

## Detection Method

Manual evaluation during AI-assisted codebase onboarding.

## Evidence

Evidence quality level:

- [x] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The post names the Bahmni/OpenMRS context, the investigated repository, the AI tools used, and the author's low confidence in generic run suggestions.
- It also links the related pull request used to identify the relevant codebase.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Read the post and inspect the linked Bahmni/OpenMRS repository and pull request.
2. Compare AI-generated setup advice against official Bahmni/OpenMRS documentation and repository run scripts.
3. Treat any mismatch as AI context drift unless a concrete AI-generated code change is found.

Missing context or limitations:

- The exact prompts and all tool outputs are not fully reproduced.
- This is an AI-assisted architecture-understanding case, not direct evidence of AI-caused architecture drift in committed code.

## Notes

Conservative reading: useful as a lead for architecture drift caused by incomplete AI context, but not strong enough to claim AI-assisted development introduced architectural defects.

