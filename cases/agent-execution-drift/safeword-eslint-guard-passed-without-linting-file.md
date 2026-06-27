# Manual ESLint Guard Passed Without Linting the Changed File

## Drift Category

Primary category:

- [ ] AI Context Drift
- [ ] Documentation Drift
- [ ] Architecture Drift
- [x] Agent Execution Drift
- [ ] Specification Drift
- [ ] Memory Drift
- [ ] Tooling Drift
- [ ] Unknown / Other

Secondary categories:

- Tooling Drift

## Summary

A Safeword issue reports that a documented manual pre-commit guard could exit successfully even when ESLint ignored the changed TypeScript file. The drift is between the intended agent/manual verification step and the actual coverage achieved by the command.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-26
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/ArcadeAI/safeword/issues/472

## Affected System or Context

Manual pre-commit verification for TypeScript changes.

## Human Intent

Maintainers and agents intended the manual ESLint guard to verify changed TypeScript files.

## Machine Knowledge

The guard command returned success even though ESLint emitted a warning that the file was ignored.

## Observable Reality

The issue includes command output showing `File ignored because of a matching ignore pattern` and states the command exited 0.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The guard was treated as lint coverage, but the tool skipped the file.
- Machine Knowledge vs Observable Reality: A successful exit code masked missing validation.
- Human Intent vs Observable Reality: The changed file was not actually linted.

## Impact

Agents or maintainers can report verification success without checking the changed file.

## Detection Method

Manual command output inspection during a PR.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [ ] Level 2: Public discussion
- [x] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue includes the exact command, output warning, expected behavior, and acceptance criteria.

## Reproducibility

Reproducibility status:

- [x] Fully reproducible
- [ ] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Run the documented ESLint command on an ignored changed TypeScript file.
2. Observe the ignored-file warning.
3. Check that the command exits successfully.

Missing context or limitations:

- Requires a repo state where the path is ignored.

## Notes

This is agent execution drift because a verification step can create a false "checked" state during delegated work.

