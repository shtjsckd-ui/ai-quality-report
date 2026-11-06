# AI 품질 개선 요청 관리

교육용 가상 데이터 기반의 Next.js 웹앱입니다.

## 현재 구현 범위
- 불량 입력, CSV/Excel 파일 선택, AI 원인 후보 및 개선 요청서 초안 생성
- 작성 시간 기록, AI 초안 활용 여부, 활용률 표시
- 초기 기록은 **브라우저 localStorage**에 저장됩니다. PostgreSQL 연결 전까지 여러 사용자 간 공유되지 않습니다.
- CSV는 8,000자까지 AI에 전달됩니다. **Excel 내용 자동 분석은 아직 미구현**입니다.
- AI Gateway 환경변수 `AI_GATEWAY_MODEL` 및 인증 구성이 필요합니다.

## 실행
`npm install && npm run dev`

## 주의
실제 검사 설비와 연동되지 않으며 AI 진단은 검증이 필요한 가설입니다. 공개 배포 전 서버 측 rate limit, 인증/비용 보호, PostgreSQL 저장 구현이 필요합니다.
