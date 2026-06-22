# 경력 탐색 서비스 데이터 파이프라인 및 백엔드 API 서버 구축 — 제안 분석 로그

> 생성일: 2026-06-22
> 공고 URL: https://www.wishket.com/project/156263/

## 1. 공고 파싱 결과

```yaml
job:
  title: "경력 탐색 서비스를 위한 데이터 수집 파이프라인 및 백엔드 API 서버 구축"
  category: "개발 기타 / 기타(내부 시스템)"
  budget_range: "5,000,000원"
  duration: "90일"
  tech_stack: ["개발사 자유 제안 (Python/FastAPI 권장)", "RDBMS", "공공 Open API", "LLM/RAG(선택)"]
  description: "데이터 기반 경력 탐색 서비스 백엔드 API + ETL 데이터 파이프라인 MVP. 직군 선택 시 자격증·시험 합격률 데이터 제공. 경산시 청년 예비 창업가 육성 사업 지원. 프론트는 내부 자체 개발."
  requirements:
    - "DB/테이블 스키마 설계 + 인덱스 설계 + 확장 고려"
    - "공공 데이터 Open API 연동(고용통계/커리어넷/워크넷), Rate Limit 고려한 수집 로직"
    - "ETL: Raw 데이터 추출·변환·적재 + 주기적 자동 업데이트 배치/스케줄러"
    - "RESTful API 서버 (직군→자격증/합격률 조회 API), 단순 테스트 계정 기초 인증"
    - "상세 API 명세서(Swagger/Postman)"
    - "LLM/RAG 맞춤형 보고서 생성 (예산 내 가능 시 선택적)"
  client_questions: []
  deadline: "2026년 06월 29일"
  job_post_url: "https://www.wishket.com/project/156263/"
  urls: []
  images: []
  notes: "정부지원사업, 사업자등록증 필수(개인/법인 가능), 세금계산서 발행 필요"
```

## 2. URL/이미지 분석

참고 URL/이미지 없음 (공고 본문에 레퍼런스 링크·첨부 이미지 미포함).

## 3. 실현 가능성 분석 (내부용)

- 프로젝트 유형: API + 데이터 파이프라인 (백엔드 전용, 프론트 제외) → "가능", 버퍼 +10%
- 기본 공수 (AI 미반영): 설계 8 + ETL 15 + DB 5 + API 12 + QA/문서 8 ≈ 48 M/D (LLM 포함 시 +10 ≈ 58 M/D)
- AI 반영 공수 (BE/DB ~50% 절감 + 버퍼): 기초 ≈ 27 M/D → 달력 약 38일 / LLM 포함 ≈ 33 M/D → 달력 약 46일
- 클라이언트 예상 90일 vs 산정 38~46일: 산정 ≤ 예상 → 90일 그대로 유지, LLM 풀스코프 수용 가능
- 판정: Python/외부 API 연동·크론 배치(P2P Funding), RAG/LLM(AI Agent·Series-B) 경험 보유 → 포함 제안 시 강한 차별화

## 4. 포트폴리오 매칭

| 순위 | 프로젝트 | 매칭 근거 | 점수 |
|-----|---------|----------|------|
| 1 | P2P Funding | Python/Django, 15+ 외부 API 연동, 3종 크론잡 배치 자동화 → ETL 파이프라인·Rate Limit·주기 배치와 직결 | ★★★★★ |
| 2 | AI Agent | RAG 컨텍스트 검색·LLM 연동·프롬프트 엔지니어링 → LLM 맞춤 보고서 과업과 동일 구조 | ★★★★★ |
| 3 | Series-B | 200~300+ REST API, 80+ 엔티티 모델링, ChatGPT AI 보고서 생성 → API 서버 + AI 보고서 양면 커버 | ★★★★☆ |

## 5. 최종 제안 요약

- 지원 금액: 4,250,000원 (클라이언트 예상 5,000,000원의 85%, VAT 별도) — 사용자 확정(85%)
- 지원 기간: 90일 (클라이언트 예상 그대로 유지)
- LLM/RAG 범위: 풀스코프 포함 (사용자 확정)
- 핵심 제안 포인트:
  1. 공공 데이터 수집의 핵심 리스크(Rate Limit·안정성)를 수집 로직 설계 단계부터 반영
  2. 공고 우선순위(파이프라인 → DB → API → LLM)를 마일스톤으로 구성, 단계별 독립 검수
  3. RAG 기반 맞춤형 보고서까지 예산 내 포함 (OpenAI 연동 AI 보고서 경험)
  4. 프론트 자체 개발 전제 → 연동 친화적 API + Swagger 문서 제공
  5. 정부지원사업 행정 절차 이해 (사업자등록증·세금계산서 발행 가능)
- 기술 스택: Python 3.12 · FastAPI · PostgreSQL · SQLAlchemy/Alembic · Celery+Redis · httpx · OpenAI/LangChain · pgvector · Swagger · Docker
