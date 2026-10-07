# MEET Project

# Agent Instructions

- 이 CLAUDE.md는 Claude code Agent가 어떻게 행동해야 하는가에 대한 규칙을 명시한 것이고, 반드시 이 규칙을 따라야 한다. 

## 언어 정책 (Language Policy)

1. 프로젝트 문서는 한국어로 작성한다.
2. 기술 용어는 의미의 정확성을 위해 영어를 병행할 수 있다.
3. 코드, 변수명, 함수명, 디렉토리명은 영어로 작성한다.
4. Claude는 작업 계획, 분석 결과, 코드 리뷰 및 검증 결과를 한국어로 보고한다.
5. 외부 라이브러리, Framework 및 API의 공식 명칭은 변경하지 않는다.
6. Developer는 프롬프트를 입력하는 개발자를 가리킨다.
7. 개발된 서비스를 사용하는 사용자는 "End User"라고 한다.

## Agent Routing

작업 유형에 따라 다음 Agent를 우선 사용한다.

- `architect`
  - 프로젝트 기획, 요구사항, Architecture, API 설계, ADR 및 `docs/` 문서 작업

- `backend-implementer`
  - Backend, API, Database 연동, 인증/인가 및 서버 구현

- `frontend-implementer`
  - Page, Component, UI/UX Interaction, 상태 관리 및 API 연동 구현

- `tester`
  - Requirement와 Acceptance Criteria 기반 테스트 및 Validation

- `reviewer`
  - 구현 결과의 Architecture, API, Security, 유지보수성 및 품질 검토

- `release-manager`
  - Git을 관리한다.  

### Routing Rules

1. 기획과 구현이 혼합된 요청은 설계와 구현 단계로 분리한다.
2. 구현 전 필요한 설계가 부족하면 `architect`를 우선 사용한다.
3. Backend와 Frontend가 모두 필요한 기능은 관련 Implementer를 각각 사용한다.
4. 구현 후 필요한 경우 `tester`와 `reviewer`를 사용한다.
5. 각 Agent의 세부 책임과 제약은 해당 Agent 정의를 따른다.