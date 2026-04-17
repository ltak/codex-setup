---
name: product-delivery-router
description: Use when the task is a product development, software development, or software-related knowledge request that may span multiple lifecycle stages such as product thinking, strategy, architecture, implementation, simplification, validation, testing, PR feedback, or review readiness. This skill routes the work through the right existing skills in the right order instead of treating the task as a single undifferentiated coding request.
---

# Product Delivery Router

Use this skill when the user wants help with product or software work that may involve more than one stage of the development lifecycle.

The purpose of this skill is not to replace specialist skills. The purpose is to sequence them well.

## Core rule

For product- and software-related work, bias toward explicit skill use instead of generic reasoning.

Prefer the smallest set of skills that matches the current stage of the work, but if the task spans multiple stages, move through them in order.

## Default lifecycle order

1. strategy
2. clarify
3. design
4. architect
5. implement
6. simplify
7. test
8. validate
9. package

## Skill mapping

Use these skills by stage:

- clarify product intent, scope, or acceptance criteria -> [`product-tactician`](/Users/lucas/.codex/skills/product-tactician/SKILL.md)
- clarify strategy, sequencing, or wedge -> [`founder-thinking`](/Users/lucas/.codex/skills/founder-thinking/SKILL.md)
- clarify UX, hierarchy, and user flow -> [`designer`](/Users/lucas/.codex/skills/designer/SKILL.md)
- define architecture, boundaries, ownership, interfaces -> [`architect`](/Users/lucas/.codex/skills/architect/SKILL.md)
- implement or modify code -> [`coder`](/Users/lucas/.codex/skills/coder/SKILL.md)
- reduce indirection, simplify, clean up touched code -> [`code-simplifier`](/Users/lucas/.codex/skills/code-simplifier/SKILL.md)
- run builds, tests, lint, formatting, and summarize validation -> [`build-validator`](/Users/lucas/.codex/skills/build-validator/SKILL.md)
- think through tests, regression risk, and coverage -> [`tester`](/Users/lucas/.codex/skills/tester/SKILL.md)
- prepare PR framing, reviewer notes, and risk callouts -> [`pr-helper`](/Users/lucas/.codex/skills/pr-helper/SKILL.md)
- handle GitHub PR comments and review threads -> [`pr-comment-responder`](/Users/lucas/.codex/skills/pr-comment-responder/SKILL.md) and [`github:gh-address-comments`](/Users/lucas/.codex/plugins/cache/openai-curated/github/2032fd0291961d866feca472adc8ed6a8cddafc6/skills/gh-address-comments/SKILL.md)

## Preferred multi-pass default

When the task spans real product delivery work, prefer this pass order:

1. `founder-thinking`
2. `product-tactician`
3. `designer`
4. `architect`
5. `coder`
6. `code-simplifier`
7. `tester`
8. `build-validator`
9. `pr-helper`

This is the default backbone for mixed product-and-engineering work.

Do not force every simple task through every stage. Use the full sequence when the work genuinely benefits from multiple passes.

## Routing heuristics

### Start with product thinking before architecture when:

- the user is asking what to build
- scope, goals, or acceptance criteria are still fuzzy
- the request is a product or feature question, not just an implementation request
- success depends on user behavior or business outcome clarity

### Bring in founder thinking when:

- the question is about sequencing, wedge, positioning, differentiation, or leverage
- the user is asking what matters most right now
- the task has product direction implications beyond one feature

### Start with architecture before coding when:

- ownership is unclear
- module boundaries are changing
- persistence or API shape may change
- the user is asking “what is the best way”
- the request smells like a refactor rather than a narrow edit

### Move straight to coding when:

- the change is narrow and local
- ownership is already clear
- the user is asking for concrete implementation
- the design question is already settled

### Bring in simplification when:

- the request mentions cleanup, refactor, readability, or reducing complexity
- implementation reveals avoidable indirection
- a reviewer asks for cleaner structure

### Bring in testing when:

- deterministic logic changes
- regression risk is non-trivial
- acceptance criteria or edge cases matter
- the user asks what to test or whether coverage is enough

### Bring in build validation when:

- code changed and confidence matters
- the repo has a meaningful local validation command
- the user asks if it works, passes, or is ready

### Bring in PR helper when:

- the work is headed to review
- a reviewer-facing explanation is needed
- the user asks for a PR summary or risk notes

## Common software flows

### Feature flow

Use:

1. `founder-thinking`
2. `product-tactician`
3. `designer`
4. `architect`
5. `coder`
6. `code-simplifier`
7. `tester`
8. `build-validator`
9. `pr-helper`

### Bug fix flow

Use:

1. `architect` only if root cause affects ownership or system shape
2. `coder`
3. `code-simplifier` if the fix exposed avoidable complexity
4. `build-validator`
5. `tester`

### Refactor flow

Use:

1. `architect`
2. `code-simplifier`
3. `coder` if behavior-preserving edits still need implementation detail
4. `build-validator`
5. `tester`

### PR comment flow

Use:

1. `pr-comment-responder`
2. `github:gh-address-comments`
3. `architect` for boundary disagreements
4. `code-simplifier` for cleanup asks
5. `tester` for validation concerns
6. `pr-helper` for polished reviewer replies when useful

## Operating posture

- Tell the user which skill or sequence you are using and why.
- Default to asking the minimum high-value questions needed to avoid expensive mistakes.
- Do not drag the user through all stages if the task is simple.
- Do not skip a clearly relevant skill just because implementation has already started.
- Prefer the next correct stage over staying stuck in one mode.
- If the task is product- or software-related, assume at least one skill should be active.
- When multiple stages matter, prefer explicit multi-pass sequencing over one blended pass.

## Good outcome

A good outcome is not “many skills were mentioned.” A good outcome is that the work moved through the right lifecycle stages in the right order with clear judgment and minimal wasted motion.
