# PCssak - Official Unsigned Free Early Access

**Primary language:** English · [한국어](README.ko.md)

**Release guides:**
[English](docs/locales/RELEASE_GUIDE.en.md) ·
[한국어](docs/locales/RELEASE_GUIDE.ko.md) ·
[Deutsch](docs/locales/RELEASE_GUIDE.de.md) ·
[日本語](docs/locales/RELEASE_GUIDE.ja.md) ·
[简体中文](docs/locales/RELEASE_GUIDE.zh-CN.md) ·
[繁體中文](docs/locales/RELEASE_GUIDE.zh-TW.md) ·
[Русский](docs/locales/RELEASE_GUIDE.ru.md) ·
[Español (Latinoamérica)](docs/locales/RELEASE_GUIDE.es-419.md) ·
[Español (España)](docs/locales/RELEASE_GUIDE.es.md) ·
[Türkçe](docs/locales/RELEASE_GUIDE.tr.md) ·
[Português (Brasil)](docs/locales/RELEASE_GUIDE.pt-BR.md)

This is the official public release and verification repository for **PCssak**,
PCSSAK's main Windows maintenance and privacy tool. Product source code and internal
development evidence are maintained separately in a private repository.

## Current status

> [!IMPORTANT]
> This documentation change does not publish a tag, Release, executable, or archive.

The planned first public test package is **PCssak 0.8.0 Unsigned Free Early Access**.
It will be a Windows x64 portable archive named exactly:

```text
PCSSAK_0.8.0_x64_Portable.zip
```

The package is intentionally unsigned for this Free Early Access phase. Authenticode
publisher verification, external legal-counsel review, SmartScreen reputation, and the
full Windows practical-test matrix are deferred to a later commercial release. These
items are disclosed as deferred or not run; they are never reported as `PASS`.

Free Early Access does not defer third-party license obligations. A public prerelease
must still include exact hashes, an SBOM, third-party notices, the Qt runtime manifest,
and the required Qt/PySide corresponding-source archives.

## Package contract

| Item | First public test policy |
|---|---|
| Version | `0.8.0` |
| Channel | Unsigned Free Early Access |
| Architecture | Windows x64 only |
| Format | Portable ZIP; no installer |
| Archive | `PCSSAK_0.8.0_x64_Portable.zip` |
| Public distributor label | PCSSAK |
| GitHub tag | `v0.8.0` only when the prerelease is actually published |
| Code signature | Not provided in this phase |
| Update behavior | A user-requested check shows status; when a newer version exists, the user may separately press the official download-page button |

PCSSAK is the public distributor label for this phase. Because the executable is
unsigned, that label is not an Authenticode-verified publisher identity.

## How to verify an official download

1. Download only from this repository's
   [Releases](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases)
   page after a `v0.8.0` prerelease is visible.
2. Confirm the exact archive name shown above.
3. Compare the archive's SHA-256 with the exact entry in `SHA256SUMS.txt` from the
   same Release.
4. Keep the archive and extracted files blocked if the hash is missing or different.
5. Scan the archive and extracted folder with an up-to-date security product before
   running `PCSSAK.exe`.

Because the executable is unsigned, Windows may show **Unknown publisher**, SmartScreen,
or antivirus warnings. A warning is neither proof of malware nor proof of safety. Stop
and report the event if the source, filename, hash, or behavior cannot be verified.

The update check does not open a page automatically. It does not automatically download,
execute, install, or roll back a package.

## Portable-package behavior

- Extract the archive to a user-owned folder; do not extract it into Windows or another
  protected system directory.
- Portable means that no installer is used. It does not mean that PCssak writes no local
  settings, logs, quarantine records, or recovery data.
- Deleting the extracted program folder does not automatically remove separately stored
  local data. Follow the release's `UNINSTALL_AND_LOCAL_DATA.md` instructions.
- The first Free Early Access scope is intentionally limited. System-changing and Pro
  features may remain unavailable while measurements are collected.

## Publication and safety documents

- [Known limitations](docs/KNOWN-LIMITATIONS.md)
- [Quality and safety standard](docs/QUALITY-AND-SAFETY.md)
- [Release asset standard](docs/RELEASE_ASSET_STANDARD.md)
- [Security reporting](SECURITY.md)
- [Support and privacy guidance](SUPPORT.md)

## Repository boundary

- **Public here:** verified prerelease assets, checksums, SBOM, approved notices,
  corresponding-source archives, localized guides, and sanitized public issues.
- **Never public here:** product source, signing keys, tokens, private customer data,
  raw ETL/DMP/EVTX/log/video evidence, internal incident reports, or unverified builds.
- This repository does not make the private product source open source or grant rights
  beyond the terms included with the published package.
