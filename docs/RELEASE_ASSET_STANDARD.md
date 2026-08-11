# 공개 릴리스 자산 기준 / Release Asset Standard

검증되지 않은 로컬 `dist` 폴더에서 공개 릴리스를 직접 만들지 않습니다. 첫 공개
후보의 정체성은 `v0.9.0-beta.1`, 표시 버전 `0.9.0 Beta 1`, Windows 파일 버전
`0.9.0.1`, 업그레이드 판정 순번(ordinal) `9,000,001`, 아키텍처 `x64`입니다.

No release may be published directly from an unverified local `dist` directory.
The first candidate identity is `v0.9.0-beta.1`, display version
`0.9.0 Beta 1`, Windows file version `0.9.0.1`, architecture `x64`.
Its monotonic installer ordinal is `9,000,001`.

## 정확한 자산 목록 18개 / Exact 18-asset allowlist

```text
PCSSAK_Setup_0.9.0-beta.1_x64.exe
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

### 한국어 계약

- `RELEASE_MANIFEST.json`은 릴리스 채널·순번, 소스 커밋, 빌드 환경, 실제 Qt
  런타임 목록, 모든 대상 자산의 크기와 SHA-256을 결속합니다.
- `SHA256SUMS.txt`는 자기 자신을 제외한 모든 자산을 정확한 파일명과 SHA-256으로
  포함합니다.
- `PCSSAK-SBOM.spdx.json`은 SPDX 2.3 JSON이며 실제 런타임 의존성 폐쇄와 설치기
  해시에 연결됩니다.
- `THIRD_PARTY_LICENSES.zip`은 결정적 ZIP으로 만들고 내부 경로·크기·해시·라이선스
  원문을 독립 검증합니다.
- Qt/PySide6 대응 소스는 같은 GitHub Release에 두며 정확한 공식 크기와 해시를
  확인합니다.
- `RELEASE_SUMMARIES.json`은 앱의 11개 로케일에 설치 전 요약·검증 경계·지원
  경로를 제공하며, 법적 통제 원문은 한국어와 영어임을 명시합니다.
- `GATE_EVIDENCE.json`과 법무·Windows 실기·백신 원시 증거는 공개 자산이 아니라
  공개 전 검증기의 비공개 입력입니다.
- `RELEASE_APPROVAL.p7m`은 아직 허용목록에 없는 미래 자산입니다. 빈 파일이나
  자체 생성 승인으로 추가하지 않습니다.
- 설치기는 독립 게시자 인증서 핀이 구성된 뒤 실제 Authenticode 서명과 RFC 3161
  타임스탬프를 우회할 수 없는 검증기로 확인합니다.
- `QT_RUNTIME_MANIFEST.json`은 실제 Qt 파일 목록·크기·SHA-256을 기록하고, 서명된
  빌드 매니페스트·공개 매니페스트·체크섬에 결속합니다.

### English contract

- `RELEASE_MANIFEST.json` binds the channel and ordinal, source commit, build
  environment, actual Qt runtime inventory, and size/SHA-256 of every payload.
- `SHA256SUMS.txt` covers every asset except itself using exact file names and
  SHA-256 values.
- `PCSSAK-SBOM.spdx.json` is SPDX 2.3 JSON and is bound to the installer hash
  and closed runtime dependency set.
- `THIRD_PARTY_LICENSES.zip` is deterministic and independently checked for
  member paths, sizes, hashes, and original license texts.
- Exact Qt/PySide6 corresponding-source archives are attached to the same
  GitHub Release after official size and hash verification.
- `RELEASE_SUMMARIES.json` provides pre-installation guidance, verification
  boundaries, and support routing for all 11 app locales while identifying
  Korean and English as the controlled legal originals.
- `GATE_EVIDENCE.json` and raw legal, real-Windows, and antivirus evidence are
  private pre-publication verifier inputs, not public assets.
- `RELEASE_APPROVAL.p7m` is not yet in the allowlist. It must never be replaced
  with an empty or self-issued approval artifact.
- After the independent publisher trust pin is configured, the installer is
  checked for actual Authenticode signing and RFC 3161 timestamping with no
  bypass.
- `QT_RUNTIME_MANIFEST.json` records the actual Qt file paths, sizes, and
  SHA-256 values and is bound to the signed build manifest, public manifest,
  and checksums.

현재 독립 승인 게시자 인증서 SHA-256 핀과 별도 콘텐츠 포함형 CMS 승인 서명은 모두
`NOT_CONFIGURED`입니다. 따라서 공개 조립 CLI와 게시 경로는 조건 미충족 시
중단됩니다.

The independently approved publisher-certificate SHA-256 pin and separate
attached-CMS release approval are both `NOT_CONFIGURED`; public assembly and
publication therefore fail closed.

## 게시 절차 / Publication procedure

먼저 Draft Release를 만들고 모든 자산을 올린 뒤 체크섬·서명·악성코드 오탐·법무·
실측 관문과 독립 게시자 확인이 모두 `PASS`이고 별도 attached CMS 승인이 검증됐을
때만 게시합니다. `NOT_CONFIGURED`와 `NOT_RUN`은 성공이 아닙니다. 게시된 태그와
자산은 조용히 교체하지 않으며, 문제가 있으면 배포를 중단하고 더 높은 ordinal의
새 태그를 사용합니다.

A Draft Release is assembled and fully verified first. Publication is a
separate reviewed action permitted only when checksum, publisher signing,
malware-scan, legal, and practical-test gates are all `PASS` and the attached
CMS approval is independently verified. `NOT_CONFIGURED` and `NOT_RUN` are not
success.
Published tags and assets are never silently replaced. A defect stops the
release and is corrected under a new, higher-ordinal tag.
