# WSL Proxy Documentation Missed Domain and Wildcard Bypass Support

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

A Rancher Desktop docs issue reports that the WSL proxy documentation was outdated because the no-proxy list now accepted domain names and wildcard patterns, not only IP and CIDR values.

## Source Type

- Source type: GitHub issue
- Date observed: 2026-06-05
- Date added: 2026-06-27
- Contributor: Codex

## Public Source URL

- URL: https://github.com/rancher-sandbox/docs.rancherdesktop.io/issues/487

## Affected System or Context

Rancher Desktop WSL proxy preference documentation.

## Human Intent

The documentation intended to describe valid proxy bypass-list inputs.

## Machine Knowledge

The docs encoded an older input contract centered on IP addresses and CIDR subnets.

## Observable Reality

The issue states that the current product accepted domain names and wildcard patterns and that the UI legend had changed to `Proxy bypass list`.

## Where the Divergence Occurred

- Human Intent vs Machine Knowledge: The docs no longer described all supported inputs.
- Machine Knowledge vs Observable Reality: The documented input types lagged behind product behavior.
- Human Intent vs Observable Reality: Users could miss supported proxy configuration options.

## Impact

Stale network-configuration docs can lead users to avoid valid configuration values or create unnecessary workarounds.

## Detection Method

Manual comparison of docs with current product behavior and related source changes.

## Evidence

Evidence quality level:

- [ ] Level 1: Anecdotal
- [x] Level 2: Public discussion
- [ ] Level 3: Reproducible example
- [ ] Level 4: Engineering postmortem
- [ ] Level 5: Academic or formal study

Evidence details:

- The issue names the changed behavior, gives examples such as wildcard domains, and references the source issue/change that introduced it.
- The issue is closed.

## Reproducibility

Reproducibility status:

- [ ] Fully reproducible
- [x] Partially reproducible
- [ ] Publicly inspectable but not reproducible
- [ ] Not publicly inspectable
- [ ] Unknown

Steps or inspection path:

1. Open the issue and the WSL proxy documentation file it names.
2. Inspect the referenced Rancher Desktop behavior change.
3. Compare supported bypass-list values with the documentation.

Missing context or limitations:

- Verifying behavior directly requires Rancher Desktop on Windows with WSL proxy settings.

## Notes

This is a closed public docs issue with specific changed behavior and target documentation scope.

