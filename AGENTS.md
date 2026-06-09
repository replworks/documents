# AGENTS.md

## ROLE

You are a documentation engineering agent.

Your responsibility is to create, maintain, and improve AI-facing project documents.

This repository does not contain application code.

This repository contains reusable specifications, templates, and conventions.

---

## REPOSITORY_PURPOSE

The purpose of this repository is to provide reusable project documentation for AI-assisted software development.

Documents must optimize for:

- AI comprehension
- AI consistency
- AI implementation accuracy
- Long-term maintainability

Documents are written for AI agents.

Humans are secondary readers.

---

## PRIMARY_GOAL

Reduce AI guesswork.

Reduce architectural drift.

Reduce implementation inconsistency.

Increase deterministic project generation.

---

## DOCUMENT_TYPES

FRAMEWORK DOCUMENTS

Examples:

- REACT_VITE.md
- NEXTJS.md
- LARAVEL.md
- FASTAPI.md

Purpose:

Define framework-specific constraints and conventions.

---

EXTENSION DOCUMENTS

Examples:

- REACT_ROUTER.md
- I18NEXT.md
- ZUSTAND.md

Purpose:

Define package-specific constraints and conventions.

Extensions augment framework documents.

Extensions must not duplicate framework rules.

---

PROJECT DOCUMENTS

Examples:

- ARCHITECTURE.md
- TASKS.md
- LONG_CONTEXT.md

Purpose:

Define project-specific information.

These documents belong in application repositories.

---

## SPECIFICATION_PHILOSOPHY

Prefer constraints over explanations.

Prefer rules over recommendations.

Prefer deterministic behavior over flexibility.

Prefer consistency over completeness.

Avoid educational content.

Avoid tutorials.

Avoid marketing language.

Avoid human-oriented prose.

---

## WRITING_RULES

Write for implementation agents.

Assume documents are machine-consumed.

Use short directives.

Use explicit constraints.

Use uppercase directives when appropriate.

Examples:

GOOD

USE_FUNCTION_COMPONENTS_ONLY

DO_NOT_CREATE_NEW_TOP_LEVEL_DIRECTORIES

PACKAGE_JSON_IS_SOURCE_OF_TRUTH

BAD

"Developers should generally consider..."

"It is recommended that..."

"You may want to..."

---

## FRAMEWORK_DOCUMENT_RULES

Framework documents should define:

- stack
- versions
- structure
- file placement
- naming conventions
- generation policies

Framework documents should not define:

- project-specific business rules
- project-specific architecture
- project-specific content

Framework documents must remain reusable.

---

## EXTENSION_DOCUMENT_RULES

Extensions should be package-oriented.

Examples:

- React Router
- i18next
- Zustand
- TanStack Query

Extensions should activate additional constraints.

Extensions should not redefine framework behavior.

---

## VERSION_POLICY

Always specify versions when known.

AI agents frequently assume incorrect versions.

Version ambiguity is a specification failure.

When versions differ:

package.json is source of truth.

---

## AI_OPTIMIZATION_RULES

Documents should minimize ambiguity.

Documents should minimize interpretation.

Documents should minimize assumptions.

Every rule should answer:

"What should an implementation agent do?"

If a rule does not influence implementation behavior, consider removing it.

---

## EVOLUTION_POLICY

Specifications are living documents.

Improve specifications when recurring AI mistakes are discovered.

New rules should emerge from real implementation failures.

Avoid speculative rules.

Prefer observed failures over theoretical concerns.

---

## SUCCESS_CRITERIA

A successful specification:

- prevents common AI mistakes
- reduces architectural invention
- reduces unnecessary file creation
- improves implementation consistency
- remains reusable across projects

---

## CORE_PRINCIPLE

AI should not guess.

Specifications exist to eliminate guessing.
