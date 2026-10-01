# PITCHING_SCRIPT.md

# ReplWorks Documents

## AI 시대의 새로운 프로젝트 문서 표준

---

"AI는 코드를 잘 짭니다."

하지만 실제로 프로젝트를 해보면 다른 문제가 발생합니다.

AI는 React를 알고 있습니다.

AI는 Laravel도 알고 있습니다.

AI는 TypeScript도 알고 있습니다.

그런데 이상하게 프로젝트를 망가뜨립니다.

왜 그럴까요?

---

AI는 기술을 모르는 것이 아닙니다.

프로젝트를 모릅니다.

예를 들어 우리는 다음과 같은 규칙을 당연하게 생각합니다.

- 컴포넌트는 components 폴더에 만든다.
- API 호출은 services 폴더에 만든다.
- Zustand를 사용한다.
- Redux는 사용하지 않는다.
- @ alias를 사용한다.
- 새로운 최상위 폴더는 만들지 않는다.

사람 개발자는 저장소를 몇 분만 둘러보면 이 규칙을 파악할 수 있습니다.

하지만 AI는 그렇지 않습니다.

매번 컨텍스트를 다시 읽고,
매번 규칙을 추론하고,
매번 다른 결론을 내립니다.

그 결과:

- 엉뚱한 폴더 생성
- 중복 코드 작성
- 예상하지 못한 라이브러리 추가
- 아키텍처 위반

같은 문제가 반복됩니다.

---

우리는 이것을 AI의 성능 문제라고 생각했습니다.

하지만 실제로는 문서 문제였습니다.

AI에게 필요한 것은 더 좋은 모델이 아니라 더 좋은 컨텍스트였습니다.

---

ReplWorks Documents는 이 문제를 해결하기 위해 만들어졌습니다.

프로젝트 시작 시 몇 개의 문서를 추가합니다.

```text
AGENTS.md
framework.md
architecture.md
tasks.md
AI_MEMORY.md
```

이 문서들은 사람을 위한 문서가 아닙니다.

AI를 위한 문서입니다.

---

예를 들어 React/Vite 프로젝트라면

framework.md 안에 다음과 같은 규칙이 들어갑니다.

- React 19
- Vite
- TypeScript
- Zustand
- Tailwind

폴더 구조

- pages/
- components/
- hooks/
- services/

규칙

- @ alias 사용
- Redux 사용 금지
- 새로운 최상위 폴더 생성 금지

AI는 더 이상 추측하지 않습니다.

문서를 따릅니다.

---

우리가 발견한 중요한 사실은 이것입니다.

AI는 일반적인 개발 지식보다 프로젝트 규칙을 더 필요로 합니다.

React 사용법은 이미 알고 있습니다.

하지만 현재 프로젝트의 구조는 알지 못합니다.

---

ReplWorks Documents는

"AI에게 프로젝트를 설명하는 방법"

을 표준화하려는 시도입니다.

---

목표는 단순합니다.

어떤 AI를 사용하든

- ChatGPT
- Claude
- Gemini
- Cursor
- Windsurf
- Cline
- Roo

동일한 프로젝트 컨텍스트를 제공할 수 있어야 합니다.

---

우리는 앞으로

AI가 코드를 작성하는 시대가 아니라

AI가 프로젝트 규칙을 따르는 시대가 올 것이라고 생각합니다.

ReplWorks Documents는 그 규칙을 담는 표준 문서 모음입니다.
