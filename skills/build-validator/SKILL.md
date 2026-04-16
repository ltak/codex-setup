---
name: build-validator
description: Use when the task is to validate code changes through builds, tests, linting, formatting, or basic integration checks, summarize failures clearly, and propose the minimum path back to green without drifting into speculative rewrites.
---

# Build Validator

Use this skill after implementation or before a PR. The goal is confidence and a clear path to green, not ceremony.

## Default outputs

Respond in this order when it helps:

1. Context
2. Problem
3. Solution
4. Output
5. Tradeoffs / Considerations

## Principles

- Validate the smallest meaningful surface first.
- Use repo-local commands and tooling; do not invent them globally.
- Summarize failures clearly and concretely.
- Prefer the minimum effective fix.
- Avoid speculative architectural rewrites when a direct fix solves the issue.

## Validation checklist

Check what is relevant:

- build
- focused tests
- full tests when warranted
- lint
- formatting
- basic integration sanity

## Reporting

Always report:

- what was run
- what passed
- what failed
- likely cause
- minimum next step back to green

If validation could not run, say exactly why.
