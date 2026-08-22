# PCssak - 공식 미서명 무료 얼리액세스

**기본 언어:** [English](README.md) · 한국어

**릴리스 안내:**
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

이곳은 PCSSAK의 핵심 Windows 관리·개인정보 보호 도구인 **PCssak**의 공식 공개
배포·검증 저장소입니다. 제품 소스와 내부 개발 증거는 별도의 비공개 저장소에서
관리합니다.

## 현재 상태

> [!IMPORTANT]
> 이번 문서 변경은 태그, Release, 실행 파일 또는 압축 파일을 게시하지 않습니다.

첫 공개 시험 패키지는 **PCssak 0.8.0 미서명 무료 얼리액세스**로 준비합니다.
Windows x64 휴대용 압축 파일의 정확한 이름은 다음과 같습니다.

```text
PCSSAK_0.8.0_x64_Portable.zip
```

무료 얼리액세스 단계에서는 의도적으로 코드 서명을 제공하지 않습니다. Authenticode
게시자 확인, 외부 법률 전문가 검토, SmartScreen 평판과 전체 Windows 실기 행렬은
향후 상용판으로 미룹니다. 이 상태는 `PASS`로 표시하지 않고 연기 또는 미실행으로
정확하게 공개합니다.

무료 얼리액세스라고 해서 제3자 라이선스 의무가 연기되는 것은 아닙니다. 공개
Prerelease에는 정확한 해시, SBOM, 제3자 고지, Qt 런타임 매니페스트와 필요한
Qt/PySide 대응 소스 압축 파일이 계속 포함되어야 합니다.

## 패키지 계약

| 항목 | 첫 공개 시험 정책 |
|---|---|
| 버전 | `0.8.0` |
| 채널 | 미서명 무료 얼리액세스 |
| 아키텍처 | Windows x64 전용 |
| 형식 | 설치기 없는 휴대용 ZIP |
| 압축 파일 | `PCSSAK_0.8.0_x64_Portable.zip` |
| 공개 배포자 표기 | PCSSAK |
| GitHub 태그 | 실제 Prerelease를 게시할 때만 `v0.8.0` |
| 코드 서명 | 이 단계에서는 제공하지 않음 |
| 업데이트 | 사용자가 확인을 요청하면 상태를 표시하고, 새 버전이 있을 때 사용자가 별도 공식 다운로드 페이지 버튼을 누를 수 있음 |

이 단계의 공개 배포자 표기는 PCSSAK입니다. 실행 파일이 미서명이므로 이 표기는
Authenticode로 검증된 게시자 정체성이 아닙니다.

## 공식 다운로드 확인 방법

1. `v0.8.0` Prerelease가 실제로 보인 뒤 이 저장소의
   [Releases](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases)
   화면에서만 받습니다.
2. 위의 정확한 압축 파일명을 확인합니다.
3. 같은 Release의 `SHA256SUMS.txt`에 기록된 SHA-256과 압축 파일을 비교합니다.
4. 해시가 없거나 다르면 압축 파일과 추출한 파일의 실행을 중단합니다.
5. `PCSSAK.exe`를 실행하기 전에 최신 보안 제품으로 압축 파일과 추출 폴더를
   검사합니다.

실행 파일이 미서명이므로 Windows에서 **알 수 없는 게시자**, SmartScreen 또는
백신 경고가 표시될 수 있습니다. 경고는 악성이라는 확정도, 안전하다는 보장도
아닙니다. 출처·파일명·해시·동작을 확인할 수 없으면 중단하고 제보해 주세요.

업데이트 확인은 페이지를 자동으로 열지 않습니다. 패키지를 자동으로 다운로드·실행·
설치하거나 롤백하지 않습니다.

## 휴대용 패키지 동작

- 사용자 소유 폴더에 압축을 풀고 Windows나 다른 보호된 시스템 폴더에는 풀지 않습니다.
- 휴대용은 설치기를 사용하지 않는다는 의미입니다. 설정·로그·격리 기록·복구 자료를
  로컬에 전혀 남기지 않는다는 의미가 아닙니다.
- 추출한 프로그램 폴더를 지워도 별도로 저장된 로컬 자료가 자동 삭제되지는 않습니다.
  해당 Release의 `UNINSTALL_AND_LOCAL_DATA.md`를 따르세요.
- 첫 무료 얼리액세스 범위는 의도적으로 제한됩니다. 실측을 수집하는 동안 시스템 변경
  기능과 Pro 기능은 제공되지 않을 수 있습니다.

## 게시·안전 문서

- [알려진 제한](docs/KNOWN-LIMITATIONS.ko.md)
- [품질·안전 기준](docs/QUALITY-AND-SAFETY.ko.md)
- [공개 자산 기준](docs/RELEASE_ASSET_STANDARD.ko.md)
- [보안 제보](SECURITY.md)
- [지원·개인정보 안내](SUPPORT.md)

## 저장소 경계

- **이곳에 공개하는 것:** 검증된 Prerelease 자산, 체크섬, SBOM, 승인된 고지,
  대응 소스 압축 파일, 현지어 안내와 비식별 공개 Issue
- **이곳에 공개하지 않는 것:** 제품 소스, 서명 키, 토큰, 고객 개인정보, 원본
  ETL/DMP/EVTX·로그·영상 증거, 내부 사고 보고서, 미검증 빌드
- 이 저장소는 비공개 제품 소스를 오픈소스로 만들거나 게시된 패키지의 사용 조건을
  넘어서는 권리를 부여하지 않습니다.
