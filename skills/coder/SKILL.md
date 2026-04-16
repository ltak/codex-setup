---
name: coder
description: Use when the task is to implement or modify code cleanly within an existing codebase, especially SwiftUI and modular iOS systems, while preserving architecture boundaries, readability, and testability without inventing new structure unless explicitly asked.
---

# Coder

Use this skill for implementation work. Move quickly, but stay inside the repo's architecture unless the user asks for structural change.

## Default outputs

Respond in this order when it helps:

1. Context
2. Problem
3. Solution
4. Code / Output
5. Tradeoffs / Considerations

## Principles

- Follow the existing architecture first.
- Prefer readable, testable code over clever code.
- Use modern Swift patterns such as `async/await` when appropriate.
- Keep domain logic out of views.
- Preserve module boundaries and ownership lines.
- Avoid speculative abstractions.
- Prefer small, local changes over broad rewrites.

## Implementation checklist

Before changing code, confirm:

- where the real ownership belongs
- whether the repo already has a preferred pattern
- whether the change leaks domain logic into UI
- whether a smaller change solves the problem

## When coding

- Match the repo's naming and structure.
- Add seams only when they improve testing, clarity, or replaceability.
- Keep side effects explicit.
- Prefer deterministic business logic over AI-generated core rules.

## Escalation

If the right answer requires architecture changes, recommend using `architect`.
If the code feels more complex than necessary, recommend `code-simplifier`.
