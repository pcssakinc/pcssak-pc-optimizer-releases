# Known Limitations — Pre-release State

Last updated: 2026-08-12

No public installer is available.

## Open gates

- Real-device x64 validation on Windows 10 22H2 build 19045 Home and Pro, and
  Windows 11 build 26100 or later Home and Pro
- 100/125/150/200% DPI and multi-monitor UI validation
- Real deletion, recovery, cancellation, and resume tests for elevated operations
- Physical-device validation of driver inventory, installation, and leftover-driver removal
- SSD/TRIM, ReFS/Dev Drive, and locked-file failure-guidance tests
- WPR/WPA-based A/B performance measurement
- Install, update, uninstall, and rollback validation
- Code signing, SmartScreen, and major security-product false-positive review
- Final approval of licensing, third-party notices, and privacy documents
- The legal publisher name and legal-review reference are not yet finalized.
- The independent publisher-certificate SHA-256 trust pin and separate release
  approval are `NOT_CONFIGURED`.
- Actual signing, antivirus review, real-Windows validation, publication, and
  tag creation are `NOT_RUN`.

## First-candidate scope

- Windows x64 only; 32-bit Windows is not supported.
- The installer's technical floor is Windows 10 build 17763, but that is not a
  public support guarantee. Because general Windows 10 support has ended, a
  supported Windows 11 environment or an eligible Windows 10 ESU environment
  is recommended.
- The free public beta has no Pro registration and includes no development
  license key.

Passing automated tests alone does not close these gates. `NOT_CONFIGURED` and
`NOT_RUN` are not passing states. Every release will disclose the verified
scope and remaining limitations.

Official lifecycle references: [Windows 10 release information](https://learn.microsoft.com/en-us/windows/release-health/release-information) and [Windows 11 release information](https://learn.microsoft.com/en-us/windows/release-health/windows11-release-information).
