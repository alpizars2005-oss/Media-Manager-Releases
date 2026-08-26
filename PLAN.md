# Repository Improvement Plan

Date: 2026-08-26

## Goal

Make the public Alpizers release channel easier to verify and safer to consume without moving private source code into this repository.

## Audit findings

- The repository currently contains only a README; binaries and manifests live in GitHub Releases.
- The README explains naming and responsibility boundaries but does not give users a concise verification procedure for the update manifest/installer SHA-256.
- The repository can document release-channel guarantees without duplicating the private development repository.

## Atomic commit plan

1. Document the audit.
2. Add a public release-channel/security policy explaining provenance, checksum verification, and reporting.
3. Improve README verification/install guidance while preserving the private-source boundary.

## Validation

- Documentation only; no release assets or manifests are modified by this pass.
- Verify all documented filenames match the current Alpizers release workflow.

## Risk / rollback

Documentation-only, very low risk. Revert individual commits if wording needs adjustment.
