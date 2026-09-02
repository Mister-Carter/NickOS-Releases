# NickOS signed runtime releases

This public repository contains only versioned, audited NickOS installer runtime assets. The private source repository and all personal data remain private.

A NickOS ISO downloads the assets from the latest release, verifies the Ed25519-signed manifest with its embedded public key, verifies the archive SHA-256, size, schema, channel, and paths, and then runs the normal blueprint audit. If any check fails, installation uses the audited offline runtime embedded in the ISO.

Release assets:

- `nickos-runtime.manifest`
- `nickos-runtime.manifest.sig`
- `nickos-runtime.tar.zst`
- `nickos-release-signing-key.pem` (public key only)

Ed25519 public-key fingerprint (SHA-256 of DER): `eba96e34d8b1db8ee275409109a8e8a698bc9a86c208ca3b6d16f059c2b7a2f3`

The private signing key is stored offline from this repository and is never included in an ISO or release.