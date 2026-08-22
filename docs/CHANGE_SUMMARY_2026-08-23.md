# 2026-08-23 변경 요약 — PCssak 0.8.0 미서명 무료 얼리액세스

## 작업 기준

- 원격 저장소: `pcssakinc/pcssak-pc-optimizer-releases`
- 최신 `main` 기준 SHA: `54c341d6d2ea2ff38cdac85d907b4f516a90eb97`
- 작업 브랜치: `codex/unsigned-free-ea-v080-20260823`
- 변경 범위: 공개 정책·안전·현지어 안내 문서와 Issue 버전 예시
- 제외 범위: 실제 태그, GitHub Release, 실행 파일, ZIP 자산, 서명, 홈페이지 배포

## 선행 정리

- 공개 명칭·영어 기본 진입점 PR #4의 exact head
  `c5746a86dc0b02cb84646e45308ac1e1eccc6588`을 확인한 뒤 squash 병합했습니다.
- 과거 PR #2는 오래된 설치기·서명/CMS 계약이 새 `0.8.0` 휴대용 미서명 정책과
  충돌하므로 영어 설명을 남기고 종료했습니다.

## 문서 계약

- 첫 공개 시험판을 `PCssak 0.8.0 Unsigned Free Early Access`로 정의했습니다.
- 정확한 Windows x64 휴대용 자산명을
  `PCSSAK_0.8.0_x64_Portable.zip`으로 고정했습니다.
- 설치기와 자동 다운로드·실행·설치·롤백을 제공하지 않는 경계를 명시했습니다.
- 미서명, 알 수 없는 게시자, SmartScreen·백신 경고 가능성을 공개하고 서명·게시자
  확인·외부 법률 검토·SmartScreen 평판·전체 Windows 실기를 `PASS`로 표현하지
  않도록 했습니다.
- 서명·외부 법률 검토를 미뤄도 SHA-256, SBOM, 제3자 고지, Qt 런타임 매니페스트,
  Qt/PySide 대응 소스와 개인정보·지원 안내 의무는 유지했습니다.
- 정확한 18개 GitHub Prerelease 자산 허용목록과 portable ZIP 내부 안전 계약,
  Draft 검증 후 한 번만 게시하는 불변 릴리스 순서를 영어·한국어로 분리했습니다.

## 글로벌 안내

다음 11개 로케일에 실제 Markdown 릴리스 안내를 추가했습니다.

- `de`, `en`, `es`, `es-419`, `ja`, `ko`, `pt-BR`, `ru`, `tr`, `zh-CN`, `zh-TW`

각 안내는 같은 버전, 정확한 ZIP 파일명, 미서명·SmartScreen 경고, SHA-256 확인,
공식 Releases 경로와 비자동 업데이트 경계를 공유합니다. 법적 통제 원문을 현지어
법률 번역으로 오해하게 만들지 않고, 상세 안전 계약은 영어 정본과 한국어 문서로
연결했습니다.

## 검증 결과

- 11개 언어 파일의 정확한 로케일 집합: PASS
- 11개 파일의 버전·파일명·SmartScreen·SHA-256·Releases·비통과 상태 토큰: PASS
- 전체 Markdown 상대 링크 존재 확인: PASS
- 영어·한국어 공개 자산 허용목록 18개 이름·순서 일치: PASS
- 과거 버전·설치기 자산명 잔존: 0건
- `git diff --check`: PASS
- 실제 태그·Release·릴리스 자산 생성: 0건
- GitHub Actions 실행: 0건

## 다음 단계

1. 이 Draft PR을 검토하고 squash 병합합니다.
2. 비공개 제품 저장소에서 같은 portable 정책과 매니페스트 스키마를 구현·시험합니다.
3. 최종 `0.8.0` 소스 기준점에서 새 휴대용 ZIP과 나머지 17개 자산을 조립합니다.
4. 악성코드 검사와 통제된 압축 해제·실행·종료·정리 스모크 시험을 수행합니다.
5. 18개 자산을 Draft Prerelease에 올려 로컬과 원격의 이름·개수·크기·해시를 비교한
   뒤에만 별도 승인으로 실제 게시합니다.
