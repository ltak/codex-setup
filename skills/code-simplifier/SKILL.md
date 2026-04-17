---
name: code-simplifier
description: Use when the task is to simplify touched code, reduce duplication or indirection, improve naming and clarity, trim over-abstraction, or present good-versus-better-versus-best simplification options while preserving behavior.
---

# Code Simplifier

Use this skill to reduce complexity without changing behavior. Bias toward clarity, explicit ownership, and fewer moving parts.

## Default outputs

Respond in this order when it helps:

1. Context
2. Problem
3. Solution
4. Code / Output
5. Tradeoffs / Considerations

## What to target

- duplication
- unnecessary indirection
- deep nesting
- vague naming
- weak ownership
- leaky abstractions
- protocol spam
- helper layers that hide simple logic

## Working method

- Preserve behavior first.
- Remove complexity before adding structure.
- Prefer local reasoning over generic frameworks.
- If tradeoffs matter, present `good vs better vs best`.

## Red flags

Call out:

- domain logic living in views
- view models mixing rendering and business decisions
- abstractions added before multiple real use cases exist
- interfaces that are broader than their consumers need

## Output preference

Keep recommendations concrete. Show the smallest acceptable simplification first, then better options only if they matter.

## Coaching lens

Teach the user to think in terms of:

- clarity as a performance advantage
- fewer moving parts as lower long-term cost
- explicit ownership as simplification
- removing code before reorganizing code
- preserving behavior while shrinking cognitive load

## Ask when needed

Pause and ask when simplification might change product intent or ownership:

- what behavior must remain identical
- which abstraction is truly paying for itself
- whether the complexity is local or structural
- whether the team needs a cleanup or an architecture fix

## Common mistakes

Call out:

- confusing more abstraction with better design
- preserving dead layers because they once felt strategic
- refactoring names and files without reducing real complexity
- collapsing boundaries that are actually useful
