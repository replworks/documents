# AI_MEMORY.md

# ReplWorks Memory

Version: 2026-06

---

# Core Understanding

ReplWorks is not a project memory system.

Project memory is only one component.

The actual goal is:

```text
Create a repeatable workflow that turns ideas into shipped products using AI.
```

The original motivation was AI memory loss during development.

However, memory loss was identified as a symptom rather than the root problem.

The root problem is:

```text
How can a solo founder repeatedly transform ideas into production software using AI?
```

ReplWorks exists to answer that question.

---

# ReplWorks Definition

Current definition:

```text
AI-Native Product Development Workflow
```

Alternative definition:

```text
A workflow methodology for turning ideas into software through AI-assisted execution.
```

ReplWorks should be positioned as a workflow system or methodology.

Not as a memory system.

Not as a documentation system.

Not as an AI tool.

---

# Important Discovery

The most valuable asset is not:

- AI_MEMORY.md
- AGENTS.md
- FRAMEWORK.md

The most valuable asset is:

```text
Workflow
+
Document Generation Prompts
+
Validation Prompts
```

The workflow is reusable across projects.

Individual documents are not.

---

# Development Philosophy

The goal is not:

```text
Find a better AI.
```

The goal is:

```text
Create a better workflow.
```

AI models will improve over time.

The workflow should survive model changes.

---

# Workflow

Current ReplWorks workflow:

```text
IDEAS.md
↓
PITCHING_SCRIPT.md
↓
PRODUCT_SPEC.md
↓
ARCHITECTURE.md
↓
FRAMEWORK.md
↓
REVIEW_IMPLEMENTATION_READINESS
↓
TASKS.md
↓
IMPLEMENTATION
↓
AI_MEMORY.md
```

This workflow is currently considered the core of ReplWorks.

---

# Document Responsibilities

## IDEAS.md

Purpose:

```text
Capture the validated product idea.
```

Rules:

- Product idea only.
- No implementation.
- No architecture.
- No technology choices.
- No execution plan.

---

## PITCHING_SCRIPT.md

Purpose:

```text
Persuade a specific audience.
```

Audience may be:

- investors
- VCs
- government programs
- partners
- customers

Expected numbers, assumptions and projections may be included.

Unlike IDEAS.md.

---

## PRODUCT_SPEC.md

Purpose:

```text
Define what the product is.
```

Contains:

- product requirements
- user-visible behavior
- user flows
- acceptance criteria

Does not contain:

- implementation
- architecture
- technologies

Question answered:

```text
What are we building?
```

---

## ARCHITECTURE.md

Purpose:

```text
Define how the product works internally.
```

Contains:

- responsibilities
- flows
- ownership boundaries
- invariants

Does not contain:

- technologies
- frameworks
- libraries

Question answered:

```text
How does the system work?
```

---

## FRAMEWORK.md

Purpose:

```text
Define implementation constraints.
```

Contains:

- language
- stack
- coding conventions
- implementation rules

Question answered:

```text
How should it be built?
```

---

## TASKS.md

Purpose:

```text
Define what remains to be implemented.
```

Contains:

- implementation milestones
- acceptance criteria

Does not contain:

- architecture
- implementation details

Question answered:

```text
What should be built next?
```

---

## AI_MEMORY.md

Purpose:

```text
Preserve decision-making context.
```

Not project documentation.

Not requirements.

Not architecture.

Used for context recovery in future sessions.

---

# Review Strategy

The most important review step is:

```text
REVIEW_IMPLEMENTATION_READINESS
```

Purpose:

```text
Determine whether implementation can begin with confidence.
```

Inputs:

- PRODUCT_SPEC.md
- ARCHITECTURE.md
- FRAMEWORK.md

Expected reviewer:

```text
Execution AI
```

Examples:

- Codex
- implementation-focused agents

Not discussion-oriented models.

---

# Discussion AI vs Execution AI

## Discussion AI

Examples:

- ChatGPT
- Claude

Responsibilities:

- ideation
- specifications
- architecture
- planning
- workflows

Question:

```text
What should we build?
```

---

## Execution AI

Examples:

- Codex

Responsibilities:

- implementation review
- implementation certainty
- execution

Question:

```text
Can this actually be built?
```

---

# Key Insight

Many people combine multiple AI systems.

The value does not come from using different models.

The value comes from separating:

```text
Creation
```

and

```text
Validation
```

ReplWorks should preserve that separation.

---

# AI-Issuer Context

AI-Issuer became an important test project.

Purpose:

```text
Separate AI-generated issues from human-generated issues.
```

Important architectural decision:

```text
Author != Publisher
```

Reason:

Publishing an AI-generated issue under a human account creates implicit ownership and responsibility.

The project attempts to preserve the distinction between:

```text
Content Creation
```

and

```text
Content Publication
```

---

# Current ReplWorks Positioning

Previous positioning:

```text
Project Memory System for AI Development
```

Current positioning:

```text
AI-Native Product Development Workflow
```

Reason:

Memory is only one step in the workflow.

Workflow is the primary product.

---

# Future Direction

ReplWorks should evolve toward:

```text
AI Product Development Methodology
```

Comparable in spirit to:

- Waterfall
- Agile
- Scrum

But designed specifically for AI-assisted software creation.

The long-term goal is not better prompting.

The long-term goal is:

```text
A repeatable system that transforms ideas into shipped products.
```
