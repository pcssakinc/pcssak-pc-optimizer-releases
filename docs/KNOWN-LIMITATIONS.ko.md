# 알려진 제한 — 공개 전 상태

최종 갱신: 2026-08-12

현재 공개 설치 파일은 없습니다.

## 미완료 관문

- Windows 10 22H2 빌드 19045 Home·Pro와 Windows 11 빌드 26100 이상
  Home·Pro x64 실제 행렬 검증
- 100/125/150/200% DPI와 다중 모니터 UI 실기 검증
- 관리자 권한 기능의 실제 삭제·복원·취소·재개 검증
- 드라이버 열거·설치·잔여 드라이버 제거의 물리 PC 검증
- SSD/TRIM, ReFS/Dev Drive 및 잠긴 파일 실패 안내 검증
- WPR/WPA 기반 성능 A/B 측정
- 설치·업데이트·제거 및 롤백 검증
- 코드 서명, SmartScreen 및 주요 보안 제품 오탐 점검
- 라이선스·제3자 고지·개인정보 문서 최종 승인
- 실제 계약·배포 주체의 법적 명칭과 법무 승인 참조는 아직 확정되지 않았습니다.
- 독립 게시자 인증서 SHA-256 신뢰 핀과 별도 릴리스 승인은 `NOT_CONFIGURED`입니다.
- 실제 서명·백신 오탐·Windows 실기·공개 게시·태그 생성은 `NOT_RUN`입니다.

## 첫 후보 지원 범위

- Windows x64 전용이며 32비트는 지원하지 않습니다.
- 설치기의 기술적 하한은 Windows 10 빌드 17763이지만, 이 수치는 공개 지원 보장이
  아닙니다. 일반 Windows 10 지원은 종료됐으므로 지원되는 Windows 11 또는 적격
  Windows 10 ESU 환경을 권장합니다.
- 무료 공개 베타에는 Pro 등록이 없으며, 개발용 라이선스 키도 포함하지 않습니다.

자동 시험 통과만으로 위 항목을 완료했다고 주장하지 않습니다. `NOT_CONFIGURED`와
`NOT_RUN`은 성공이 아닙니다. 각 릴리스에는 실제로 통과한 범위와 남은 제한을
별도로 공개합니다.

공식 OS 수명주기: [Windows 10 릴리스 정보](https://learn.microsoft.com/en-us/windows/release-health/release-information), [Windows 11 릴리스 정보](https://learn.microsoft.com/en-us/windows/release-health/windows11-release-information)
