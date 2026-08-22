# Quality and Safety Publication Standard

PCssak uses verifiable evidence and accurate failure guidance as its release standard rather than promising that errors cannot occur.

## Required before publication

1. Traceability between source checkpoint, commit, version, channel, and build artifact
2. SHA-256 coverage for every public asset
3. Verified installer signature and publisher identity
4. SBOM and third-party license notices
5. Real-Windows matrix results and known limitations
6. UI contracts that never present failure, cancellation, or partial completion as success
7. Evidence that files, registry entries, and drivers outside the selected scope were unchanged
8. Recovery procedures and stop-release criteria for severe defects

## Result states

- Success: the requested scope completed with verifiable evidence
- Skipped: safely excluded by policy, compatibility, or permission conditions
- Failed: incomplete, with a reason and a practical alternative
- Cancelled: stopped by the user, with completed work clearly separated

Performance claims require same-device, same-workload WPR/WPA A/B evidence.
