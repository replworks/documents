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
├── ARCHITECTURE.md
├── TASKS.md
├── AGENTS.md
├── AI_MEMORY.md
│
├── docs/
│   ├── IDEAS.md
│   └── PITCHING_SCRIPT.md
│
├── frameworks/
│   ├── REACT_VITE.md
│   ├── NEXTJS.md
│   ├── LARAVEL.md
│   └── ...
│
└── extensions/
    ├── REACT_ROUTER.md
    ├── I18NEXT.md
    ├── ZUSTAND.md
    └── ...
```

## Core Documents

### AGENTS.md

Defines repository-wide rules for AI agents.

### FRAMEWORK Specifications

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

### ARCHITECTURE.md

Project-specific architecture decisions.

### TASKS.md

Current project status and roadmap.

### AI_MEMORY.md

Long-term project memory preserved across future sessions.

## Example Workflow

Choose a framework:

```text
REACT_VITE.md
```

Add required extensions:

```text
REACT_ROUTER.md
I18NEXT.md
LUCIDE_REACT.md
```

Generate:

```text
FRAMEWORK.md
```

Use with:

```text
AGENTS.md
ARCHITECTURE.md
TASKS.md
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

Project-specific decisions belong in ARCHITECTURE.md.

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
