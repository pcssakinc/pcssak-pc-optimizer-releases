# Quality and Safety Standard for Unsigned Free Early Access

PCssak uses verifiable evidence and accurate limitations instead of claiming that an
Early Access build is error-free or fully validated.

## Result states

- **PASS:** the exact release-specific procedure completed with verifiable evidence.
- **DEFERRED:** intentionally moved to a later commercial-release gate and disclosed.
- **NOT_RUN:** no qualifying execution or evidence exists.
- **FAILED:** the procedure did not complete or produced a conflicting result.

`DEFERRED`, `NOT_RUN`, and `FAILED` are never represented as `PASS`.

## Required before an unsigned portable prerelease

1. Traceability between the approved source commit, version `0.8.0`, channel,
   Windows x64 build, and `PCSSAK_0.8.0_x64_Portable.zip`.
2. A clean and reviewed source checkpoint and a build record that contains no private
   keys, tokens, raw user evidence, or development-only license data.
3. An exact portable-archive inventory that rejects absolute paths, parent traversal,
   symbolic links, reparse points, unexpected executables, and test-only files.
4. SHA-256 coverage for every public Release asset except `SHA256SUMS.txt` itself,
   using exact, case-sensitive filenames.
5. A release manifest, SPDX SBOM, deterministic third-party-license package, Qt runtime
   manifest, notices, replacement guidance, source offer, and exact Qt/PySide
   corresponding-source archives.
6. Release-specific known limitations, update/rollback guidance, local-data removal
   guidance, and the 11 localized release guides.
7. Recorded malware-scan results and at least one controlled extract, launch, close,
   and cleanup smoke test for the exact archive candidate. Unresolved detections block
   publication.
8. Independent local-to-Draft comparison of asset names, counts, sizes, and SHA-256
   values before the Draft Prerelease is published.

## Explicitly deferred gates

The first unsigned Free Early Access prerelease may disclose the following as
`DEFERRED` or `NOT_RUN`:

- Authenticode code signing, RFC 3161 timestamping, and publisher-certificate trust;
- SmartScreen reputation and signed-publisher user experience;
- external legal-counsel approval;
- the complete physical Windows 10/11 Home and Pro, DPI, filesystem, administrator,
  recovery, performance, and security-product matrix.

Deferral does not permit false signature claims, missing license/source material,
incorrect hashes, an unreviewed asset inventory, or a known destructive defect.

## Stop-release conditions

Publication stops when any of the following is observed:

- version, source commit, filename, size, or hash mismatch;
- an unexpected, missing, duplicate, or unsafe archive member;
- missing SBOM, notice, license, Qt runtime record, or corresponding source;
- secrets, private logs, user data, internal evidence, or development-only files;
- an unresolved malware detection, startup failure, data-loss risk, privilege-boundary
  defect, or misleading success state;
- documentation that describes a deferred or untested gate as passed.

## Immutable publication

The GitHub Release is created as a Draft Prerelease first. Every approved asset is
attached and verified before publication. After publication, the `v0.8.0` tag and its
assets are not silently replaced. A correction uses a new version and a new immutable
Release.
