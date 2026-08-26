# Security policy for the Alpizers release channel

This repository is a **binary distribution channel**. Application source is maintained separately.

## What to verify

Before running a downloaded installer, verify that:

- it came from an expected Alpizers GitHub Release;
- its version matches the release/tag you intended to install;
- the installer SHA-256 matches the value in that release's `update-manifest.json` when using the manifest as the verification source.

See [`VERIFY_RELEASES.md`](VERIFY_RELEASES.md) for the manual procedure.

## What a hash proves

A matching SHA-256 establishes byte-for-byte integrity relative to the expected digest. It does not by itself establish that the publisher account, release channel, or original build environment was uncompromised.

Do not interpret an official-looking filename, a successful download, or a matching hash from an untrusted manifest as a malware guarantee.

## Reporting

Do not publish credentials, private source code, local tokens, or sensitive downloaded content in an issue. A release-channel report should identify the affected tag/asset and include non-sensitive evidence such as filenames and hashes.

If a release asset and its expected manifest/digest disagree, do not execute the asset until the release has been investigated.

## Supported releases

The latest non-prerelease Alpizers release receives priority for release-channel security fixes. Older releases remain available for history/rollback but may not be rebuilt.
