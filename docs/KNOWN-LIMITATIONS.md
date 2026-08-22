# PCssak 0.8.0 Known Limitations

Last updated: 2026-08-23

This document describes the published **Unsigned Free Early Access** portable
prerelease [`v0.8.0`](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases/tag/v0.8.0).

## Distribution and trust boundary

- The only official application archive is
  `PCSSAK_0.8.0_x64_Portable.zip` for Windows x64.
- Its SHA-256 is
  `88d9e2012b329242ab2903268f46ec5b4a6f69d06582d262cf706704cd0406aa`.
- The archive uses no installer. It must be extracted to a user-owned folder.
- `PCSSAK.exe` is intentionally not Authenticode-signed in this phase. Windows may
  display Unknown publisher, SmartScreen, or antivirus warnings.
- Code signing, publisher-certificate verification, SmartScreen reputation, and
  external legal-counsel review are deferred. They are not passing gates.
- A hash match proves that a file matches the asset published in the same GitHub
  Release; it does not independently prove that the software is harmless.

## Validation boundary

- Automated regression results do not replace practical testing on physical Windows
  systems.
- The complete Windows 10/11 Home and Pro, DPI, multi-monitor, filesystem, elevation,
  security-product, install/update/removal, and recovery matrices are not complete.
- Windows x86 is not supported. The first package is x64 only.
- Real-world measurements from additional PCs will be collected after the prerelease
  becomes downloadable. Each result must identify the exact release hash and Windows
  environment.
- Performance or detection-accuracy claims must not be generalized beyond the devices,
  data, and workloads that were actually measured.

## Product-scope boundary

- The first Free Early Access scope is limited primarily to read-only diagnostics.
  System-changing and Pro features may remain unavailable.
- The update control checks only when the user requests it and displays the result.
  When a newer version exists, the user may separately press the official download-page
  button. The check does not open a page, download, execute, install, or roll back a
  package automatically.
- Portable does not mean zero local state. Settings, logs, quarantine information,
  recovery records, or other application data may be stored outside the extracted
  folder.
- Deleting the extracted folder is not a complete data-removal procedure. Follow the
  `UNINSTALL_AND_LOCAL_DATA.md` document included with the actual Release.

## License and source obligations

- Deferring external legal review does not defer third-party license obligations.
- Every published prerelease must retain the SBOM, third-party notices, Qt runtime
  manifest, replacement guidance, source offer, and exact Qt/PySide corresponding
  source archives defined by the release asset standard.
- Missing or mismatched required license/source material blocks publication.

## Safe response to a warning or defect

Do not run the package when its origin, exact filename, SHA-256, or extracted contents
cannot be verified. Stop using the affected copy, preserve only privacy-safe evidence,
and follow [SECURITY.md](../SECURITY.md) for a security-sensitive issue or
[SUPPORT.md](../SUPPORT.md) for a general defect.
