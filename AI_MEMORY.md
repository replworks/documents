# AI_MEMORY.md

## Purpose

This document exists to transfer context between AI sessions.

It is intended to be provided as part of the first prompt when starting a new conversation.

The goal is not to describe the project.

The goal is to preserve decision-making context.

A future AI should be able to continue discussions with similar understanding and reasoning.

---

# Project

Name: ReplWorks Documents

Repository:

<https://github.com/replworks/documents>

Website:

<https://www.repl.net>

---

# What We Are Building

ReplWorks Documents is a collection of AI-oriented project specification templates.

The target audience is developers using AI-assisted development and vibe coding.

The repository is not intended to teach technologies.

The repository exists to provide constraints that reduce AI guessing.

The primary objective is predictable AI behavior.

---

# Philosophy

AI already knows technologies.

Documentation should provide constraints, not tutorials.

Good documentation tells AI:

- what exists
- where things belong
- what is allowed
- what is forbidden

Bad documentation explains React, Laravel, FastAPI, etc.

The project follows:

- AI First
- Constraints Over Knowledge
- Explicit Over Implicit
- Latest Stable Only
- Official Recommendations First
- Do Not Guess

---

# Development Preferences

The project owner prefers:

- strong conventions
- predictable structures
- minimal architectural creativity
- fewer frameworks
- fewer options
- fewer layers

The project owner dislikes:

- unnecessary abstractions
- architecture invented by AI
- speculative folder structures
- excessive flexibility
- legacy compatibility requirements

---

# Framework Selection Criteria

A framework is worth supporting when:

- it is commonly used for new projects
- it has strong conventions
- it has predictable structure
- it is AI-friendly
- it is likely to be used by solo developers, indie hackers, startups, or AI-assisted developers

Popularity alone is not enough.

---

# Current Framework Decisions

Supported:

- VANILLA
- REACT_VITE
- ASTRO
- NEXTJS
- FASTAPI

Planned:

- LARAVEL

Excluded:

- DJANGO
- NUXT
- SVELTEKIT
- SPRING_BOOT
- ASPNET_CORE

Reasons vary, but usually involve:

- low probability of actual usage
- weak convention enforcement
- architectural fragmentation
- poor fit for AI-assisted development

---

# Framework Philosophy

Framework documents should contain:

- stack
- versions
- project structure
- file placement rules
- generation rules
- constraints

Do not split STACK and PROJECT_STRUCTURE into separate documents.

One framework document should contain all framework-related rules.

Examples:

- REACT_VITE.md
- NEXTJS.md
- FASTAPI.md

---

# Version Policy

Version information is important.

AI frequently assumes older versions.

Framework documents should define current major versions.

Project configuration remains the source of truth.

Examples:

- package.json
- pyproject.toml

If project configuration exists, follow it.

Otherwise follow framework specifications.

---

# FastAPI Decision

FastAPI should remain minimal.

Do not introduce:

- services
- repositories
- controllers

unless explicitly requested.

FastAPI is treated as an API framework.

Not a full-stack framework.

---

# Django Decision

Django was intentionally excluded.

Reasoning:

- highly fragmented architecture styles
- inconsistent project structures
- heavy customization across teams
- difficult for AI to predict correctly

The issue is not technical quality.

The issue is predictability.

---

# Long-Term Direction

Future work may include:

- additional framework specifications
- specification generators
- CLI tooling
- project detection
- framework composition

Potential examples:

- replworks detect
- replworks generate
- replworks validate

Framework specifications may eventually be generated from project dependencies.

Example:

package.json
→ detect stack
→ generate FRAMEWORK.md

---

# Important Context

When making decisions, prioritize:

1. AI predictability
2. simplicity
3. convention over flexibility
4. real-world usage
5. latest stable ecosystem

Do not optimize for theoretical completeness.

Do not optimize for enterprise requirements.

Do not optimize for legacy projects.

Optimize for AI-assisted development.
