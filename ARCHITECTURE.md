# ARCHITECTURE.md

# ReplWorks Documents Architecture

## 개요

ReplWorks Documents는 AI 에이전트 기반 개발을 위한 문서 템플릿 저장소이다.

이 저장소의 목적은 프로젝트 문서를 표준화하는 것이 아니라,

AI가 프로젝트를 이해하기 위해 필요한 컨텍스트를 계층적으로 제공하는 것이다.

---

# 핵심 개념

AI는 프로젝트를 직접 이해하지 않는다.

AI는 입력된 컨텍스트를 통해 프로젝트를 이해한다.

따라서 프로젝트의 품질은 AI 모델 자체보다 컨텍스트 품질에 크게 의존한다.

ReplWorks Documents는 이 컨텍스트를 구조화하기 위한 문서 아키텍처를 제공한다.

---

# 컨텍스트 계층

프로젝트 컨텍스트는 다음 계층으로 구성된다.

```text
LONG_CONTEXT
    ↓
ARCHITECTURE
    ↓
FRAMEWORK
    ↓
TASKS
    ↓
AGENT EXECUTION
```

---

## LONG_CONTEXT

가장 상위 계층.

프로젝트가 존재하는 이유를 설명한다.

포함 내용:

- 제품 비전
- 목표 사용자
- 핵심 가치
- 장기 방향성
- 해결하려는 문제

질문:

"왜 이 프로젝트를 만드는가?"

---

## ARCHITECTURE

시스템 구조를 설명한다.

포함 내용:

- 주요 구성 요소
- 계층 구조
- 데이터 흐름
- 책임 분리

질문:

"이 프로젝트는 어떻게 구성되는가?"

---

## FRAMEWORK

기술 스택과 개발 규칙을 설명한다.

포함 내용:

- 사용 기술
- 폴더 구조
- 네이밍 규칙
- Import 규칙
- 금지 사항

질문:

"어디에 무엇을 만들어야 하는가?"

---

## TASKS

현재 작업 상태를 정의한다.

포함 내용:

- 현재 작업
- 우선순위
- 완료 상태
- 다음 단계

질문:

"지금 무엇을 해야 하는가?"

---

## AGENTS

에이전트 행동 규칙을 정의한다.

포함 내용:

- 작업 절차
- 검증 절차
- 문서 참조 순서
- 실패 시 행동

질문:

"어떻게 행동해야 하는가?"

---

# 문서 의존성

```text
LONG_CONTEXT
        ↓
ARCHITECTURE
        ↓
FRAMEWORK
        ↓
TASKS
        ↓
AGENTS
```

상위 문서는 하위 문서에 영향을 준다.

하위 문서는 상위 문서를 변경하지 않는다.

예:

- TASKS는 ARCHITECTURE를 변경할 수 없다.
- FRAMEWORK는 LONG_CONTEXT를 변경할 수 없다.

---

# 프레임워크 템플릿 구조

저장소는 프레임워크별 규칙을 템플릿으로 제공한다.

```text
frameworks/
 ├─ REACT_VITE.md
 ├─ NEXTJS.md
 ├─ LARAVEL.md
 ├─ FASTAPI.md
 └─ DJANGO.md
```

새 프로젝트 생성 시 적절한 템플릿을 선택하여 FRAMEWORK.md로 복사한다.

```text
REACT_VITE.md
        ↓
project/FRAMEWORK.md
```

---

# 설계 원칙

## AI First

모든 문서는 AI 소비를 우선한다.

---

## Explicit Over Implicit

규칙은 추론하지 않는다.

명시한다.

---

## Constraints Over Knowledge

AI는 이미 기술을 알고 있다.

문서는 기술 설명보다 프로젝트 제약조건을 제공해야 한다.

---

## Consistency Over Flexibility

프로젝트마다 문서 구조가 달라지지 않는다.

동일한 문서 구조를 유지한다.

---

# 최종 목표

AI가 프로젝트를 추측하도록 만드는 것이 아니라,

문서를 통해 프로젝트를 이해하도록 만드는 것.

ReplWorks Documents는 이를 위한 표준 컨텍스트 구조를 제공한다.
