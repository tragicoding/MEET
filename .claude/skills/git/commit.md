# Git Skill

## 1. 목적

본 문서는 프로젝트에서 Git 작업을 수행할 때 따르는 규칙을 정의한다.

목표는 다음과 같다.

- Commit History의 가독성을 유지한다.
- 변경 목적을 명확하게 기록한다.
- 하나의 Commit에 하나의 논리적 변경만 포함한다.
- 자동화된 Changelog, Release Note, Semantic Versioning과 연계 가능한 형태를 유지한다.
- 위험한 Git 작업을 방지한다.

---

# 2. Commit Message 규칙

Commit Message는 기본적으로 Conventional Commits 형식을 따른다.

형식:

```text
<type>(<scope>): <subject>

<body>

<footer>
```
scope, body, footer는 필요한 경우에만 작성한다.

최소 형식:
<type>: <subject>

예:
feat: add schedule creation feature

또는:
feat(calendar): add schedule creation modal

커밋 타입은 예를 들어 다음과 같다.
| Type | 의미 |
|---|---|
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `refactor` | 기능 변화 없는 코드 구조 개선 |
| `docs` | 문서 수정 |
| `test` | 테스트 추가 또는 수정 |
| `style` | 코드 동작에 영향을 주지 않는 포맷 수정 |
| `perf` | 성능 개선 |
| `build` | Build System 또는 Dependency 변경 |
| `ci` | CI/CD 설정 변경 |
| `chore` | 기타 유지보수 작업 |
| `revert` | 기존 Commit 되돌리기 |

# 3. Subject 규칙
Subject는 Commit의 변경 내용을 한 줄로 명확하게 설명한다.
규칙:
1. 짧고 구체적으로 작성한다.
2. 명령형 또는 현재형으로 작성한다.
3. 불필요한 마침표를 붙이지 않는다.
4. update, modify, change처럼 의미가 모호한 표현만 사용하지 않는다.
5. 무엇을 왜 변경했는지 유추할 수 있도록 작성한다.
6. 하나의 Commit에 여러 목적을 나열하지 않는다.

# 4. Body 규칙
단순한 변경은 Subject만으로 충분하다.
복잡하거나 중요한 변경은 Body를 작성한다.
Body에는 다음 내용을 작성할 수 있다.
- 변경 이유
- 기존 문제
- 핵심 구현 방식
- 중요한 제약사항
- 영향 범위

# 5. Staging 규칙
가능하면 변경 목적별로 선택적으로 Stage한다.
권장:
git add apps/api/schedule/
git add tests/schedule/

또는:
git add -p

모든 파일을 무조건 Stage하는 것은 피한다.
git add .

git add .는 변경 범위를 충분히 확인한 경우에만 사용한다.

