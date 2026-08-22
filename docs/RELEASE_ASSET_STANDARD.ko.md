# PCssak 0.8.0 휴대용 공개 자산 기준

검증하지 않은 로컬 `dist` 폴더에서 공개 자산을 직접 복사하거나 과거 내부 빌드의
이름만 바꿔 게시하지 않습니다.

첫 공개 시험 정체성은 다음과 같습니다.

- 제품: `PCssak`
- 공개 배포자 표기: `PCSSAK`
- 버전·표시 버전: `0.8.0`
- 채널: `free-ea`
- 아키텍처: `x64`
- GitHub 태그: `v0.8.0`
- 배포 형식: 설치기가 아닌 휴대용 ZIP
- 기본 압축 파일: `PCSSAK_0.8.0_x64_Portable.zip`

이 정책 문서는 태그, Release 또는 압축 파일을 생성하지 않습니다. 실행 파일이
미서명이므로 공개 배포자 표기를 Authenticode로 검증된 게시자 정체성처럼 표현하지
않습니다.

## 정확한 18개 자산 허용목록

실제 `v0.8.0` Draft Prerelease에는 다음 파일만 정확히 포함합니다.

```text
PCSSAK_0.8.0_x64_Portable.zip
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

예상하지 않았거나 누락·중복됐거나 대소문자가 다른 자산, 심볼릭 링크 또는 재분석
지점 자산이 있으면 게시를 차단합니다.

## 휴대용 압축 파일 계약

`PCSSAK_0.8.0_x64_Portable.zip`은 다음 조건을 만족해야 합니다.

- 과거 내부 RC의 이름을 바꾸지 않고 승인된 `0.8.0` 소스 기준점에서 생성
- 최상위 `PCssak-0.8.0-x64/` 폴더 하나와 그 아래의 공개 실행 파일
  `PCSSAK.exe` 포함
- 절대 경로, 드라이브 지정 경로, 상위 경로 이동, 대체 데이터 스트림, 심볼릭 링크,
  재분석 지점 또는 대소문자를 무시한 중복 경로 금지
- 서명 키, 토큰, 비공개 로그, 원본 시험 증거, 개발 라이선스, 내부 매니페스트,
  `_test` 실행 파일 또는 무관한 프로그램 금지
- 앱에 버전 `0.8.0`을 표시하고 `RELEASE_MANIFEST.json`의 버전 정체성과 일치
- 오프라인에서도 확인할 수 있도록 사용자용 라이선스, 개인정보, 제3자 고지,
  업데이트·롤백과 로컬 데이터 제거 문서 포함
- 빌드 절차가 정한 검토된 결정적 구성원 순서와 시각을 사용해 같은 후보를 재현·비교
- 최종 압축 바이트와 SHA-256이 고정된 뒤 악성코드 검사와 스모크 시험 수행

## 미서명 상태 계약

무료 얼리액세스 단계의 실행 파일은 의도적으로 미서명입니다.

- `RELEASE_MANIFEST.json`과 `RELEASE_NOTES.md`는 Authenticode 서명, 게시자 인증서
  확인, RFC 3161 타임스탬프, SmartScreen 평판과 외부 법률 전문가 승인을
  `DEFERRED` 또는 `NOT_RUN`으로 기록해야 합니다.
- 문서, UI, 체크섬, 증명 또는 파일명이 코드 서명이나 게시자 확인을 통과한 것처럼
  표현해서는 안 됩니다.
- 빈 서명, 자체 발급 인증서, 이름을 바꾼 내부 승인 또는 조작한 `PASS` 증거를
  첨부해서는 안 됩니다.
- Windows 경고는 릴리스 노트와 현지어 안내에 공개하되 안전 또는 악성의 증거라고
  설명하지 않습니다.

## 무결성·준수 계약

- `RELEASE_MANIFEST.json`은 소스 커밋, 버전, 채널, 아키텍처, 휴대용 압축 목록,
  빌드 환경과 모든 payload의 크기·SHA-256을 결속합니다.
- `SHA256SUMS.txt`는 휴대용 ZIP과 릴리스 매니페스트를 포함한 나머지 17개 자산을
  소문자 SHA-256, 공백 두 칸, 정확한 파일명과 LF 형식으로 덮습니다.
- `PCSSAK-SBOM.spdx.json`은 SPDX 2.3 JSON이며 닫힌 런타임 의존성 집합을 휴대용
  압축 파일 해시에 결속합니다.
- `THIRD_PARTY_LICENSES.zip`은 결정적이며 구성원 경로·크기·해시와 라이선스 원문을
  독립 검증합니다.
- `QT_RUNTIME_MANIFEST.json`은 휴대용 후보에서 추출한 정확한 Qt 런타임 경로·크기·
  SHA-256을 기록합니다.
- 정확한 Qt 6.11.1과 PySide6 6.11.1 대응 소스 압축 파일을 같은 GitHub
  Prerelease에 첨부하고 승인된 공식 크기·해시와 비교합니다.
- `RELEASE_SUMMARIES.json`은 `ko`, `en`, `de`, `ja`, `zh-CN`, `zh-TW`, `ru`,
  `es-419`, `es`, `tr`, `pt-BR` 안내를 포함합니다. `docs/locales/`의 렌더링 문서는
  같은 버전·파일명·미서명 경고·검증 절차를 전달해야 합니다.
- 외부 법률 검토를 미뤄도 고지, 소스 제공 또는 다른 제3자 라이선스 자료의 누락을
  허용하지 않습니다.

## Draft·불변 게시 절차

1. 검토된 문서와 릴리스 계약 커밋을 `main`에 병합합니다.
2. 이 공개 저장소 밖에서 완전한 18개 자산 후보를 빌드·검증합니다.
3. 검토된 `main` 커밋을 대상으로 `v0.8.0` **Draft Prerelease**를 만듭니다.
4. Draft를 게시하지 않은 상태에서 18개 자산을 모두 업로드합니다.
5. 로컬과 GitHub의 자산명·개수·크기·SHA-256을 독립 비교합니다.
6. 정확한 ZIP의 악성코드 검사와 통제된 휴대용 스모크 시험 증거를 다시 확인합니다.
7. 연기하지 않은 모든 관문이 통과하고 연기 관문이 정확하게 공개됐을 때 한 번만
   게시합니다.
8. 불변 Release와 로컬 자산을 검증한 뒤 홈페이지 다운로드와 업데이트 메타데이터를
   엽니다.

게시된 태그와 자산은 조용히 교체하지 않습니다. 결함은 `v0.8.1` 같은 새 상위
버전에서 수정합니다.
