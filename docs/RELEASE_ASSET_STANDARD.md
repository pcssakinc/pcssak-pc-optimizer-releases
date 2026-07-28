# Release Asset Standard

No release may be published directly from an unverified local `dist` directory.

Each public release must be assembled from an approved source checkpoint and include:

- verified installer file(s);
- `RELEASE-MANIFEST.json` linking version, channel, source commit, clean-tree state, build environment, and artifact hashes;
- `SHA256SUMS.txt` covering every release asset except the checksum file itself;
- Authenticode signature information and additional updater signature files when that update system is enabled;
- CycloneDX SBOM;
- `THIRD-PARTY-NOTICES.txt`;
- exact source bundles required by reciprocal third-party licenses;
- localized release notes and known limitations;
- recovery, uninstall, and support instructions.

The workflow must create a draft release first. Publication is a separate, reviewed action after checksum, signature, malware-scan, legal, and practical-test gates pass. Existing published tags and assets are never silently replaced.
