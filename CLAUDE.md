# youthbible.github.io 작업 입구

GitHub Pages 정적 페이지. 병합 = 바로 공개 (배포 단계·검사 도구 없음). 공통 작업 방식 = `claude-home/CLAUDE.md`

## 주인

- 루트 (`index.html`·`login.html`·`privacy.html`·`terms.html`) = 예약 시스템 (`youthbible/reservation_system`, 규칙 원본 = 그 `apps/reservation_system/docs/MAINTENANCE.md` §2·§7·§8)
- `anatomy/` = 해부학 코치 프로젝트 몫 (예약 규칙과 무관, 서로 파일 건드리지 않음)

## 로그인 페이지 고정 규칙 (`login.html`, 원본 = 이 절)

- `MAIN_APP_URL` = 예약 운영 웹앱 Deployment `…-varA` 그대로. 바꾸지 않음 (새 Deployment = 로그인 끊김)
- `next` 목록 = 예약 화면 (`dept`·`study`·`vehicle`·`external`·`admin`·`my`·`accounts`). 예약에 화면 추가 = 같이 고침
- 30일 유지 토큰 (localStorage `rsv_keep_login`)·중복 클릭 방지·15초 넘으면 '다시 시도' = 유지
- 도메인 바뀜 = GCP '승인된 JavaScript 원본' + 예약 설정 `GATEWAY_URL` 같이 (사용자)
- 수집 개인정보 바뀜 = `privacy.html` 같이

## 확인

- 병합 직후 = 페이지 주소 응답 (PC RC `curl`, 클라우드 = proxy 막힘 가능) + 로그인 흐름 = 사용자에게 지금 확인 요청
