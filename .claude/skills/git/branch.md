# Git Skill

## 1. 목적

본 문서는 프로젝트에서 Git branch 관리할 때 사용된다. 

## 2. 규칙

Branch 전략에 대해서 설명한다.
main
developer
feature/architect
feature/be
feature/fe
hotfix/name



### 1. main
- 전체 서비스 단위의 최상위 기능 개발 버전이다.
- main branch는 developer가 main으로 push하라는 말이 없으면 진행하지 않는다.

### 2. developer
- 기능 개발의 개별적 집합체이다.
- feature에서의 작업이 모인다. 

### 3. feature/
- 각 기능에 따른 개별적 개발 branch이다. 

### 4. hotfix/
- 오류나 버그가 생겼을때 임시적으로 만들어지고 developer의 요구에 따라 삭제될 수 있다. 