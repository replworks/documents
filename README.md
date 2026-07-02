# ReplWorks Documents

AI-first project specifications for consistent software development.

## Why?

Modern AI coding agents are excellent at writing code but often struggle with project consistency.

Without clear constraints, AI agents tend to:

- invent new folder structures
- create unnecessary files
- introduce inconsistent patterns
- assume incorrect framework versions
- drift away from established architecture

ReplWorks Documents provides reusable specifications that reduce guesswork and improve implementation consistency.

The goal is simple:

> AI should not guess.

## Philosophy

Traditional documentation is written for humans.

ReplWorks Documents is primarily written for AI agents.

Specifications focus on:

- constraints
- conventions
- structure
- deterministic behavior

Instead of explaining how frameworks work, these documents define how projects should be implemented.

## Repository Structure

```text
.
├── AGENTS.md
├── AI_MEMORY.md
├── .repl/
│   ├── agent.md
│   ├── architecture.md
│   └── tasks.md
│
├── prompts/
│   ├── AI_MEMORY_PROMPT.txt
│   ├── ARCHITECTURE_PROMPT.txt
│   ├── BLOG_PROMPT.txt
│   ├── DEVELOPMENT_LOG_PROMPT.txt
│   ├── FRAMEWORK_DISCOVERY.txt
│   ├── FRAMEWORK_PROMPT.txt
│   ├── IDEAS_PROMPT.txt
│   ├── JOURNAL_PROMPT.txt
│   ├── PITCHING_SCRIPT_PROMPT.txt
│   ├── PRODUCT_SPEC_PROMPT.txt
│   ├── REVIEW_IMPLEMENTATION_READINESS_PROMPT.txt
│   └── TASKS_PROMPT.txt│
└── frameworks/
    ├── react-vite.md
    ├── nextjs.md
    ├── laravel.md
    └── ...
```

## Core Documents

### AGENTS.md

Defines repository-wide rules for AI agents.

### Framework Specifications

Framework-specific conventions and constraints.

Examples:

- React + Vite
- Next.js
- Laravel
- FastAPI

### Extension Specifications

Package-specific rules that augment framework specifications.

Examples:

- React Router
- i18next
- Zustand
- TanStack Query

### architecture.md

Project-specific architecture decisions.

### tasks.md

Current project status and roadmap.

### AI_MEMORY.md

Long-term project memory preserved across future sessions.

## Example Workflow

Choose a framework:

```text
react-vite.md
```

Add required extensions:

```text
react-router.md
i18next.md
lucide-react.md
```

Generate:

```text
framework.md
```

Use with:

```text
agent.md
architecture.md
tasks.md
```

The AI agent now has deterministic implementation rules instead of making assumptions.

## Design Principles

### Constraints Over Explanations

Prefer:

```text
DO_NOT_CREATE_NEW_TOP_LEVEL_DIRECTORIES
```

Over:

```text
Developers should generally avoid...
```

### Structure Over Flexibility

Consistency is more valuable than unlimited freedom.

### Versions Matter

Framework specifications should define versions.

AI agents frequently assume incorrect versions when versions are not explicitly stated.

### Reuse Over Reinvention

Framework specifications should be reusable across many projects.

Project-specific decisions belong in architecture.md.

## Validation

Lint markdown files:

```bash
npm run lint
```

Fix markdown issues:

```bash
npm run lint:fix
```

Check formatting:

```bash
npm run format:check
```

Format all documents:

```bash
npm run format
```

Validate repository:

```bash
npm run validate
```

## Status

Work in progress.

Current focus:

- framework specifications
- extension specifications
- specification composition
- AI implementation consistency

## License

MIT
