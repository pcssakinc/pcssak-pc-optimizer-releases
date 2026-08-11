# PCSSAK PC Optimizer — Official Releases

[한국어](#한국어) | [English](#english)

## 한국어

이 저장소는 **PCSSAK PC Optimizer의 공식 무료 배포 전용 저장소**입니다. 제품 소스와 내부 개발 자료는 별도의 비공개 저장소에서 관리합니다.

### 현재 상태

> 첫 번째 공개 설치 파일은 아직 배포하지 않았습니다.

첫 공개 후보는 **PCSSAK 0.9.0 Beta 1 무료 공개 베타(x64)**로 준비하고 있습니다.
버전·파일명과 자동 검증 계약을 준비한 상태일 뿐, 아래 검증 관문을 통과하기 전에는
릴리스나 다운로드로 간주하지 않습니다. 무료 공개 베타에는 개발용 라이선스 키를
포함하지 않으며 Pro 등록을 제공하지 않습니다.

실제 Windows 환경 검증, 배포 산출물의 출처·무결성 재검증, 악성코드 오탐 점검,
법적 고지 승인, 실제 Authenticode 서명·RFC 3161 타임스탬프·독립 게시자 확인이
끝나기 전에는 다운로드 파일을 게시하지 않습니다. 독립 게시자 인증서 신뢰 핀과
별도 릴리스 승인은 아직
`NOT_CONFIGURED`입니다. 현재 이 저장소에 실행 파일·태그·공식 릴리스가 없는 것이
정상입니다.

첫 후보의 기술적 설치 하한은 Windows 10 빌드 17763 x64이지만, 이는 공개 지원을
보장한다는 뜻이 아닙니다. 공개 전 실기 대상은 Windows 10 22H2 빌드 19045
Home·Pro와 Windows 11 빌드 26100 이상 Home·Pro입니다. 일반 Windows 10 지원은
종료됐으므로 Microsoft가 지원하는 Windows 11 또는 적격 Windows 10 ESU 환경을
권장합니다.

### 향후 공식 다운로드 확인법

- 다운로드는 이 저장소의 **Releases** 화면에서만 제공합니다.
- 게시자, 버전, 파일명과 `SHA256SUMS.txt`의 해시를 함께 확인하세요.
- 출처가 불분명한 미러, 메신저 첨부 파일 또는 재포장 설치 파일은 사용하지 마세요.
- 릴리스가 게시되면 11개 앱 언어의 안내 요약과 한·영 통제 릴리스 노트·알려진
  제한을 함께 제공합니다.

현재 경계는 [알려진 제한](docs/KNOWN-LIMITATIONS.ko.md),
[품질·안전 기준](docs/QUALITY-AND-SAFETY.ko.md),
[공개 자산 기준](docs/RELEASE_ASSET_STANDARD.md)에서 확인할 수 있습니다.

보안 문제는 공개 이슈에 악용 가능한 내용을 쓰지 말고 [보안 정책](SECURITY.md)을 따라 비공개로 제보해 주세요. 일반 문의는 [지원 안내](SUPPORT.md)를 확인하세요.

### 저장소 경계

- 이곳에 공개하는 것: 검증된 릴리스 파일·체크섬, 준비된 경우의 서명 또는 증명,
  승인된 고지, 현지화 릴리스 안내, 민감정보를 제거한 공개 이슈
- 이곳에 공개하지 않는 것: 제품 소스, 서명 키, 토큰, 고객 개인정보, 원본
  ETL/DMP/EVTX·로그·영상 증거, 내부 사고 보고서, 미검증 빌드
- 이 저장소가 공개돼 있다는 사실은 제품 소스를 오픈소스로 만들거나 소프트웨어
  이용권을 부여하지 않습니다. 향후 바이너리는 해당 릴리스에 포함된 승인된 최종
  사용자 약관을 따릅니다.

## English

This is the **official free-distribution repository for PCSSAK PC Optimizer**. Product source code and internal development material are maintained separately in a private repository.

### Current status

> No public installer has been released yet.

The first candidate is being prepared as **PCSSAK 0.9.0 Beta 1, a free public
beta for x64 Windows**. Its version, asset names, and automated verification
contract are preparatory only; they do not constitute a release or download.
The public beta contains no development license key and offers no Pro
registration.

Downloads will remain unpublished until real-Windows validation, artifact
provenance and integrity verification, antivirus false-positive review,
legal-notice approval, actual Authenticode signing, RFC 3161 timestamping, and
independent publisher verification are complete. The
independent publisher-certificate trust pin and separate release approval are
still `NOT_CONFIGURED`. The absence of executables, tags, and official releases
in this repository is intentional.

The technical installer floor is Windows 10 build 17763 x64, but that does not
constitute a public support claim. Pre-publication practical targets are
Windows 10 22H2 build 19045 Home and Pro, and Windows 11 build 26100 or later
Home and Pro. Because general Windows 10 support has ended, a Microsoft-
supported Windows 11 environment or an eligible Windows 10 ESU environment is
recommended.

### How to verify future official downloads

- Obtain downloads only from this repository's **Releases** page.
- Verify the publisher, version, file name, and matching hash in `SHA256SUMS.txt`.
- Do not use unknown mirrors, messenger attachments, or repackaged installers.
- Each release will include an 11-locale guidance summary plus controlled
  Korean/English release notes and known limitations.

See the current [known limitations](docs/KNOWN-LIMITATIONS.md),
[quality and safety standard](docs/QUALITY-AND-SAFETY.md), and
[release asset standard](docs/RELEASE_ASSET_STANDARD.md).

Do not disclose exploitable details in a public issue. Follow the [security policy](SECURITY.md) for private reporting. For general help, see [support](SUPPORT.md).

## Repository boundary

- Public here: verified release files, checksums, signatures or attestations when available, approved notices, localized release notes, and sanitized public issue reports.
- Never public here: product source, signing keys, tokens, private customer data, raw ETL/DMP/EVTX/log/video evidence, internal incident reports, or unverified builds.
- Publishing this repository does **not** make the product source open source or grant a software license. Release binaries will be governed by the approved end-user terms included with that release.

Official OS lifecycle references: [Windows 10 release information](https://learn.microsoft.com/en-us/windows/release-health/release-information) and [Windows 11 release information](https://learn.microsoft.com/en-us/windows/release-health/windows11-release-information).
