# PCssak - Official Release Preparation

**Languages:** English · [한국어](README.ko.md)

This is the official public release-preparation and verification repository for **PCssak**,
PCSSAK's main Windows maintenance and privacy tool. Product source code and internal development
material are maintained separately in a private repository.

## Current status

> [!IMPORTANT]
> No public installer has been released yet.

Downloads will remain unpublished until real-Windows validation, reproducible artifact checks,
antivirus false-positive review, legal-notice approval, and code-signing preparation are
complete. The absence of executables and official releases in this repository is intentional.

## How to verify future official downloads

- Obtain downloads only from this repository's **Releases** page after an approved release is
  visible.
- Verify the publisher, version, exact filename, and matching hash in `SHA256SUMS.txt`.
- Do not use unknown mirrors, messenger attachments, or repackaged installers.
- Each release will include localized guidance and known limitations only for languages with
  an actual published document.

Read the current [known limitations](docs/KNOWN-LIMITATIONS.md),
[quality and safety standard](docs/QUALITY-AND-SAFETY.md), and
[release asset standard](docs/RELEASE_ASSET_STANDARD.md).

Do not disclose exploitable details in a public issue. Follow the [security
policy](SECURITY.md) for private reporting. For general help, see [support](SUPPORT.md).

## Repository boundary

- **Public here:** verified release files, checksums, signatures or attestations when available,
  approved notices, localized release notes, and sanitized public issue reports.
- **Never public here:** product source, signing keys, tokens, private customer data, raw
  ETL/DMP/EVTX/log/video evidence, internal incident reports, or unverified builds.
- Publishing this repository does **not** make the product source open source or grant a software
  license. Release binaries will be governed by the approved end-user terms included with that
  release.
