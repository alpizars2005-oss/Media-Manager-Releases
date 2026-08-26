# Verify Alpizers release files

Alpizers publishes Windows binaries separately from its private development repository. Every current release is expected to contain:

- `Alpizers-Setup-<version>.exe`
- `Alpizers-Windows-portable-<version>.zip`
- `update-manifest.json`

GitHub Releases also exposes a digest for uploaded assets when available. The Alpizers updater independently uses the SHA-256 stored in `update-manifest.json` for the installer.

## Manual installer verification on Windows

1. Download the installer and `update-manifest.json` from the **same release**.
2. Inspect `update-manifest.json` and copy its `sha256` value.
3. In PowerShell, run:

```powershell
Get-FileHash -Algorithm SHA256 .\Alpizers-Setup-<version>.exe
```

4. Compare the resulting hash with the manifest value. They must match exactly, ignoring letter case.

A matching SHA-256 means the installer bytes match the digest recorded in that manifest. It does **not** prove that a file is harmless if both the binary and its manifest came from a compromised release channel.

## Portable ZIP

GitHub may display a SHA-256 digest for the uploaded ZIP asset on the release/API. That digest can be compared with:

```powershell
Get-FileHash -Algorithm SHA256 .\Alpizers-Windows-portable-<version>.zip
```

The in-app updater currently verifies the installer referenced by the update manifest; it does not use the portable ZIP for automatic updates.

## Version consistency

For a normal release, the tag, release title, installer filename, portable filename, and manifest `version` should all represent the same version.

Do not mix an installer from one release with a manifest from another release.

## Publisher identity

The current integrity mechanism is HTTPS + GitHub release provenance + SHA-256 verification. Authenticode signing is a separate future hardening layer and should not be claimed until a valid signing certificate is actually used by the release pipeline.
