# 프로젝트 명칭: CorpBrain AI (기업 문서 지능형 비서 서비스)

## 1. 프로젝트 개요
본 프로젝트는 중소기업(SMB) 및 사내 문서 관리가 미흡한 기업들을 대상으로 하는 B2B 서비스입니다. 산재된 로컬/클라우드 문서 및 이메일을 수집, 정제, 벡터화하여 보안 등급에 따른 맞춤형 답변을 제공하는 AI 비서 솔루션을 구축합니다.

### 핵심 차별점
- **비용 최적화**: 초기 대량 인덱싱 작업 시 로컬 LLM을 활용하여 토큰 비용 절감.
- **데이터 정제**: 중복 문서 제거 및 폴더 구조 자동 최적화.
- **보안/권한**: 직급 및 역할별 접근 제어(RBAC) 적용.
- **확장성**: 초기 인덱싱 후 외부 상용 LLM(OpenAI, Anthropic 등) 연동 가능.

## 2. 에이전트 역할 정의 (Agent Roles)
Antigravity는 다음 역할을 수행하는 에이전트들을 생성하고 Taskboard MCP를 통해 협업을 시작하십시오.

1.  **Project Planner (기획자)**: 전체 로드맵 작성, 요구사항 정의서(PRD) 작성, Taskboard의 최상위 에픽 및 초기 티켓 발행 담당.
2.  **Backend Developer (백엔드 개발자)**: 문서 수집 파이프라인(ETL), 로컬 LLM 연동, Vector DB 구축, API 설계 및 RBAC 로직 구현.
3.  **Frontend Developer (프론트엔드 개발자)**: 대화형 웹 인터페이스, 문서 대시보드, 관리자 설정 페이지 구현.
4.  **UI/UX Designer (디자이너)**: 사용자 경험 설계, 웹 UI 와이어프레임 및 디자인 시스템 가이드라인 작성.

## 3. 기술 스택 및 연동 지침
- **Communication**: Stitch MCP를 통해 각 에이전트 간의 대화 및 상태 공유.
- **Task Management**: Taskboard MCP를 사용하여 모든 일감을 티켓화(To-Do, In Progress, Review, Done).
- **Core Tech**: 
    - LangChain/LlamaIndex (RAG 구현)
    - Local LLM (Ollama 등) & Cloud LLM Hybrid
    - Vector DB (ChromaDB, Pinecone, or Milvus)
    - Frontend: Next.js / Tailwind CSS

## 4. 초기 가동 지침 (Initial Instruction)

Stitch와 Taskboard를 활용하여 다음 순서로 프로젝트를 시작하세요.

### Phase 1: 기획 및 티켓팅 (Project Planner 주도)
1.  Planner는 서비스의 전체 기능을 분석하여 `Backlog`에 초기 티켓들을 생성합니다.
2.  각 티켓에는 `Backernd`, `Frontend`, `Design` 태그를 부여하고 담당 에이전트를 지정합니다.
3.  티켓 예시:
    - [기획] 서비스 아키텍처 및 데이터 흐름 정의
    - [백엔드] 로컬 LLM 기반 문서 인덱싱 모듈 프로토타입 개발
    - [백엔드] Vector DB 스키마 설계 및 RBAC 권한 테이블 설계
    - [프론트엔드] 대화형 챗봇 인터페이스 UI 개발
    - [디자인] 기업용 대시보드 레이아웃 디자인

### Phase 2: 개발 착수 및 업데이트 (각 개발자/디자이너 주도)
1.  각 에이전트는 자신에게 할당된 티켓 중 우선순위가 높은 항목을 `In Progress`로 변경합니다.
2.  작업 수행 중 발생하는 이슈나 설계 결정 사항은 Stitch를 통해 공유하고, 결과물은 Taskboard 티켓의 코멘트로 기록합니다.
3.  단계별로 개발이 완료되면 티켓 상태를 `Review`로 변경하고 다른 에이전트의 피드백을 요청합니다.

## 5. 최종 목표
- Taskboard에서 모든 티켓이 `Done`으로 이동하는 과정을 시각적으로 확인.
- 최종적으로 회사의 문서를 업로드하면 권한에 맞게 답변하는 워킹 프로토타입(MVP) 완성.

---
**Antigravity 지시사항:**
지금 즉시 위 내용을 바탕으로 `Project Planner` 에이전트를 호출하여 Taskboard에 첫 번째 에픽(Epic)과 세부 티켓들을 생성하도록 명령하십시오.