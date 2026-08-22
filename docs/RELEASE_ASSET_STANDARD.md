# PCssak 0.8.0 Portable Release Asset Standard

No public asset may be copied directly from an unverified local `dist` directory or
renamed from an older internal build.

The first public test identity is:

- product: `PCssak`;
- public distributor label: `PCSSAK`;
- version and display version: `0.8.0`;
- channel: `free-ea`;
- architecture: `x64`;
- GitHub tag: `v0.8.0`;
- distribution format: portable ZIP, not an installer;
- primary archive: `PCSSAK_0.8.0_x64_Portable.zip`.

This policy does not create the tag, Release, or archive. Because the executable is
unsigned, the public distributor label is not represented as an
Authenticode-verified publisher identity.

## Exact 18-asset allowlist

An actual `v0.8.0` Draft Prerelease must contain exactly these files:

```text
PCSSAK_0.8.0_x64_Portable.zip
RELEASE_MANIFEST.json
SHA256SUMS.txt
PCSSAK-SBOM.spdx.json
THIRD_PARTY_LICENSES.zip
QT_RUNTIME_MANIFEST.json
pyside-setup-everywhere-src-6.11.1.tar.xz
qt-everywhere-src-6.11.1.tar.xz
LICENSE.md
PRIVACY_POLICY.md
QT_SOURCE_OFFER.md
QT_LIBRARY_REPLACEMENT.md
QT_THIRD_PARTY_NOTICES.md
RELEASE_NOTES.md
KNOWN_LIMITATIONS.md
RELEASE_SUMMARIES.json
UPDATE_AND_ROLLBACK.md
UNINSTALL_AND_LOCAL_DATA.md
```

Unexpected, missing, duplicated, case-mismatched, symbolic-link, or reparse-point
assets block publication.

## Portable archive contract

`PCSSAK_0.8.0_x64_Portable.zip` must:

- be created from the approved `0.8.0` source checkpoint, never by renaming an older
  internal RC;
- contain one top-level `PCssak-0.8.0-x64/` directory and the release executable
  `PCSSAK.exe` below that directory;
- contain no absolute path, drive-qualified path, parent traversal, alternate data
  stream, symbolic link, reparse point, or duplicate case-insensitive path;
- contain no signing key, token, private log, raw test evidence, development license,
  internal manifest, `_test` executable, or unrelated program;
- display version `0.8.0` in the application and use the version identity recorded in
  `RELEASE_MANIFEST.json`;
- include the user-facing license, privacy, third-party notices, update/rollback, and
  local-data removal documents needed when the PC is offline;
- use a reviewed, deterministic member order and timestamps defined by the build
  process so that the exact candidate can be reproduced and compared;
- be scanned and smoke-tested only after the final archive bytes and SHA-256 are fixed.

## Unsigned-status contract

The executable is intentionally unsigned for this Free Early Access phase.

- `RELEASE_MANIFEST.json` and `RELEASE_NOTES.md` must state that Authenticode signing,
  publisher-certificate verification, RFC 3161 timestamping, SmartScreen reputation,
  and external legal-counsel approval are `DEFERRED` or `NOT_RUN`.
- No document, UI, checksum, attestation, or filename may imply that code signing or
  publisher verification passed.
- No empty signature, self-issued certificate, renamed internal approval, or fabricated
  `PASS` evidence may be attached.
- A Windows warning is disclosed in the release notes and localized guides. It is not
  described as proof that the file is safe or malicious.

## Integrity and compliance contract

- `RELEASE_MANIFEST.json` binds the source commit, version, channel, architecture,
  portable archive inventory, build environment, and size/SHA-256 of every payload.
- `SHA256SUMS.txt` covers all 17 other assets, including the portable ZIP and release
  manifest, with lowercase hexadecimal SHA-256, two spaces, exact filename, and LF.
- `PCSSAK-SBOM.spdx.json` is SPDX 2.3 JSON and binds the closed runtime dependency set
  to the portable archive hash.
- `THIRD_PARTY_LICENSES.zip` is deterministic and independently checked for member
  paths, sizes, hashes, and original license texts.
- `QT_RUNTIME_MANIFEST.json` records exact Qt runtime paths, sizes, and SHA-256 values
  extracted from the portable candidate.
- The exact Qt 6.11.1 and PySide6 6.11.1 corresponding-source archives are attached to
  the same GitHub Prerelease and checked against the approved official size and hash.
- `RELEASE_SUMMARIES.json` contains guidance for `ko`, `en`, `de`, `ja`, `zh-CN`,
  `zh-TW`, `ru`, `es-419`, `es`, `tr`, and `pt-BR`. The rendered repository guides in
  `docs/locales/` must communicate the same version, filename, unsigned warning, and
  verification steps.
- Deferring external legal review does not permit missing notices, source delivery, or
  other third-party license material.

## Draft and immutable publication procedure

1. Merge the reviewed documentation and release-contract commit to `main`.
2. Build and verify the complete 18-asset candidate outside this public repository.
3. Create `v0.8.0` as a **Draft Prerelease** targeting the reviewed `main` commit.
4. Upload all 18 assets without publishing the Draft.
5. Independently compare local and GitHub asset names, count, size, and SHA-256.
6. Recheck malware-scan and controlled portable smoke-test evidence for the exact ZIP.
7. Publish once only after every non-deferred gate passes and each deferred gate is
   disclosed honestly.
8. Verify the immutable Release and local assets, then enable the website download and
   update metadata.

Published tags and assets are never silently replaced. A defect is corrected in a new,
higher version such as `v0.8.1`.
