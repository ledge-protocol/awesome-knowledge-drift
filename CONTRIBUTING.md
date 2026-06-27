# Contributing

Thank you for helping build a public evidence base for Knowledge Drift in AI-assisted software development.

This repository values evidence over opinion. Contributions should help readers inspect, reproduce, classify, or better understand a concrete drift pattern.

## Contribution principles

- **Evidence first**: Prefer concrete cases, citations, reproduction steps, and observable behavior.
- **Neutral tone**: Describe what happened without assigning blame or intent.
- **Public sources preferred**: Link to public issues, pull requests, papers, posts, discussions, or documentation whenever possible.
- **Reproducible cases preferred**: Include enough detail for others to inspect the mismatch.
- **No vendor blame**: The goal is to understand a class of problems, not to score vendors.
- **No hype**: Avoid claims that overgeneralize from limited evidence.
- **No solution-first framing**: Do not organize a contribution around selling a tool or approach.

## What to contribute

You can contribute:

- Case studies of Knowledge Drift.
- Public sources such as papers, engineering blogs, or discussions.
- Taxonomy improvements.
- Glossary entries.
- Better links, summaries, and citations.
- Corrections to existing entries.

## Adding a case

Use [templates/case-template.md](templates/case-template.md) as the starting point.

A strong case usually includes:

- A short neutral title.
- The drift category or categories.
- A public source link.
- A clear description of the mismatch.
- The human intent, machine knowledge, and observable reality involved.
- Steps to reproduce or inspect the behavior, if possible.
- Impact and limitations.

Place cases in the closest category under `cases/`. If a case spans multiple categories, choose the most specific primary category and mention the secondary categories in the case file.

## Adding a source

Use [templates/source-template.md](templates/source-template.md) for papers, blog posts, discussions, or tool reports.

Sources should include:

- Title.
- Author or organization.
- Date, if available.
- Link.
- Source type.
- Short relevance summary.
- The drift pattern it supports.
- Any limitations or caveats.

## Writing style

Use plain, neutral language.

Prefer:

> The issue thread shows that the generated change relied on an outdated API contract.

Avoid:

> This proves the tool is unreliable.

Prefer:

> The documentation and implementation disagreed about authentication behavior.

Avoid:

> The team failed to maintain their docs.

## Privacy and safety

Do not include:

- Secrets, tokens, credentials, or private logs.
- Private customer data.
- Non-public internal documents.
- Personally identifying information unless it is already clearly part of the public source and relevant to the evidence.
- Harassment, speculation about motives, or personal criticism.

If a public source contains sensitive material, summarize only the relevant technical point and avoid amplifying unnecessary details.

## Review expectations

Maintainers may ask contributors to:

- Add citations.
- Narrow broad claims.
- Rephrase subjective language.
- Move an entry to a better category.
- Add reproduction details.
- Clarify limitations.

The aim of review is to improve the evidence base, not to win an argument about a tool, company, or workflow.

## Licensing

By contributing, you agree that your contribution will be licensed under the repository license.
