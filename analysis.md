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

## 6. 최종 산출물 (8단계 출력 전문)

### 제안서 사이트 URL
https://proposal-router.claude-ai-b27.workers.dev/proposal-career-explorer-data-pipeline-api/

### 지원 금액
4,250,000원 (VAT 별도) — 클라이언트 예상 5,000,000원의 85%

### 지원 기간
90일

### 클라이언트 질문 답변
공고 내 별도 질문 없음 — 해당 없음.

### 지원 내용 (전체)

안녕하세요, 경력 탐색 서비스를 위한 데이터 수집 파이프라인 및 백엔드 API 서버 구축 프로젝트에 지원합니다.

본 프로젝트에 대한 상세 제안서(견적서, 공수계산서, PRD, 일정, 포트폴리오)를 별도 페이지로 준비하였습니다.
▶ 제안서 상세 페이지: https://proposal-router.claude-ai-b27.workers.dev/proposal-career-explorer-data-pipeline-api/
▶ 위시켓 포트폴리오: https://www.wishket.com/partners/p/blueverse1/

[프로젝트 분석] 공공 데이터(고용통계·커리어넷·워크넷) 안정적 수집 ETL 파이프라인 + 내부 프론트 연동 RESTful API 서버. Rate Limit·수집 안정성을 설계 단계부터 반영. 공고 우선순위(파이프라인→DB→API→LLM)를 마일스톤으로 구성. LLM/RAG 보고서까지 예산 내 포함 제안.

[작업 일정]
- Phase 1 설계 & 데이터 모델링: Day 1–15
- Phase 2 데이터 파이프라인(ETL): Day 16–45
- Phase 3 백엔드 API 서버: Day 46–66
- Phase 4 LLM/RAG 맞춤형 보고서: Day 67–80
- Phase 5 QA & 배포 & 인수인계: Day 81–90

[마일스톤] M1(D15) 설계 승인 / M2(D45) 파이프라인 가동 / M3(D66) API 완료 / M4(D80) LLM 보고서 / M5(D90) 최종 납품
[산출물] 백엔드·파이프라인 소스코드, DB 설계 문서(ERD), API 명세서(Swagger/Postman)

[협의 필요] 공공 API 키 발급 주체·호출 한도 / 수집 직군·자격증 범위·최신화 주기 / LLM 보고서 형식·OpenAI 비용 부담 / 호스팅 인프라

### 관련 포트폴리오 추천
1. P2P 크라우드펀딩 플랫폼 — Python·외부 API 연동·크론 배치 (ETL 파이프라인 직결)
2. AI-Native 개발 프레임워크 — RAG·LLM 연동·프롬프트 엔지니어링 (맞춤형 보고서 직결)
3. VC 펀드 관리 플랫폼 — 대규모 REST API·DB 모델링·AI 보고서 (API 서버 + LLM 양면 커버)

### 기술 스택
Python 3.12 · FastAPI · PostgreSQL · SQLAlchemy/Alembic · Celery+Redis · httpx · OpenAI/LangChain · pgvector · Swagger · Docker
