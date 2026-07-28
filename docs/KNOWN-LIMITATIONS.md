# Known Limitations — Pre-release State

Last updated: 2026-07-28

No public installer is available. The following gates must be closed before the first public release:

- Real-device Windows 10/11 Home and Pro validation across supported architectures
- 100/125/150/200% DPI and multi-monitor UI validation
- Real deletion, recovery, cancellation, and resume tests for elevated operations
- Physical-device validation of driver inventory, installation, and leftover-driver removal
- SSD/TRIM, ReFS/Dev Drive, and locked-file failure-guidance tests
- WPR/WPA-based A/B performance measurement
- Install, update, uninstall, and rollback validation
- Code signing, SmartScreen, and major security-product false-positive review
- Final approval of licensing, third-party notices, and privacy documents

Passing automated tests alone does not close these gates. Every release will disclose the verified scope and remaining limitations.
