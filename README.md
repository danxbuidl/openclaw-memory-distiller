# openclaw-memory-distiller

`memory-distiller` is an OpenClaw skill for turning repeated user preferences,
successful patterns, and durable operating rules into reusable memory notes.

It is designed for workflows like:

- extracting stable preferences from conversations
- turning task outcomes into reusable rules
- producing prompt-ready context blocks from prior work
- separating durable memory from one-off chatter

## Skill

The published skill lives at:

- `memory-distiller/SKILL.md`

## Installation

Until this skill is published to ClawHub, install it by copying or cloning the
`memory-distiller/` directory into one of OpenClaw's skill locations:

- workspace-local: `./skills/memory-distiller`
- shared user install: `~/.openclaw/skills/memory-distiller`

After placing the skill, start a new OpenClaw session so the skill snapshot
refreshes.

## Usage

Call the skill explicitly with `$memory-distiller`.

Example prompts:

- `Use $memory-distiller to extract durable preferences from this conversation.`
- `Use $memory-distiller to turn these task outcomes into reusable working rules.`
- `Use $memory-distiller to create a concise context block I can reuse next time.`
- `Use $memory-distiller to review this memory profile and remove weak or temporary items.`

## What it produces

Depending on the request, the skill can help generate:

- a compact memory profile
- a prompt-ready context block
- a rules checklist for future tasks
- a cleanup pass that removes weak or temporary memories

## Design principles

This skill is intentionally conservative:

- it prefers durable rules over narrative summaries
- it avoids inventing user preferences
- it separates stable memory from one-off chatter
- it keeps prompt-ready context blocks compact enough to be reusable

## Repository structure

- `memory-distiller/SKILL.md` - core skill behavior
- `memory-distiller/agents/openai.yaml` - UI-facing metadata
- `memory-distiller/references/output-format.md` - structured output patterns

## Repository goal

This repository is intended to host a standalone OpenClaw skill that can be
published to ClawHub and improved independently from core runtime changes.

## Status

Current status:

- standalone repository created
- first working skill draft implemented
- preparing for public iteration and ClawHub publication
