---
name: memory-distiller
description: Distill repeated user preferences, successful patterns, and durable working rules into reusable memory notes or prompt-ready context blocks. Use when a user wants to capture habits, preserve preferences, summarize lessons from prior work, or convert raw conversation/task outcomes into structured memory.
---

# Memory Distiller

## Overview

Use this skill when the user wants to turn raw interaction history into stable,
reusable memory. The goal is not to summarize everything. The goal is to keep
only the parts that are durable enough to improve future work.

Read `references/output-format.md` when the user wants a structured output
template, a prompt-ready context block, or a reusable memory profile format.

## When To Use

Use this skill when the user asks to:

- capture recurring preferences or habits
- preserve successful working patterns
- record constraints, defaults, or anti-patterns
- turn task outcomes into future-facing rules
- clean up or refine an existing memory/profile document
- produce a compact context block for reuse in future prompts

Do not use this skill for:

- one-off conversational summaries
- temporary task state that will expire quickly
- guesses about user preferences that are not supported by evidence
- hidden or background memory injection into runtime code paths

## Core Rule

Only preserve information that looks durable.

Good candidates:

- stable preferences
- repeated defaults
- persistent constraints
- explicit dislikes
- reusable procedures
- recurring failure-avoidance rules

Weak candidates:

- one-off requests
- temporary deadlines
- transient debugging state
- personal guesses not explicitly supported by the source material

When a memory candidate is uncertain, mark it as tentative or exclude it.

## Workflow

### 1. Gather source material

Start from the material the user provides or points to:

- conversation excerpts
- task outcomes
- prior memory notes
- preference documents
- review summaries

If the source material is large, first compress it into candidate signals rather
than copying everything forward.

### 2. Extract candidate memories

Look for statements that imply stable behavior, such as:

- "always"
- "prefer"
- "do not"
- "default to"
- "use X when Y"
- repeated successful patterns across multiple examples

Group candidates into a small set of categories:

- preferences
- defaults
- constraints
- anti-patterns
- reusable procedures

### 3. Remove weak or noisy items

Drop any item that is:

- purely situational
- contradicted by newer evidence
- too vague to be useful
- likely to cause bad prompt injection if reused blindly

Prefer precision over recall. A small memory set with strong signal is better
than a large noisy list.

### 4. Rewrite into future-facing rules

Rewrite valid items as clear, reusable guidance.

Prefer forms like:

- "Prefer concise technical explanations."
- "Use JSON output when the user asks for machine-readable results."
- "Avoid storing one-off operational incidents as durable preferences."

Avoid forms like:

- "The user once asked..."
- "Yesterday they said..."
- "Maybe they prefer..."

### 5. Produce the requested output

Choose the narrowest useful output for the user:

- memory profile
- cleaned memory list
- prompt-ready context block
- review of existing memory quality

If the user does not specify a format, default to:

1. Stable preferences
2. Working rules
3. Anti-patterns
4. A short reusable context block

## Output Guidance

When producing memory content:

- keep wording concise
- keep claims evidence-based
- prefer durable rules over narrative summaries
- avoid hidden assumptions about the user
- separate "confirmed" from "tentative" when needed

If a prompt-ready context block is requested, keep it short enough that it can
realistically be reused without bloating future prompts.

## Safety And Quality

- Do not invent personal traits or preferences.
- Do not retain sensitive details unless the user clearly wants them preserved.
- Do not turn one failure into a permanent rule without evidence that it is recurring.
- When in doubt, exclude the item or mark it tentative.
