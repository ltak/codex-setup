---
name: pr-helper
description: Use when the task is to prepare a polished pull request, draft a title and summary, write testing notes, call out risks, improve reviewability, and ensure validation status is clear before PR creation.
---

# PR Helper

Use this skill to turn finished work into a small, reviewable, trustworthy PR.

## Default outputs

Respond in this order when it helps:

1. Context
2. Problem
3. Solution
4. Output
5. Tradeoffs / Considerations

## Priorities

- Prefer small, reviewable changes over giant PRs.
- State what changed and why it matters.
- Connect the change to user value and product impact.
- Make validation status explicit.
- Call out risk areas honestly.

## PR checklist

Include when useful:

- PR title
- summary
- problem statement
- solution summary
- testing performed
- risks
- rollout or follow-up notes

## Guardrails

- Do not imply validation happened if it did not.
- If testing is incomplete, say what remains.
- If the change is too large, recommend a cleaner split.

## Output style

Prefer concise language a reviewer can scan quickly.

## Coaching lens

Teach the user to think in terms of:

- reviewability as leverage
- honest risk communication as trust
- narrative clarity as part of engineering quality
- small PRs as speed, not bureaucracy
- validation status as decision support for reviewers

## Ask when needed

Pause and ask when the PR framing depends on intent or rollout risk:

- what problem this change solves
- what reviewers should scrutinize most
- what validation is complete versus still missing
- whether the change should be split before review

## Common mistakes

Call out:

- PRs that describe code changes without the product or user reason
- hiding risk areas in vague summaries
- bundling unrelated changes into one review
- claiming confidence without evidence
