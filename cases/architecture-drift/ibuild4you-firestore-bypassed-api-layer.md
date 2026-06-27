# Realtime Messages Hook Bypassed the API Route Layer

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

- 

## Summary

An `ibuild4you` issue reports that `useRealtimeMessages.ts` read Firestore directly from the client SDK, bypassing a documented rule that all database access should go through API routes using the Firebase Admin SDK.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-05-24
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/nicolovejoy/ibuild4you/issues/40

## Affected System or Context

Client messaging hook, Firestore access pattern, and API-route architecture rule.

## Human Intent

The documented rule in `CLAUDE.md` was that database access goes through API routes and the Firebase Admin SDK.

## Machine Knowledge

The hook implementation used the client SDK and `onSnapshot()` directly.

## Observable Reality

The issue states this path worked because current Firestore rules allowed it, but it bypassed the intended route layer.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The implementation did not reflect the documented access boundary.
- Machine Knowledge vs Observable Reality: The app still worked, hiding the architectural mismatch.
- Human Intent vs Observable Reality: Runtime success masked a violation of the intended boundary.

## Impact

Reduced observability, harder testing, and risk that future auth changes miss this direct path.

## Detection Method

Codebase audit.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the file, the documented rule, the bypass, and a proposed fix shape.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Inspect the issue.
2. Inspect `lib/hooks/useRealtimeMessages.ts`.
3. Compare with the database access rule in `CLAUDE.md`.

Missing context or limitations:

- Requires repository access to confirm exact line numbers.

## Notes

The issue explicitly rates severity as low and says there was no current user-facing bug.

