# REPLWorks Documents

**AI가 구현하기 전에, 프로젝트를 먼저 정의하는 문서 체계.**

> **AI should not guess.**

AI coding agent의 문제는 코드를 못 쓴다는 것이 아닙니다. 정보가 부족해도 그럴듯한 코드를 너무 쉽게 만들어낸다는 것입니다.

정의되지 않은 빈칸을 AI가 스스로 채우면, 코드는 동작해도 프로젝트는 의도한 방향에서 벗어납니다.

ReplWorks Documents는 이 문제를 문서로 해결합니다.

- **무엇을 정의해야 하는지** 정해 두고
- **정의되지 않은 것은 질문하거나 멈추도록** 규칙으로 만들고
- 그 문서와 프롬프트를 **한 저장소에서 계속 개선**합니다.

이 저장소는 ReplWorks의 AI-assisted development 문서 체계의 **원본(source repository)** 입니다. 문서 체계 자체를 개발하고 유지하는 곳이며, 애플리케이션 코드는 여기에 없습니다.

## 어떻게 다른가

> 아래는 설명을 위한 예시입니다. 실제 사례로 교체하세요.

### 문서가 없을 때

```text
요청: "회원 목록 페이지를 만들어줘"
AI:   (ORM을 직접 고르고, src/features/ 디렉터리를 새로 만들고, 페이지네이션 방식을 임의로 결정)
```

### 문서가 있을 때

```text
DO_NOT_CREATE_NEW_TOP_LEVEL_DIRECTORIES
DO_NOT_ADD_DEPENDENCIES_NOT_LISTED_IN_TECH_STACK
IF_REQUIREMENT_IS_UNDEFINED_ASK_BEFORE_IMPLEMENTING
```

설명보다 **구현자가 따라야 할 제약**을 우선합니다. 제약은 구현 결과에 직접 영향을 주는 형태로 씁니다.

## 저장소 구성

```text
.
├── AGENTS.md        # 이 저장소를 관리하는 AI agent의 규칙
├── CHANGELOG.md     # 규칙 변경 기록
├── tech-stacks/     # 재사용 가능한 tech stack specification
├── prompts/         # 문서를 만들고 검증하는 프롬프트
├── docs/            # 보조 자료와 기록 (source of truth 아님)
└── package.json     # 문서 검증 도구 (Markdownlint, Prettier, Husky)
```

| 경로           | 역할                                                                    |
| -------------- | ----------------------------------------------------------------------- |
| `AGENTS.md`    | 저장소의 목적, 문서 작성 원칙, specification 관리 방법                  |
| `tech-stacks/` | 특정 프로젝트에 종속되지 않고 여러 프로젝트에서 반복 사용하는 기술 규칙 |
| `prompts/`     | specification 자체가 아니라, specification을 만들고 검증하는 도구       |
| `docs/`        | 작성 과정에서 생긴 보조 기록                                            |

## 사용 방법

1. `prompts/`의 프롬프트로 AI와 함께 프로젝트 문서(요구사항, 기술 스택, 아키텍처, 작업 계획)를 정의합니다.
2. 프로젝트가 쓰는 기술에 맞는 `tech-stacks/`의 specification을 프로젝트에 가져옵니다.
3. 구현 에이전트에게 문서를 전달합니다. 문서에 없는 내용은 에이전트가 질문하거나 멈춥니다.
4. 진행 중 발견한 AI의 실수와 문서의 빈틈을 이 저장소로 되돌려 반영합니다.

## 문서의 원칙

**AI는 추측하지 않습니다.** 정의되지 않은 요구사항은 AI가 임의로 결정하지 않습니다. 정보가 없으면 질문하거나 구현을 중단합니다.

**제약은 명확해야 합니다.** 구현 결과에 직접 영향을 주는 규칙을 설명보다 우선합니다.

**문서는 하나의 책임만 가집니다.** 제품이 무엇인지, 어떤 기술을 쓰는지, 어떻게 동작하는지, 무엇을 구현할지를 한 문서에 섞지 않습니다.

**규칙은 실제 문제에서 나옵니다.** 일어날 수 있는 모든 문제를 미리 규칙으로 만들지 않습니다. 실제 프로젝트에서 반복된 AI의 실수를 관찰하고, 그 문제를 막는 규칙만 추가합니다.

## 운영 방법

```text
실제 프로젝트에서 사용
        ↓
문제 또는 개선점 발견
        ↓
문서 / 프롬프트 개선
        ↓
Markdown 검증 → Commit
        ↓
다른 프로젝트에서 재사용
        ↓
(반복)
```

이 저장소의 문서는 처음부터 완성된 규칙집이 아니라, 실제 개발 경험으로 계속 진화하는 문서 체계입니다.

## 문서를 변경할 때

- **새 요구사항을 발견했다면** 먼저 여러 프로젝트에서 재사용될 규칙인지 판단합니다. 특정 프로젝트에만 필요하다면 그 프로젝트의 문서에 남깁니다.
- **AI의 반복적인 실수를 발견했다면** 이를 막는 specification 또는 prompt를 추가하거나 수정합니다. 근거는 실제로 발생한 문제여야 합니다.
- **기존 규칙을 변경한다면** 해당 specification을 쓰는 프로젝트에 영향이 있는지 확인하고, `CHANGELOG.md`에 기록합니다.

### Pull Request 체크리스트

1. 이 변경이 왜 필요한지 설명했습니다.
2. 기존 문서와 책임이 중복되지 않습니다.
3. 특정 프로젝트의 요구사항을 공통 규칙으로 잘못 추가하지 않았습니다.
4. AI의 실제 구현 문제를 해결하는 변경입니다.
5. 기존 프로젝트에 영향을 줄 수 있는 변경이라면 `CHANGELOG.md`에 기록했습니다.
6. `npm run validate`를 통과합니다.

## 로컬 개발 환경

Node.js 기반 도구로 문서 품질을 검증합니다. Husky가 commit 시점에 변경된 파일의 formatting을 자동으로 관리합니다.

```bash
npm install            # 의존성 설치
npm run validate       # lint + format 전체 검증

npm run lint           # Markdown lint
npm run lint:fix       # lint 자동 수정
npm run format:check   # formatting 확인
npm run format         # formatting 적용
```

## License

MIT
